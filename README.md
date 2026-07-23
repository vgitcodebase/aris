<h1>Trinity Web Services — Aris Developer Program</h1>

**The AI that cites its source.** Aris answers questions *only from your records* — it
shows the exact source and a signed receipt, and when there is no record it **says so
instead of guessing**. This is the developer hub for building on Aris.

> A chatbot guesses from a blurry memory and can't show you where the answer came from.
> **Aris answers are the record itself — cited, signed, and honest when it doesn't know.**

---

## What Trinity Web Services is

Four services and a set of A.I. support offerings, each delivering an outcome you can
verify:

| Service | What it does for you |
| --- | --- |
| **Aris** | Cited, signed answers over your records — computed or quoted, never guessed |
| **Genesis** | Choose-your-experience delivery over your data |
| **Abel** | Real sign / verify — provable authenticity |
| **Maths** | Compute-and-prove — every number carries a receipt |
| **A.I. support** | Managed A.I. services on the Trinity substrate |

This repository is the place where **members build on Aris**.

## How you build on Aris — with data, not code

You never touch our engine. You teach Aris your world by writing a **pack** — a small
data file describing *your* vocabulary and how *your* records should read back:

- the words your people say for a total, an average, a count;
- the fields your records carry;
- how a matched record becomes a plain-English answer.

You publish the pack, point Aris at your records through the API, and you get cited and
computed answers with signed receipts. That's the whole surface.

**Want to see a finished tool first?** [examples/](examples) has **seven complete worked tools** —
each a pack, 14 real records, a connector, and the exact cited, signed answers it gives back.
Clone one, point it at your records, done:
[field-audit](examples/field-audit),
[retail-store-network](examples/retail-store-network),
[clinic-scheduling](examples/clinic-scheduling),
[logistics-freight](examples/logistics-freight),
[commercial-leasing](examples/commercial-leasing),
[lending-portfolio](examples/lending-portfolio),
[signage](examples/signage).

**Ready to build? Start with the [Starter Kit](STARTER-KIT.md)** — a phrasebook plus seven
worked example packs (signage, retail, logistics, leasing, field service, lending,
clinic). Copy the closest one and change the words. See **[PACKS.md](PACKS.md)** for the
four things a pack defines.

### You can teach Aris a lot more — still with data only

A pack can go well beyond basic questions, all by writing data about *your* world:

- **Talk like your team** — map your idioms and shorthand ("fast food", "bleeding money",
  "high-risk", "underwater") to your fields, and let "where / who / when" answer directly.
  See **[packs/UNDERSTANDING.md](packs/UNDERSTANDING.md)**.
- **Ask relative-time questions** — "this year", "last quarter", "in 2025".
- **Hold a conversation** — ask, then follow up ("what about Texas", "just the high-risk
  ones", "average rate on those") and Aris keeps the thread — cited and signed at every step.
- **Let Aris watch your books** — declare what should always be true and Aris flags the
  records that don't add up, with your message. See **[packs/WATCHDOG.md](packs/WATCHDOG.md)**.

The worked **[packs/lending-portfolio.rulepack.json](packs/lending-portfolio.rulepack.json)**
shows every one of these. None of it is code — you describe your world, the sealed engine
does the rest.

```
Your records  ──▶  Aris (sealed)  ──▶  cited / computed answer + signed receipt
   your pack ─────────▲                         you verify it yourself
```

## Why this is different

- **Grounded.** Every answer resolves to a real record, or an honest "no record."
- **Signed.** Every answer — even "I don't know" — carries a receipt you can verify
  offline with a public key. You never have to trust us; you can *check*.
- **Yours to extend.** Your packs are your data. Build any vertical — retail, clinics,
  field service, finance — without waiting on us and without exposing your data to us.

## Get access

Aris is available to people who hold it through a Trinity service or contract. There's
a **free, limited tier** to build and prove value, and **member / partner** tiers for
production and custom verticals. See **[PROGRAM.md](PROGRAM.md)**.

> **Downloads are Coming Soon** — binaries land with the Series 1 launch. Join the
> program to be first in line.

## Contribute

The community pack library is the heart of this program — every domain someone packs
makes Aris more useful for everyone. Contributions are welcome for **packs, connectors,
and integration examples**. See **[CONTRIBUTING.md](CONTRIBUTING.md)**.

## Packs the community could build

The seven worked tools above are a start, not the map. **If your field keeps records with
names, places, money, counts, and status, it can be a pack.** Here are open domains worth
building — pick one, model ~14 synthetic records, and open a PR:

| Domain | Records look like… | Questions it would answer |
| --- | --- | --- |
| **Insurance claims** | claim, adjuster, peril, payout, status | "total payouts in Florida?", "average cycle time by adjuster?" |
| **Construction / GC** | job, trade, change orders, cost, phase | "which job has the most change orders?", "total committed cost?" |
| **Hospitality / hotels** | property, room nights, ADR, occupancy | "average ADR in Q3?", "occupancy at the downtown property?" |
| **Municipal permits** | permit, department, fee, applicant, status | "how many permits pending review?", "total fees collected?" |
| **Manufacturing runs** | line, product, yield, downtime, shift | "worst-yield line last month?", "total downtime by plant?" |
| **Legal matters** | matter, practice, client, hours, billing | "hours on the Acme matter?", "average bill by practice?" |
| **Grants / nonprofit** | grant, program, funder, award, spend | "total awarded this year?", "spend-down on the youth program?" |
| **Fleet management** | vehicle, driver, mileage, maintenance cost | "highest-mileage vehicle?", "total maintenance by depot?" |
| **Warranty / RMA** | return, product, reason, cost, disposition | "top return reason?", "warranty cost by product line?" |
| **Sales pipeline** | deal, rep, stage, value, close date | "pipeline value by rep?", "how many deals in negotiation?" |
| **Higher-ed enrollment** | program, term, headcount, tuition, status | "enrollment by program?", "total tuition this term?" |
| **Utilities / assets** | asset, feeder, output, outages, region | "outage count by region?", "total output by substation?" |

Copy the closest [example tool](examples), keep the four-part shape (your fields, your
words, how numbers read, how a record reads back), add synthetic records, and — importantly —
**verify your walkthrough numbers against your own records** before you PR. Aris is the AI
that cites; an example has to be exact.

## The one boundary

Aris ships **only as a sealed, signed binary**, and this repository contains **no engine
source and no logic** — by design, permanently, for every audience. You build on Aris;
you never read Aris. See **[SECURITY.md](SECURITY.md)**.

---

<sub>© 2026 Brian Michael Smith (CrashOverride). "Trinity Web Services", "Aris",
"Genesis", "Abel", "Maths", and "Mark" are brands of their owner. Example packs and
docs are provided under the terms in [LICENSE](LICENSE) / [NOTICE](NOTICE).</sub>
