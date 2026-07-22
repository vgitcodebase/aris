# Example tool — Clinic Scheduling & Visits

A **complete, finished tool** built on Aris — cited answers over outpatient clinic visits:
volume, wait times, charges, and reimbursement by clinic, department, and provider. Clone this
folder, point it at your own (de-identified) records, and you have a working tool. Everything
here is **data and docs** — no code to read or run.

## What's in the box

| File | What it is |
| --- | --- |
| [../../packs/clinic-scheduling.rulepack.json](../../packs/clinic-scheduling.rulepack.json) | The **pack** (in the shared pack library) — your fields, your words, your phrasing |
| [records.sample.jsonl](records.sample.jsonl) | **14 synthetic visit records** to answer over (swap in your own) |
| [connector.emr-export.json](connector.emr-export.json) | A **connector** — maps a common EMR/PM visit export onto the pack's fields (data, no code) |
| [answers.md](answers.md) | **The tool in action** — real questions and the exact cited, signed answers |

## Use it in three moves

1. **Load** the pack + records (or map your own EMR export with the connector — de-identified
   records only).
2. **Ask** in plain English — "how many visits at Lakeshore Orthopedics?", "average wait in
   Orthopedics?", "what did we collect from Riverbend Pediatrics?", "pull up the injection visit".
3. **Trust it** — every answer is a real record or an honest "no record," each with a signed
   receipt. Aris answers **only from the record** and never infers clinical content. See
   [answers.md](answers.md).

Change the words, change the records, add fields — it's your tool. Nothing sealed leaks.
