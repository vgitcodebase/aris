# The tool in action — what you get back

Real answers over the 14 shipments in [records.sample.jsonl](records.sample.jsonl), using the
[logistics-freight pack](../../packs/logistics-freight.rulepack.json). Every answer is a real
record or an honest "no record," each with a signed receipt you can verify.

---

**Q. "How many shipments on the Seattle-Denver lane?"**

> There are **4** records matching "seattle-denver".
> *Computed by Validiti Maths · signed by Validiti Mark ✓ verified*

**Q. "What's our total freight cost with BlueLine Freight?"**

> Across 5 records matching "blueline freight", the total **freight cost** is **$10,630**.
> *signed ✓ verified*

**Q. "What's the average on-time rate for Cascade Carriers?"**

> Across 5 records matching "cascade carriers", the average **on-time rate** is **80.0%**.
> *signed ✓ verified · (one Reefer run to Denver ran late)*

**Q. "Which shipment took the longest?"**

> The highest **transit (days)** is **6**.

**Q. "Pull up the Dallas-Phoenix FTL shipment."** *(a lookup)*

> **BlueLine Freight on the Dallas-Phoenix lane (Dallas → Phoenix) by FTL. Status: Delivered.**
> Cited source · **SHP-3007** · fingerprint `…` ✓ · Signed by Validiti Mark ✓ verified

**Q. "How many shipments to the Moon?"** *(not in the records)*

> I have no record matching that — so I won't guess.
> *Even the "I don't know" is signed by Validiti Mark ✓*

---

Swap in your own shipments (see [connector.tms-export.json](connector.tms-export.json)) and the
same questions answer on your lanes.
