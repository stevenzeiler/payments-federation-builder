# Status

Last reviewed: 2026-11-20 (pass 02 of the GitHub audit; docs only, nothing was run).

## What works
- By reading the code: `FederationService.lookup(name)` chains `getTag()` and `getCurrencies()` and returns a federation response object; subclasses can override both getters.
- `test/` holds two demo scripts that print a response.

## Known broken or unverified
- Not run in this pass; no automated tests (`npm test` is the placeholder).
- Defaults return hard-coded sample data (a fixed tag and a USD issuer address), and `getCurrencies()` logs to the console.
- Uses the global `Promise`, so it needs Node 0.12 or newer, or a polyfill **(inference)**.
- Babel 5 / `babel-node` is long deprecated.
- `package.json` has empty `description` and `author`, and no `repository` field.
- Unmerged work: branch `feature/tag-not-supported` (WIP async lookup and quotes, 2015-05-30).

## Next
1. Decide what to do with `feature/tag-not-supported` (merge, finish or delete).
2. Replace the demo scripts with real tests.
3. Add `repository`, `description` and `author` to `package.json`; decide on a LICENSE file.

## Not yet from the standard
CONTRIBUTING.md, docs/ARCHITECTURE.md, docs/RELEASING.md, docs/decisions/, events/CATALOG.md, CHANGELOG.md, SECURITY.md, LICENSE, .github/.
