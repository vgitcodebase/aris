# Starter kit — your launchpad

New here? Don't start from a blank file. Copy one of these, change the words to match
your world, and you have a working pack. Everything in this kit is **data** — adapt it
freely.

## Phrasebook

- **[packs/starter-vocab.json](packs/starter-vocab.json)** — common words your people say
  for a total, an average, a count, and the field-kind each business word usually points
  at. Lift what fits; rename the rest.

## Example packs — pick the closest and adapt

| Pack | Domain | Good starting point if your records are… |
| --- | --- | --- |
| [signage](packs/signage.rulepack.json) | Signage / installations | projects with brands, products, margins |
| [retail-store-network](packs/retail-store-network.rulepack.json) | Multi-store retail | stores with sales, rent, margin |
| [logistics-freight](packs/logistics-freight.rulepack.json) | Freight / logistics | shipments with lanes, cost, reliability |
| [commercial-leasing](packs/commercial-leasing.rulepack.json) | Commercial real estate | leases with rent, term, occupancy |
| [field-service](packs/field-service.rulepack.json) | Field service | work orders with labor, parts, SLA |
| [lending-portfolio](packs/lending-portfolio.rulepack.json) | Lending / finance | loans with principal, rate, LTV |
| [clinic-scheduling](packs/clinic-scheduling.rulepack.json) | Healthcare ops | visits with charges, waits, providers |

## Three steps to your own pack

1. **Copy the closest example** above into `packs/your-domain.rulepack.json`.
2. **Edit four things** to match your records — see [PACKS.md](PACKS.md):
   your fields, your words, how numbers read, and how a record reads back as a sentence.
   Borrow words from [starter-vocab.json](packs/starter-vocab.json).
3. **Validate** before you publish:
   `check-jsonschema --schemafile packs/pack.schema.json packs/your-domain.rulepack.json`

Then open a pull request — see [CONTRIBUTING.md](CONTRIBUTING.md). Use synthetic example
records only; never real customer data.

## What this kit is (and isn't)

It's a set of **phrasebooks** — starting words and shapes for your domain. It is not, and
never will be, how Aris understands or answers; that ships sealed. You copy examples and
teach Aris your world. You never open the engine. See [SECURITY.md](SECURITY.md).
