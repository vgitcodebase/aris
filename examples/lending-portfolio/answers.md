# The tool in action — what you get back

Real answers over the 14 loans in [records.sample.jsonl](records.sample.jsonl), using the
[lending-portfolio pack](../../packs/lending-portfolio.rulepack.json). Every answer is a real
record or an honest "no record," each with a signed receipt you can verify.

---

**Q. "How many loans do we have through Harbor Trust?"**

> There are **5** records matching "harbor trust".
> *Computed by Validiti Maths · signed by Validiti Mark ✓ verified*

**Q. "What's the total principal with Summit Community Bank?"**

> Across 5 records matching "summit community bank", the total **principal** is **$3,415,000**.
> *signed ✓ verified*

**Q. "What's the average rate on Equipment Finance loans?"**

> Across 3 records matching "equipment finance", the average **rate** is **6.6%**.
> *signed ✓ verified*

**Q. "Which loan has the highest loan-to-value?"**

> The highest **loan-to-value** is **82.0%**.
> *(LN-5008 — Cascade Carriers, Equipment Finance through Harbor Trust)*

**Q. "Pull up the IronRoad Logistics loan."** *(a lookup)*

> **IronRoad Logistics — Commercial Term Loan through Harbor Trust (Memphis, TN). Status: Watch.**
> Cited source · **LN-5004** · fingerprint `…` ✓ · Signed by Validiti Mark ✓ verified

**Q. "How much did we lend to the Wayne Foundation?"** *(not in the records)*

> I have no record matching that — so I won't guess.
> *Even the "I don't know" is signed by Validiti Mark ✓*

---

Swap in your own book (see [connector.loan-servicing-export.json](connector.loan-servicing-export.json))
and the same questions answer on your portfolio.
