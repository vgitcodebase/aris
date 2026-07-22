# Example tool — Field Audit Trail

A **complete, finished tool** built on Aris, not just instructions. Clone this folder,
point it at your own records, and you have a working cited-answer tool for equipment
audits — "who inspected what, where, the result, time, cost, and compliance."

Everything here is **data and docs** — there is no code to read or run. Aris (sealed) does
the work; this folder is what *you* provide.

## What's in the box

| File | What it is |
| --- | --- |
| [field-audit.rulepack.json](field-audit.rulepack.json) | The **pack** — your fields, your words, your answer phrasing (data) |
| [records.sample.jsonl](records.sample.jsonl) | **14 synthetic audit records** to answer over (swap in your own) |
| [connector.csv-export.json](connector.csv-export.json) | A **connector** — maps a common CMMS/work-order CSV export onto the pack's fields (data, no code) |
| [answers.md](answers.md) | **The tool in action** — real questions and the exact cited, signed answers you get back |

## Use it in three moves

1. **Load** the pack + records (or map your own export with the connector).
2. **Ask** in plain English — "how many audits in Dallas?", "average compliance?",
   "pull up the audit for Pump-07", "who audited the Mars rover?"
3. **Trust it** — every answer is a real record or an honest "no record," each with a
   signed receipt you can verify yourself. See [answers.md](answers.md).

## Make it yours

- Change the **words** in the pack to match how your team talks.
- Change the **records** to your own (the connector shows how to bring a CSV export in).
- Add fields — cost, downtime, parts, whatever your audits carry.

That's the whole tool. No engine, no logic, nothing sealed leaks — you build on Aris with
data, and Aris answers with citations and receipts. See the repo
[README](../../README.md) and [PACKS.md](../../PACKS.md) to go further.
