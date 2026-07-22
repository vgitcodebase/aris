# Example tool — Retail Store Network

A **complete, finished tool** built on Aris — cited answers over a multi-store retail chain:
sales, rent, margin, and format by location. Clone this folder, point it at your own stores,
and you have a working tool. Everything here is **data and docs** — no code to read or run.

## What's in the box

| File | What it is |
| --- | --- |
| [../../packs/retail-store-network.rulepack.json](../../packs/retail-store-network.rulepack.json) | The **pack** (in the shared pack library) — your fields, your words, your phrasing |
| [records.sample.jsonl](records.sample.jsonl) | **14 synthetic store records** to answer over (swap in your own) |
| [connector.pos-export.json](connector.pos-export.json) | A **connector** — maps a common POS/back-office export onto the pack's fields (data, no code) |
| [answers.md](answers.md) | **The tool in action** — real questions and the exact cited, signed answers |

## Use it in three moves

1. **Load** the pack + records (or map your own POS export with the connector).
2. **Ask** in plain English — "how many FreshField stores?", "total sales in Denver?",
   "average margin at UrbanThreads?", "pull up the QuickMart Domain store".
3. **Trust it** — every answer is a real record or an honest "no record," each with a signed
   receipt you can verify. See [answers.md](answers.md).

Change the words, change the records, add fields — it's your tool. Nothing sealed leaks; you
build on Aris with data, and Aris answers with citations and receipts.
