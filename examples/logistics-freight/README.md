# Example tool — Logistics & Freight

A **complete, finished tool** built on Aris — cited answers over freight shipments: cost,
revenue, transit, and on-time performance by carrier and lane. Clone this folder, point it at
your own loads, and you have a working tool. Everything here is **data and docs** — no code.

## What's in the box

| File | What it is |
| --- | --- |
| [../../packs/logistics-freight.rulepack.json](../../packs/logistics-freight.rulepack.json) | The **pack** (shared pack library) — fields, words, phrasing |
| [records.sample.jsonl](records.sample.jsonl) | **14 synthetic shipment records** to answer over |
| [connector.tms-export.json](connector.tms-export.json) | A **connector** — maps a common TMS export onto the pack's fields (data, no code) |
| [answers.md](answers.md) | **The tool in action** — real questions and the exact cited, signed answers |

## Use it in three moves

1. **Load** the pack + records (or map your own TMS export with the connector).
2. **Ask** — "how many shipments on the Seattle-Denver lane?", "total freight cost with
   BlueLine?", "average on-time for Cascade Carriers?", "pull up the Dallas-Phoenix FTL shipment".
3. **Trust it** — every answer is a real record or an honest "no record," each signed and
   verifiable. See [answers.md](answers.md).

Change the words, the records, the fields — it's your tool. Nothing sealed leaks.
