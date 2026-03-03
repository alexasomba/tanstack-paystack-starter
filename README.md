# TanStack Paystack Starter 🚀

A production-ready SaaS starter template featuring **TanStack Start**, **Better Auth**, and **Paystack** integration. Built to be deployed on **Cloudflare Workers**.

[**Live Demo**](https://better-auth-paystack.gittech.workers.dev)

## Features

- 🔐 **Authentication**: Powered by [Better Auth](https://www.better-auth.com/)
- 💳 **Payments**: Subscription & one-time payment flows via [@alexasomba/better-auth-paystack](https://github.com/alexasomba/better-auth-paystack)
- 🏢 **Organization Billing**: Managed subscriptions for teams/organizations
- ⚡ **Framework**: [TanStack Start](https://tanstack.com/start) (Full-stack React)
- 🌥️ **Deployment**: Optimized for [Cloudflare Workers](https://workers.cloudflare.com/)
- 🎨 **UI**: Tailwind CSS + Shadcn UI + Phosphor Icons
- 📦 **Database**: SQLite via Drizzle ORM

## Quick Start

### 1. Use this Template

Click the green **"Use this template"** button above to create a new repository from this starter.

### 2. Clone and Install

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
pnpm install
```

### 3. Configure Environment

Copy the example environment file:

```bash
cp .dev.vars.example .dev.vars
```

Fill in your keys in `.dev.vars`:

- `PAYSTACK_SECRET_KEY`: From your [Paystack Dashboard](https://dashboard.paystack.com/#/settings/developer)
- `BETTER_AUTH_SECRET`: Generate a random string (e.g., `openssl rand -base64 32`)

### 4. Development

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Project Structure

```text
src/
├── lib/
│   ├── auth.ts          # Better Auth + Paystack plugin config
│   └── auth-client.ts   # Client-side auth with Paystack client
├── routes/
│   ├── __root.tsx       # Root layout
│   ├── index.tsx        # Landing page
│   ├── dashboard.tsx    # Protected dashboard
│   └── billing/
│       └── paystack/
│           └── callback # Paystack redirect callback
└── components/          # UI components
```

## Deployment

Deploy to Cloudflare Workers with one command:

```bash
pnpm deploy
```

Make sure to set your production environment variables in the Cloudflare Dashboard or via `wrangler secret put`.

## License

MIT © [Alex Asomba](https://github.com/alexasomba)
