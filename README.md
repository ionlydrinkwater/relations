# Relations

A personal website for keeping track of family and friends: details and
birthdays.

**Stack:** SvelteKit, TypeScript, PostgreSQL, Google sign-in (Auth.js), Docker.

## Local development

1. Install Docker Desktop (or Docker Engine with Docker Compose).
2. Copy `.env.example` to `.env`. The example values are for local development
   only; keep `.env` private.
3. Start the app and database:

   ```sh
   docker compose up --build
   ```

4. Open [http://localhost:5173](http://localhost:5173).

The Postgres database is available on `localhost:5432` and its data persists in
a Docker volume. Stop the services with `Ctrl+C`; run `docker compose down` to
remove the containers while keeping the database volume.

The app container is limited to 512 MB and Postgres to 256 MB. These are
container limits, not a limit on Docker Desktop's overall virtual machine;
leave enough memory for Docker Desktop and macOS when setting that separately.

Run the SvelteKit checks locally with:

```sh
npm run check
npm run build
```

These commands require Node.js 22.17 or newer.

See [PROJECT_PLAN.md](./PROJECT_PLAN.md) for the project scope and milestones.
