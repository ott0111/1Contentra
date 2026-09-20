# Contentra

The Operating System for Creators. A functional growth workspace for creators, businesses, personal brands, and agencies.

## Stack

- Next.js App Router
- React
- Prisma ORM
- PostgreSQL
- Vercel
- TypeScript

## Local development

1. Install dependencies: `pnpm install`
2. Copy `.env.example` to `.env.local` and set `DATABASE_URL`.
3. Generate Prisma Client: `pnpm db:generate`
4. Validate the schema: `pnpm db:validate`
5. Run the app: `pnpm dev`

## Vercel

- Framework: Next.js
- Root Directory: `./`
- Install Command: `pnpm install`
- Build Command: `pnpm build`
- Production Branch: `main`
- Node.js: 22.x

Required environment variable: `DATABASE_URL`.

Also configure `NEXT_PUBLIC_APP_URL`, `NEXT_PUBLIC_API_URL`, and `SESSION_COOKIE_NAME`.

Add provider/API secrets only when those integrations are enabled.

## Database deployment

Use `pnpm db:deploy` for an existing Prisma migration set. Use `pnpm db:migrate` for local schema development.

Do not commit `.env.local` or production secrets.
