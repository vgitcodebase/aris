# Example tool — Lending Portfolio

A **complete, finished tool** built on Aris — cited answers over a lending book: principal,
interest, rate, and loan-to-value by lender, borrower, and product. Clone this folder, point it
at your own (de-identified) book, and you have a working tool. Everything here is **data and
docs** — no code.

## What's in the box

| File | What it is |
| --- | --- |
| [../../packs/lending-portfolio.rulepack.json](../../packs/lending-portfolio.rulepack.json) | The **pack** (shared pack library) — fields, words, phrasing |
| [records.sample.jsonl](records.sample.jsonl) | **14 synthetic loan records** to answer over |
| [connector.loan-servicing-export.json](connector.loan-servicing-export.json) | A **connector** — maps a loan-servicing export onto the pack's fields (data, no code) |
| [answers.md](answers.md) | **The tool in action** — real questions and the exact cited, signed answers |

## Use it in three moves

1. **Load** the pack + records (or map your own servicing export with the connector —
   de-identified records only).
2. **Ask** — "how many loans through Harbor Trust?", "total principal with Summit Community
   Bank?", "average rate on Equipment Finance loans?", "which loan has the highest LTV?".
3. **Trust it** — every answer is a real record or an honest "no record," each signed and
   verifiable. Aris answers **only from the record**. See [answers.md](answers.md).

Change the words, the records, the fields — it's your tool. Nothing sealed leaks.
