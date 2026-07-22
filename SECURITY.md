# Security & the one permanent boundary

Aris is delivered **only as a sealed, signed binary**. This repository — and every
repository in this program — contains **no engine source and no logic**, for **every**
audience, without exception: not the public, not customers, not members, not partners.
This is permanent and is not a limitation to be lifted "later."

## What lives here

Only things that are **yours to hold**: example **packs** (data), the pack data-contract
(a JSON Schema), the results-only **API reference**, and program docs. All of it is safe
to read, copy, and adapt.

## What is never here, ever

- Aris engine source, logic, algorithm descriptions, or internal module/import names
- The record substrate and anything describing how it works
- Signing keys or key material of any kind
- Real customer records

You build **on** Aris through data and the API. You never read Aris. Because the logic
was never placed here, there is nothing in this repository that could leak it.

Receipt **verification** is public by design — anyone can prove an answer is genuine
with a public key, and that proves nothing about how the answer was produced. Verifiers
ship as sealed tools; public keys ship with membership. Signing keys never leave the
sealed core.

## For contributors

CI (`.github/workflows/guard.yml`) fails any change that introduces source code, key
material, or real records. Contributions are limited to **packs, connectors, and
integration examples** — data and documentation only. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Reporting

Report anything sensitive **privately** to your program contact — never in a public
issue. If you believe any artifact here reveals more than an outcome, tell us privately
and we will remove it.
