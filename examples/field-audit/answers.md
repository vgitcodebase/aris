# The tool in action — what you get back

These are real answers over the 14 records in
[records.sample.jsonl](records.sample.jsonl), using the
[field-audit pack](field-audit.rulepack.json). Every answer is either a real record
or an honest "no record" — and every one carries a signed receipt you can verify.
Ask them yourself once the tool is loaded.

---

**Q. "How many audits did we run in Dallas?"**

> There are **4** records matching "dallas".
> *Computed by Validiti Maths · signed by Validiti Mark ✓ verified*

**Q. "What's our average compliance across all audits?"**

> Across 14 records, the average **compliance** is **88.7%**.
> *Computed over 14 records · signed ✓ verified*

**Q. "Which audit had the worst compliance?"**

> The lowest **compliance** is **58.0%**.
> *(AUD-1009 — Priya Nair, leak test on Ammonia Chiller B, Gulfport MS — result Fail)*

**Q. "What did we spend on audits at Harbor Cold Storage?"**

> Across 4 records matching "harbor cold storage", the total **cost** is **$3,395**.
> *signed ✓ verified*

**Q. "Pull up the audit for Pump-07 at the Riverside center."** *(a lookup)*

> **Marcus Lee performed seal replacement on the Pump-07 at Riverside Distribution
> Center (Dallas, TX) — result: Conditional. Status: Follow-up.**
> Cited source · **AUD-1002** · fingerprint `…` ✓ · Signed by Validiti Mark ✓ verified

**Q. "Who audited the Mars rover?"** *(not in the records)*

> I have no record matching that — so I won't guess.
> *Even the "I don't know" is signed by Validiti Mark ✓*

---

That last one is the whole point: the tool answers **only from your records**, shows the
exact source, and says so plainly when the answer isn't there. Swap in your own records
(see [connector.csv-export.json](connector.csv-export.json)) and the same questions work
on your world.
