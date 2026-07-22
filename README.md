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

**Want to see a finished tool first?** [examples/field-audit](examples/field-audit) is a
**complete worked tool** — a pack, 14 real records, a connector, and the exact cited,
signed answers it gives back. Clone it, point it at your records, done.

**Ready to build? Start with the [Starter Kit](STARTER-KIT.md)** — a phrasebook plus seven
worked example packs (signage, retail, logistics, leasing, field service, lending,
clinic). Copy the closest one and change the words. See **[PACKS.md](PACKS.md)** for the
four things a pack defines.

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

## The one boundary

Aris ships **only as a sealed, signed binary**, and this repository contains **no engine
source and no logic** — by design, permanently, for every audience. You build on Aris;
you never read Aris. See **[SECURITY.md](SECURITY.md)**.

---

<sub>© 2026 Brian Michael Smith (CrashOverride). "Trinity Web Services", "Aris",
"Genesis", "Abel", "Maths", and "Mark" are brands of their owner. Example packs and
docs are provided under the terms in [LICENSE](LICENSE) / [NOTICE](NOTICE).</sub>
