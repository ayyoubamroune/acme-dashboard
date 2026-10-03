# Next.js Dashboard

A financial dashboard I built with the Next.js App Router. You can log in, browse invoices and customers, and create, edit and delete invoices, all backed by a Postgres database.

Live demo: [acme-dashboard-two.vercel.app](https://acme-dashboard-two.vercel.app/)
To try it out, log in with:

- Email: `user@nextmail.com`
- Password: `123456`

## What it does

- Login with email and password using Auth.js, with dashboard routes protected by middleware
- Create, update and delete invoices through Server Actions (no separate API routes)
- Form validation with Zod, with error messages shown using `useActionState`
- Invoice and customer data read from and written to a Postgres database
- Loading skeletons and error boundaries, using a route group for the dashboard overview
- Responsive layout built with Tailwind CSS

## Stack

- Next.js 14 (App Router) and TypeScript
- Tailwind CSS
- Vercel Postgres
- NextAuth.js / Auth.js
- Zod
- Heroicons

## Running it locally

Clone the repo and move into it:

```bash
git clone https://github.com/your-username/nextjs-dashboard.git
cd nextjs-dashboard
```

Install dependencies (I use pnpm):

```bash
pnpm install
```

Copy the example env file:

```bash
cp .env.example .env
```

Then fill in `.env` with your own Postgres connection details and an `AUTH_SECRET`. You can generate a secret with:

```bash
openssl rand -base64 32
```

Start the dev server:

```bash
pnpm dev
```

The app will be running at [http://localhost:3000](http://localhost:3000).

## Notes

The demo account above is seed data, so feel free to add, edit or delete invoices. Changes may be reset from time to time.

## Author

Ayyoub Amroune
[GitHub](https://github.com/ayyoubamroune)
