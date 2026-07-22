# Example tool — Signage Projects

A **complete, finished tool** built on Aris — cited answers over a book of signage/installation
projects: contract value, build cost, margin, and quantity by client, product, and partner.
Clone this folder, point it at your own jobs, and you have a working tool. Everything here is
**data and docs** — no code.

## What's in the box

| File | What it is |
| --- | --- |
| [../../packs/signage.rulepack.json](../../packs/signage.rulepack.json) | The **pack** (shared pack library) — fields, words, phrasing |
| [records.sample.jsonl](records.sample.jsonl) | **14 synthetic project records** to answer over |
| [connector.project-erp-export.json](connector.project-erp-export.json) | A **connector** — maps a project/ERP export onto the pack's fields (data, no code) |
| [answers.md](answers.md) | **The tool in action** — real questions and the exact cited, signed answers |

## Use it in three moves

1. **Load** the pack + records (or map your own project export with the connector).
2. **Ask** — "how many projects for FreshField Grocers?", "total contract value in Denver?",
   "average margin on Summit Graphics jobs?", "pull up the UrbanThreads flagship storefront".
3. **Trust it** — every answer is a real record or an honest "no record," each signed and
   verifiable. See [answers.md](answers.md).

Change the words, the records, the fields — it's your tool. Nothing sealed leaks.
