# Authoring a pack

A **pack** is a small data file (JSON) that teaches Aris your world. It contains only
*your* domain description — your fields, your words, your answer phrasing. It is not
code, and it says nothing about how Aris works. You provide it; Aris does the rest.

A pack has four parts. Copy [packs/signage.rulepack.json](packs/signage.rulepack.json)
and adapt it, then check it against the contract in
[packs/pack.schema.json](packs/pack.schema.json).

### 1. `record_schema` — the fields your records carry
Name each field your records have and its kind (`string`, `money`, `percent`,
`number`). This is the shape of *your* data.

```json
"record_schema": {
  "id": "string", "brand": "string", "city": "string",
  "contract": "money", "margin_pct": "percent", "qty": "number"
}
```

### 2. `vocab` — the words your people use
Map the everyday words your users say to the field they mean and the kind of answer they
want. If your team says "spend" when they mean build cost, say so here.

```json
"vocab": {
  "agg":    { "average": "mean", "total": "sum", "how many": "count", "highest": "max" },
  "metric": { "margin": "margin_pct", "spend": "build_cost", "revenue": "contract" },
  "stop":   ["the", "a", "for", "our", "how", "many"]
}
```

### 3. `compute` — how a number should read
Give each number a unit and a plain label, so a computed answer comes back in your
language ("the **average margin** is **20.1%**", "**total contract value** is
**$1,325,866**").

```json
"compute": {
  "units":  { "margin_pct": "%", "contract": "$" },
  "labels": { "margin_pct": "margin", "contract": "contract value" }
}
```

### 4. `cite` — how a record reads back as a sentence
Describe how a matched record should be spoken as plain English, clause by clause. A
clause appears only when its fields are present, so answers never read awkwardly.

```json
"cite": {
  "template": [
    { "when": ["brand", "program"], "text": "For {brand}, we ran {program}" },
    { "when": ["city", "state"],    "text": "in {city}, {state}" }
  ],
  "fields": ["brand", "program", "city", "state", "contract"]
}
```

## Rules a pack always keeps

- **Records-first.** Every answer resolves to a real record or an honest "no record" —
  a pack can never conjure an answer from nothing.
- **Your data only.** A pack names your fields and your words. It has no way to reach
  anything inside Aris.
- **Signed for you.** The receipt on every answer is produced by Aris; a pack can't
  forge one, and you can verify it yourself.

## Validate before you publish

Check your pack against the published contract with any standard JSON-Schema validator:

```bash
check-jsonschema --schemafile packs/pack.schema.json packs/your-domain.rulepack.json
```

Open a pull request with your pack (and, ideally, a few example records) — see
[CONTRIBUTING.md](CONTRIBUTING.md).
