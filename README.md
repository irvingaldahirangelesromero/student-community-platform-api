For developers:
pnpm dlx wrangler login
________


Packet: pnpm

_____________________
  student-community-platform-api   main   pnpm create cloudflare@latest student-community-platform-api
.../1a06f2e58d6-1924                     |   +1 +
.../1a06f2e58d6-1924                     | Progress: resolved 1, reused 0, downloaded 1, added 1, done
(node:9068) Warning: `--localstorage-file` was provided without a valid path
(Use `node --trace-warnings ...` to show where the warning was created)

──────────────────────────────────────────────────────────────────────────────────────────────────────────
👋 Welcome to create-cloudflare v2.72.5!
🧡 Let's get started.
📊 Cloudflare collects telemetry about your usage of Create-Cloudflare.

Learn more at: https://github.com/cloudflare/workers-sdk/blob/main/packages/create-cloudflare/telemetry.md
──────────────────────────────────────────────────────────────────────────────────────────────────────────

╭ Create an application with Cloudflare Step 1 of 3
│
├ In which directory do you want to create your application?
│ dir ./student-community-platform-api
│
├ What would you like to start with?
│ category Hello World example
│
├ Which template would you like to use?
│ type API starter (OpenAPI compliant)
│
├ Copying template files
│ files copied to project directory
│
├ Installing dependencies
│ installed via `pnpm install`
│
├ Do you want to add an AGENTS.md file to help AI coding tools understand Cloudflare APIs?
│ yes agents
│
╰ Application created

╭ Configuring your application for Cloudflare Step 2 of 3
│
├ Installing wrangler A command line tool for building Cloudflare Workers
│ installed via `pnpm install wrangler --save-dev`
│
├ Selecting workerd compatibility date
│ compatibility date 2026-09-03
│
├ Generating types for your application
│ generated to `./worker-configuration.d.ts` via `pnpm run cf-typegen`
│
├ Installing @types/node
│ installed via pnpm
│
├ You're in an existing git repository. Do you want to use git for version control?
│ yes git
│
╰ Application configured

╭ Deploy with Cloudflare Step 3 of 3
│
├ Do you want to deploy your application?
│ no deploy via `pnpm run deploy`
│
╰ Done

────────────────────────────────────────────────────────────
🎉  SUCCESS  Application created successfully!

💻 Continue Developing
Change directories: cd student-community-platform-api
Deploy: pnpm run deploy

📖 Explore Documentation
https://developers.cloudflare.com/workers

🐛 Report an Issue
https://github.com/cloudflare/workers-sdk/issues/new/choose

💬 Join our Community
https://discord.cloudflare.com
────────────────────────────────────
```
student-community-platform-api
├─ readme.md
└─ student-community-platform-api
   ├─ AGENTS.md
   ├─ package.json
   ├─ pnpm-lock.yaml
   ├─ pnpm-workspace.yaml
   ├─ README.md
   ├─ src
   │  ├─ ...
   │  ├─ index.ts
   │  └─ types.ts
   ├─ tsconfig.json
   ├─ worker-configuration.d.ts
   └─ wrangler.jsonc

```
______________
# Cloudflare Workers OpenAPI 3.1

This is a Cloudflare Worker with OpenAPI 3.1 using [chanfana](https://github.com/cloudflare/chanfana) and [Hono](https://github.com/honojs/hono).

This is an example project made to be used as a quick start into building OpenAPI compliant Workers that generates the
`openapi.json` schema automatically from code and validates the incoming request to the defined parameters or request body.

## Get started

1. Sign up for [Cloudflare Workers](https://workers.dev). The free tier is more than enough for most use cases.
2. Clone this project and install dependencies with `npm install`
3. Run `wrangler login` to login to your Cloudflare account in wrangler
4. Run `wrangler deploy` to publish the API to Cloudflare Workers

## Project structure

1. Your main router is defined in `src/index.ts`.
2. Each endpoint has its own file in `src/endpoints/`.
3. For more information read the [chanfana documentation](https://chanfana.pages.dev/) and [Hono documentation](https://hono.dev/docs).

## Development

1. Run `wrangler dev` to start a local instance of the API.
2. Open `http://localhost:8787/` in your browser to see the Swagger interface where you can try the endpoints.
3. Changes made in the `src/` folder will automatically trigger the server to reload, you only need to refresh the Swagger interface.
