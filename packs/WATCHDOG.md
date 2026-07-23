# Watchdog rules — teach Aris what "doesn't add up" (pack v1)

A `watchdog` section is a list of consistency rules Aris checks across your records and
signs. Records that break a rule are flagged with **your** message and the reason; every
other record stays silent — a clean, signed bill of health. It turns Aris from something
you ask into something that also *watches*: it surfaces the entry that's wrong before you
go looking.

All declarative. You describe what should always be true; you never write code.

Add a `watchdog` array to your pack, keep `"version": "1"`, and validate against
[`pack.schema.json`](pack.schema.json).

---

## Four rule kinds

### `compare` — a value must stay within a bound
```json
{ "kind": "compare", "field": "ltv_pct", "op": "<=", "value": 100,
  "message": "loan-to-value over 100% — the loan is larger than its collateral" }
```

### `formula` — a value must match a relationship of other fields
Give an arithmetic relationship among your fields with `+ - * / ( )` and one `==`. Aris
flags any record where the two sides differ by more than `tolerance`. This catches edited
or fat-fingered numbers that no longer reconcile with each other.
```json
{ "kind": "formula",
  "expr": "margin_pct == (contract - build_cost) / contract * 100",
  "tolerance": 0.6,
  "message": "the stated margin doesn't match contract minus cost" }
```

### `order` — one date/step must not come after another
```json
{ "kind": "order", "before": "originated", "after": "closed",
  "message": "closed before it was originated" }
```

### `outlier` — values far outside the normal range
```json
{ "kind": "outlier", "field": "rate_pct", "method": "iqr", "k": 3,
  "message": "rate is far outside the normal range for this book" }
```

---

## How it reads back
Aris checks every record and answers with the count and the reasons — for example:

> I checked **3,000** records. **3** don't add up — here's exactly why.
> - LN‑5102 — loan-to-value **112%**: the loan is larger than its collateral
> - LN‑5140 — rate **19.5%** is far outside the normal range for this book
> - LN‑5177 — closed before it was originated

Ask it against a slice, too — *"check the Texas loans"* — and if they're clean, it says so.

## A note on scope
Watchdog rules are about **your** records against **your** rules. They don't reach outside
your data, and the reason shown is the plain-English message you wrote. The result is
signed like every other answer, so a clean bill is something you can hand to an auditor.
