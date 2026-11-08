# Agentrail

**See how AI agents use your product and where they get stuck.**

When an agent moves from your docs to your API or calls an MCP tool, Agentrail connects the steps your systems record. You can follow what the agent tried, inspect errors and retries, and use that evidence to decide what to fix. Readiness scans help you find problems on your public site, docs, and API before an agent runs into them.

[![Docs: Quickstart](https://img.shields.io/badge/Docs-Quickstart-2563eb)](https://www.agentrail.co/docs/quickstart)
[![Node SDK version on npm](https://img.shields.io/npm/v/agentrail-node?label=Node%20SDK)](https://registry.npmjs.org/agentrail-node)
[![CLI: Source](https://img.shields.io/badge/CLI-Source-475569?logo=github)](https://github.com/agentrail-co/agentrail-cli)

[Website](https://www.agentrail.co/) · [Documentation](https://www.agentrail.co/docs) · [Docs for agents (`llms.txt`)](https://www.agentrail.co/docs/llms.txt)

## Get started

- **Run your first scan.** Follow the [quickstart](https://www.agentrail.co/docs/quickstart) to set up a workspace and get your first agent readiness score.
- **Follow real activity.** Start with the [Journeys guide](https://www.agentrail.co/docs/guides/journeys), then instrument the parts of your product you want to observe.
- **Build against the public API.** See the [API reference](https://www.agentrail.co/docs/api-reference/introduction) for readiness scans, leaderboard data, and agent feedback.

## JavaScript SDKs

Pick the package for the part of your stack you want to instrument. The packages live in [agentrail-js](https://github.com/agentrail-co/agentrail-js), ship together, and require Node.js 22 or newer for npm installs.

| npm package | Use it to | Install |
| --- | --- | --- |
| [`agentrail-edge`](https://registry.npmjs.org/agentrail-edge) | [Record requests at the edge](https://www.agentrail.co/docs/guides/journeys-edge), including requests from agents that never run JavaScript. | `npm install agentrail-edge` |
| [`agentrail-browser`](https://registry.npmjs.org/agentrail-browser) | [Record page views, calls to your own services, and WebMCP tool calls](https://www.agentrail.co/docs/guides/journeys-browser). Use npm if you bundle the browser script yourself. | `npm install agentrail-browser` |
| [`agentrail-node`](https://registry.npmjs.org/agentrail-node) | [Capture backend HTTP traces, structured logs, and MCP calls](https://github.com/agentrail-co/agentrail-js/tree/main/packages/node) from Node.js services. | `npm install agentrail-node` |
| [`agentrail-core`](https://registry.npmjs.org/agentrail-core) | Use shared event types, trace context, and the collector client when building your own integration. | `npm install agentrail-core` |

## CLI for terminals and coding agents

The [Agentrail CLI](https://github.com/agentrail-co/agentrail-cli) gives terminals and coding agents access to the tools available to their workspace role. The [`agentrail-cli` npm entry](https://registry.npmjs.org/agentrail-cli) is a placeholder with no executable. To try the CLI, build it from source with Node.js 24 and pnpm 11.20.0:

```sh
git clone --depth 1 https://github.com/agentrail-co/agentrail-cli.git
cd agentrail-cli
pnpm install --frozen-lockfile
pnpm build
node dist/cli.js --help
```

If you're working with a coding agent, the [Agentrail skill](https://github.com/agentrail-co/agentrail-cli/blob/main/skills/agentrail/SKILL.md) walks through readiness scans, simulations, and feedback.

## Explore and contribute

Need an app to experiment with? Start with the [Next.js starter](https://github.com/agentrail-co/starter-nextjs), or try a fuller example: [Kanbo](https://github.com/agentrail-co/kanbo-nextjs) for task boards, [Shelfwise](https://github.com/agentrail-co/shelfwise-nextjs) for a bookshop, or [Tally](https://github.com/agentrail-co/tally-nextjs) for invoicing.

Found something that could work better? Open an issue in the [SDK](https://github.com/agentrail-co/agentrail-js/issues) or [CLI](https://github.com/agentrail-co/agentrail-cli/issues) repo. A minimal reproduction, the package version or commit, and the result you expected are a useful starting point. Pull requests are welcome.
