# Example tool — Commercial Leasing

A **complete, finished tool** built on Aris — cited answers over a commercial lease portfolio:
rent, TI allowances, term, and occupancy by property and tenant. Clone this folder, point it at
your own rent roll, and you have a working tool. Everything here is **data and docs** — no code.

## What's in the box

| File | What it is |
| --- | --- |
| [../../packs/commercial-leasing.rulepack.json](../../packs/commercial-leasing.rulepack.json) | The **pack** (shared pack library) — fields, words, phrasing |
| [records.sample.jsonl](records.sample.jsonl) | **14 synthetic lease records** to answer over |
| [connector.lease-admin-export.json](connector.lease-admin-export.json) | A **connector** — maps a lease-admin export onto the pack's fields (data, no code) |
| [answers.md](answers.md) | **The tool in action** — real questions and the exact cited, signed answers |

## Use it in three moves

1. **Load** the pack + records (or map your own lease-admin export with the connector).
2. **Ask** — "how many leases at Beacon Tower?", "total annual rent at Riverside Logistics
   Park?", "average occupancy?", "pull up the FreshField lease at Gateway Commons".
3. **Trust it** — every answer is a real record or an honest "no record," each signed and
   verifiable. See [answers.md](answers.md).

Change the words, the records, the fields — it's your tool. Nothing sealed leaks.
