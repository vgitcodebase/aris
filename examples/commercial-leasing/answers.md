# The tool in action — what you get back

Real answers over the 14 leases in [records.sample.jsonl](records.sample.jsonl), using the
[commercial-leasing pack](../../packs/commercial-leasing.rulepack.json). Every answer is a real
record or an honest "no record," each with a signed receipt you can verify.

---

**Q. "How many leases at Beacon Tower?"**

> There are **4** records matching "beacon tower".
> *Computed by Validiti Maths · signed by Validiti Mark ✓ verified*

**Q. "What's the total annual rent at Riverside Logistics Park?"**

> Across 3 records matching "riverside logistics park", the total **annual rent** is **$2,490,000**.
> *signed ✓ verified*

**Q. "What's our average occupancy across all leases?"**

> Across 14 records, the average **occupancy** is **92.9%**.
> *signed ✓ verified · (one medical suite sits vacant)*

**Q. "Which lease has the largest TI allowance?"**

> The highest **TI allowance** is **$420,000**.
> *(LSE-4009 — Lakeshore Orthopedics at Summit Medical Plaza, Madison WI)*

**Q. "Pull up the FreshField Grocers lease at Gateway Commons."** *(a lookup)*

> **FreshField Grocers at Gateway Commons in Denver, CO — Retail space. Status: Active.**
> Cited source · **LSE-4003** · fingerprint `…` ✓ · Signed by Validiti Mark ✓ verified

**Q. "How many leases on the Moon?"** *(not in the records)*

> I have no record matching that — so I won't guess.
> *Even the "I don't know" is signed by Validiti Mark ✓*

---

Swap in your own leases (see [connector.lease-admin-export.json](connector.lease-admin-export.json))
and the same questions answer on your portfolio.
