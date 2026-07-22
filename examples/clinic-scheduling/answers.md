# The tool in action — what you get back

Real answers over the 14 visits in [records.sample.jsonl](records.sample.jsonl), using the
[clinic-scheduling pack](../../packs/clinic-scheduling.rulepack.json). Every answer is a real
record or an honest "no record," each with a signed receipt you can verify.

---

**Q. "How many visits at Lakeshore Orthopedics?"**

> There are **5** records matching "lakeshore orthopedics".
> *Computed by Validiti Maths · signed by Validiti Mark ✓ verified*

**Q. "What's the average wait time in Orthopedics?"**

> Across 5 records matching "orthopedics", the average **wait (minutes)** is **38.8**.
> *signed ✓ verified*

**Q. "What did we collect from Riverbend Pediatrics?"**

> Across 4 records matching "riverbend pediatrics", the total **amount reimbursed** is **$560**.
> *signed ✓ verified*

**Q. "Which visit had the longest wait?"**

> The highest **wait (minutes)** is **52**.
> *(VIS-511 — consult with Dr. Owen Brand, Lakeshore Orthopedics, Madison WI)*

**Q. "Pull up the injection visit at Lakeshore."** *(a lookup)*

> **At Lakeshore Orthopedics, an injection visit in Orthopedics (Madison, WI) with
> Dr. Priya Anand. Status: Completed.**
> Cited source · **VIS-508** · fingerprint `…` ✓ · Signed by Validiti Mark ✓ verified

**Q. "How many visits in Tokyo?"** *(not in the records)*

> I have no record matching that — so I won't guess.
> *Even the "I don't know" is signed by Validiti Mark ✓*

---

Swap in your own visit records (see [connector.emr-export.json](connector.emr-export.json))
and the same questions answer on your clinics. No content is ever inferred — only what's on
the record.
