# This is an opionated boilerplate that I use to build app quick and fast.

This boilerplate combine **React Router v7**, **Hono**, **Cloudflare**, **Worklow**, **Durable Object**, **R2**.
The project is structured has a **monorepo**.You will find apps continaing the docs your are reading and the web. We have 4 packages.The fist one is the db which provide the api to query your database with **dirzzle ORM**. The second one is **shared** package containing all the assets, config, constants, hooks and types that can be shared accros frontend. The third one is **tsconfig**, it contain the base config that we will be using in other packages or apps to avoid repetition. And the last one is  **utils**, it contain all the utilities that we will be using in the app. 

## Main libs

- 📦 pnpm – Monorepo package manager
- 🎨 Tailwind CSS v4 – Utility-first CSS framework
- 🧩 shadcn/UI – Component library
- 🔍 BiomeJS – Code formatting and linting
- ⚡ Vite.js – Build tool
- 🪝 Lefthook – Git hooks manager
- 🔧 Wrangler – Cloudflare development CLI
- 🗃️ Drizzle ORM – SQL-first ORM
- 🌩️ Cloudflare D1 (Default) – SQLite database for Cloudflare Workers
- 🔐 Better Auth – Comprehensive authentication

## Project Structure

```
react-router-v7-hono-cloudflare-boilerplate/
├── apps/                      # Application directory
│   ├── web/                   # Main Web application
│   │   ├── app/               # Application source code
│   │   │   ├── routes/        # Route definitions
│   │   │   └── styles/        # Style files
│   │   ├── public/            # Static assets
│   │   ├── workers/           # Cloudflare workers
│   │   └── ...                # App configs & scripts
│   └── service/               # Backend or middleware services
│       ├── durable-objects/   # Cloudflare Durable Objects
│       ├── hono/              # Hono framework-based services
│       └── workflows/         # Background jobs or orchestrations
├── packages/              # Shared packages
│   ├── db/                # Drizzle ORM + Cloudflare D1 database
│   ├── shared/            # Common utilities, hooks, and assets
│   ├── ui/                # shadcn/ui-based reusable UI components
│   └── tsconfig/          # Centralized TypeScript config presets
├── .cursor/               # Cursor editor config & code style rules
├── .github/               # GitHub workflow config
├── biome.json             # BiomeJS config
├── lefthook.yml           # Lefthook Git hooks config
├── commitlint.config.cjs  # Commit message linting config
├── tsconfig.json          # Root TypeScript config
├── pnpm-workspace.yaml    # pnpm workspace config
└── ...                    # Other root config files
```

## Root Configuration Files

- **biome.json**: Code formatting and linting rules (BiomeJS)
- **lefthook.yml**: Git hooks for pre-commit (format, lint, typecheck) and commit-msg (commitlint)
- **commitlint.config.cjs**: Conventional commit message enforcement
- **tsconfig.json**: Extends centralized TypeScript config from `packages/tsconfig`
- **pnpm-workspace.yaml**: Declares workspace packages in `apps/*` and `packages/*`
