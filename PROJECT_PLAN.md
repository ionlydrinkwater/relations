# Project Plan

## Purpose

A personal tool to keep track of family and friends: important details and
birthdays. Website-first, responsive for phones.

## Stack

- SvelteKit + TypeScript
- PostgreSQL, accessed from server code only
- Google sign-in via Auth.js; scope every query to the signed-in user
- Everything runs locally in Docker; secrets stay in untracked env files
- Responsive website; no PWA for now

## Scope

People, their details, and birthdays. No reminders, history, or sharing yet.

## Open decisions

- Person fields to store
- How birthdays are surfaced
- Postgres access (Drizzle or plain SQL) and migrations
- Backups for the Docker volume

## Milestones

1. Scaffold SvelteKit + Docker Compose with Postgres
2. Google sign-in
3. People list (add, view, edit, remove)
4. Details and birthdays
5. Phone usability, privacy review, tests
