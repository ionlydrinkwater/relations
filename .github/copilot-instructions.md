# Copilot Instructions

## Project context

This project is a personal tool for keeping track of family and friends,
including important details and birthdays. It is a website-first app intended
to work well on phones. Follow the project decisions in
[PROJECT_PLAN.md](../PROJECT_PLAN.md).

## Working in this repository

- Use SvelteKit and TypeScript. Persist data in PostgreSQL, accessed only from
  server code, with Google sign-in via Auth.js. Scope every query to the
  signed-in user.
- Everything must run locally in Docker containers; keep secrets in untracked
  environment files and never commit them.
- Keep the UI responsive and usable on small phone screens.
- Keep changes focused on the project goals and update related documentation
  when behavior or setup changes.
- Add or update tests for behavior changes and run the relevant checks available
  in the repository.
- Treat personal information with care: collect and expose only what a feature
  needs, and avoid adding real personal data to source, tests, or examples.
- Do not promise backups for data in the local Docker database volume.
