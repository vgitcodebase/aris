# Contributing to the Aris Developer Program

The community pack library is what makes this program valuable — every domain someone
packs makes Aris more useful for the next member. Contributions are welcome for:

- **Packs** — new domains, as data (see [PACKS.md](PACKS.md))
- **Connectors** — mappings from a common record source into a pack's `record_schema`,
  expressed as configuration/data
- **Integration examples** — how you call the API from your stack, described as usage

## The one hard rule

**Never contribute source or logic.** This program ships sealed binaries only. CI
rejects any pull request that adds source code, key material, or real customer records.
If a contribution needs runnable logic to work, it doesn't belong here — bring it to
your program contact instead.

## Make a pack contribution

1. Copy an example in [packs/](packs/) and adapt it to your domain.
2. Validate it against the contract:
   `check-jsonschema --schemafile packs/pack.schema.json packs/your-domain.rulepack.json`
3. Use **synthetic** example records only — never real customer data.
4. Open a pull request. CI validates every pack automatically.

## Developer Certificate of Origin (DCO)

Sign off each commit (`git commit -s`) to certify you have the right to contribute it
under this project's terms:

```
Signed-off-by: Your Name <you@example.com>
```

CI verifies sign-off on every commit.

## Good vs out of scope

- **Good:** new packs, connector configs, API usage examples, docs.
- **Out of scope:** anything containing or describing engine logic, or asking for it.
