# The tool in action — what you get back

Real answers over the 14 stores in [records.sample.jsonl](records.sample.jsonl), using the
[retail-store-network pack](../../packs/retail-store-network.rulepack.json). Every answer is a
real record or an honest "no record," each with a signed receipt you can verify.

---

**Q. "How many FreshField stores do we have?"**

> There are **5** records matching "freshfield".
> *Computed by Validiti Maths · signed by Validiti Mark ✓ verified*

**Q. "What's our total monthly sales in Denver?"**

> Across 4 records matching "denver", the total **monthly sales** is **$2,383,000**.
> *signed ✓ verified*

**Q. "What's the average margin at UrbanThreads?"**

> Across 4 records matching "urbanthreads", the average **margin** is **46.8%**.
> *signed ✓ verified*

**Q. "Which store earned the highest margin?"**

> The highest **margin** is **48.6%**.
> *(STR-205 — UrbanThreads Gallery, Portland OR)*

**Q. "Pull up the QuickMart Domain store."** *(a lookup)*

> **QuickMart — QuickMart Domain in Austin, TX (Convenience) managed by Rosa Delgado.
> Status: Open.**
> Cited source · **STR-213** · fingerprint `…` ✓ · Signed by Validiti Mark ✓ verified

**Q. "How many stores do we have in Paris?"** *(not in the records)*

> I have no record matching that — so I won't guess.
> *Even the "I don't know" is signed by Validiti Mark ✓*

---

Swap in your own store records (see [connector.pos-export.json](connector.pos-export.json))
and the same questions answer on your chain.
