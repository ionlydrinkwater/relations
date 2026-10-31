# Project Plan

## Purpose

Relations is a personal tool to help someone keep track of family and friends,
remembering important details and birthdays. It will start as a responsive
website.

## Intended users

People who want a simple, private way to organize information about people
important to them.

## Initial goals

1. Keep a browsable list of family members and friends.
2. Let the user save and update useful details for each person.
3. Store birthdays and make upcoming or relevant dates easy to find.
4. Keep the experience straightforward so information is quick to add and
   retrieve.

## Initial scope

The first version should focus on people, their important details, and
birthdays. Features such as interaction history, reminders, sharing, and
external integrations are not part of the initial scope unless the project
direction changes.

## Technology decisions

- **Framework:** SvelteKit.
- **Language:** TypeScript.
- **Persistence:** PostgreSQL, accessed only from SvelteKit server code.
- **Authentication:** Google sign-in using Auth.js. Every query must be scoped
  to the signed-in user, since Postgres access control is enforced in app code.
- **Runtime:** everything runs locally in Docker containers (the SvelteKit app
  and PostgreSQL, for example via Docker Compose). Keep secrets such as Google
  OAuth credentials and database passwords in untracked environment files.
- **Phone experience:** responsive web design. PWA installation and offline
  support are not planned for now.

Local storage is no longer the persistence plan. If it is used at all, it should
only hold non-sensitive UI preferences, since it is browser/device-specific,
can be cleared, and is not encrypted.

## Guiding principles

- Keep the feature set simple and centered on remembering people.
- Respect privacy: minimize personal data and make its handling clear.
- Prefer useful, understandable behavior over unnecessary complexity.

## Open decisions

- Decide which person details are useful to store and which should be optional.
- Decide how birthday information should be displayed or surfaced.
- Choose the Postgres access approach (for example Drizzle or plain SQL) and
  migration tooling.
- Decide how local database backups will be handled, since data lives in a
  Docker volume.
- Decide whether the project will ever be deployed beyond local Docker.

## Suggested milestones

1. **Create the foundation:** scaffold a SvelteKit app with TypeScript and a
   Docker Compose setup for the app and PostgreSQL.
2. **Add Google sign-in:** configure Auth.js with Google and protect routes.
3. **Create the people list:** add, view, edit, and remove a person, stored in
   Postgres and scoped to the signed-in user.
4. **Add details and birthdays:** support the initial person information and
   birthday display.
5. **Review usability and privacy:** validate the core flow on desktop and
   phone-sized screens, document data handling and backups, and test the main
   behaviors.
