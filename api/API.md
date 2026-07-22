# Aris API reference

You reach Aris over a simple HTTP API. You send a question; Aris returns a grounded
answer with a signed receipt. Point your own client at it in any language — the API is
all you need; there is nothing to install to *read* Aris.

Base URL is issued with your membership. All responses are JSON.

## Ask a question

```
GET  {base}/ask?q=<your question>
```

Aris decides, from your pack, whether the question wants a **quoted record** or a
**computed number**, and answers accordingly.

**Cited answer** — a record:

```json
{
  "grounded": true,
  "kind": "cite",
  "answer": "For Walmart, we ran Wayfinding in Dallas, TX using the Interior Wayfinding Suite. Status: In service.",
  "cited": [{ "id": "PRJ-2", "brand": "Walmart", "fingerprint": "…", "fingerprint_ok": true }],
  "receipt": { "signer": "Validiti Mark", "fingerprint": "…", "signature": "…", "verified": true }
}
```

**Computed answer** — a number over records:

```json
{
  "grounded": true,
  "kind": "compute",
  "answer": "Across 159 records matching \"walmart\", the total contract value is $1,325,866.",
  "value": "$1,325,866",
  "records_used": 159,
  "receipt": { "signer": "Validiti Mark", "fingerprint": "…", "signature": "…", "verified": true }
}
```

**No record** — the honest miss:

```json
{
  "grounded": false,
  "kind": "cite",
  "answer": "I have no record matching that — so I won't guess.",
  "receipt": { "signer": "Validiti Mark", "verified": true }
}
```

Note that even "I don't know" is signed.

## Verify a receipt yourself

Every answer carries a receipt. You can confirm it is genuine **offline**, with only the
published signer public key — you never have to trust the endpoint, you can check it:

1. Recompute the fingerprint from the answer content and compare.
2. Verify the signature over that fingerprint with the signer's Ed25519 public key.

A conforming verifier is distributed as a sealed Trinity tool; the public key ships with
your membership. Verification is public by design — proving an answer never reveals how
it was produced.

## Health

```
GET  {base}/health   →   { "ok": true, "signer": "Validiti Mark" }
```

> These endpoints describe **outcomes** — what you send and what you get back. How Aris
> produces them is sealed inside the binary and is not part of any client integration.
