# Fullstack SaaS boilerplate

Typed SaaS foundation with Fastify, tRPC, React 19, Drizzle, and PostgreSQL. The client is a Vite SPA; the server exposes end-to-end typed procedures, Better Auth sessions, and an optional OpenAI-backed chat path over SSE.

## Overview

This repository is the SaaS starter in the [antonkarasbiz](https://github.com/antonkarasbiz) full-stack and AI practice. It is aimed at application products (authenticated workspaces, admin tools, internal AI features) rather than SEO marketing sites.

## Stack

| Layer | Choice |
| --- | --- |
| API | Fastify + tRPC |
| Web | React 19, React Router 7, Tailwind CSS 4, Vite |
| Data | PostgreSQL + Drizzle |
| Auth | Better Auth |
| AI | OpenAI API, SSE chat |
| Monorepo | pnpm workspaces |
| QA | Playwright |

## Capabilities

- End-to-end TypeScript types from server procedures to the client
- Health checks on the HTTP and tRPC surfaces
- Debounced search via a shared hook
- Server-sent events chat without a custom WebSocket server
- Database seed and push workflows
- Impersonation and role-aware admin screens

## Getting started

```bash
# Install pnpm, then:
cp example.env .env
cp client/example.env client/.env

# Create a Postgres database named fsb
pnpm install
pnpm run push
pnpm run seed
pnpm run dev
```

Production:

```bash
pnpm run build
pnpm run start
```

End-to-end tests expect the app to be running:

```bash
pnpm run test
```

## Layout

```text
client/     React application
server/     Fastify + tRPC
packages/   shared Zod schemas and Drizzle kit
tests-e2e/  Playwright
```

## License

MIT. Implementation follows the Fullstack SaaS Boilerplate lineage. Upstream license terms apply. Third-party sponsor marks are not part of this account’s brand.

## Maintainer

[Anton Karas](https://github.com/antonkarasbiz) — full-stack, blockchain, and AI engineering.
