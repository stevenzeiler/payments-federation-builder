# AGENTS.md

## Stack
ES6 JavaScript run with `babel-node` (Babel 5). No other runtime dependencies. Dormant since 2015.

## Layout
- `lib/federation_service.js` - `FederationService` base class (package `main`)
- `lib/federation_request.js` - per-lookup request holder
- `test/` - demo scripts, run with `babel-node`; not assertions
- `docs/STATUS.md` - current state

## Commands
- `npm install`
- `node_modules/.bin/babel-node test/federation_service.js`
- `node_modules/.bin/babel-node test/random_subclass.js`
- No working `npm test` yet.

## Rules
- Never commit secrets or credentials.
- Use Conventional Commits (`docs:`, `fix:`, `feat:`).
- Keep `docs/STATUS.md` current when behaviour or state changes.
- Keep sample addresses in tests as public placeholders only.
