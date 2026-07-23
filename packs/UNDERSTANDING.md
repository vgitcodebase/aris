# Teaching Aris how your people actually talk (pack v1)

The v0 basics (`record_schema`, `vocab`, `compute`, `cite`) already let Aris answer
plain questions about your records. **v1 adds six optional sections** that close the gap
between how a system names things and how a person asks for them. Every one is data you
write about *your* world — nothing about how Aris works, no code.

Add any of these to your pack, bump `"version": "1"`, and validate against
[`pack.schema.json`](pack.schema.json). See [`lending-portfolio.rulepack.json`](lending-portfolio.rulepack.json)
for a worked example that uses all of them.

---

## `aliases` — words that mean a specific value
Your users say "fast food" but the record says industry *Quick Service Restaurants*;
they say "the bank" but the field is a lender. Map the everyday phrase to the value (or a
distinctive part of it) that appears in your data.

```json
"aliases": {
  "product": { "heloc": "line of credit", "mortgage": "mortgage" },
  "status":  { "late": "delinquent", "paid off": "paid" }
}
```
Now *"how many delinquent loans in Texas"* finds them even though the field says something
slightly different.

## `polarity` — idioms for the good end / bad end of a number
"Bleeding money", "the safest loans", "our best earners" — people describe the extremes of
a number without naming the field. Tell Aris which direction, on which field, the idiom
means.

```json
"polarity": [
  { "terms": ["underwater", "riskiest"], "field": "ltv_pct", "direction": "max" },
  { "terms": ["safest", "conservative"], "field": "ltv_pct", "direction": "min" }
]
```
*"which loans are underwater"* → the ones with the highest loan-to-value, worst first.

## `thresholds` — named filters your team uses
Give a name to a cut people ask for constantly — "high-risk", "jumbo", "profitable". Aris
counts and filters the records that meet it, and a follow-up can stack another on top.

```json
"thresholds": {
  "high-risk": { "field": "ltv_pct", "op": ">", "value": 80 },
  "jumbo":     { "field": "principal", "op": ">", "value": 1000000 }
}
```
*"how many high-risk loans"* · then *"just the jumbo ones"*.

## `focus` — which field answers a question word
"Where", "who", and "when" each point at a field. Tell Aris which, and those questions get
a direct answer instead of a whole record.

```json
"focus": { "where": ["city", "state"], "who": ["lender", "borrower"], "when": ["originated"] }
```

## `dates` — relative time
Name the date field and Aris understands *"this year"*, *"last quarter"*, *"in 2025"*.

```json
"record_schema": { "originated": "date", "...": "..." },
"dates": { "field": "originated" }
```

## `out_of_domain` — what your records *can't* answer
List words that mean a question is outside your data — "ceo", "weather", "credit score".
When one shows up, Aris says *"no record"* rather than guessing on a name that happened to
match. Saying "I don't know" honestly is a feature, not a gap.

```json
"out_of_domain": ["ceo", "weather", "forecast", "credit score", "ssn"]
```

---

### It carries a conversation
Once your words are mapped, Aris follows a thread. Ask a question, then a follow-up that
leaves out what's obvious — Aris keeps the earlier scope and swaps only what changed:

```
how many loans in Texas        → 142
just the high-risk ones        → (keeps Texas, adds high-risk)
average rate on those          → (keeps Texas + high-risk, new measure)
what about last year           → (keeps all of it, adds the date)
```

Every answer is grounded in your records and signed — and every follow-up shows what it
carried over, so nothing is hidden.
