# Copilot Instructions

Personal, website-first app for tracking family and friends (details and
birthdays), usable on phones. See [PROJECT_PLAN.md](../PROJECT_PLAN.md).

- Use SvelteKit and TypeScript; keep the UI responsive on small screens.
- Use PostgreSQL from server code only, with Google sign-in via Auth.js.
  Scope every query to the signed-in user.
- Everything runs locally in Docker; never commit secrets.
- Keep changes focused, update related docs, and add or run tests for behavior
  changes.
- Treat personal data with care: collect only what's needed and use no real
  personal data in source, tests, or examples.
