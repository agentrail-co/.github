# Agentrail

**See how AI agents use your product and where they get stuck.**

When an agent moves from your docs to your API or calls an MCP tool, Agentrail connects the steps your systems record. You can follow what the agent tried, inspect errors and retries, and use that evidence to decide what to fix. Readiness scans help you find problems on your public site, docs, and API before an agent runs into them.

[![agentrail-node on npm](https://img.shields.io/npm/v/agentrail-node?label=agentrail-node)](https://www.npmjs.com/package/agentrail-node)
[![agentrail-python on PyPI](https://img.shields.io/pypi/v/agentrail-python?label=agentrail-python)](https://pypi.org/project/agentrail-python/)
[![agentrail-go reference](https://pkg.go.dev/badge/github.com/agentrail-co/agentrail-go.svg)](https://pkg.go.dev/github.com/agentrail-co/agentrail-go)

[Website](https://www.agentrail.co/) · [Documentation](https://www.agentrail.co/docs) · [Docs for agents (`llms.txt`)](https://www.agentrail.co/docs/llms.txt)

## Get started

- **Run your first scan.** Follow the [quickstart](https://www.agentrail.co/docs/quickstart) to set up a workspace and get your first agent readiness score.
- **Follow real activity.** Start with the [Journeys guide](https://www.agentrail.co/docs/guides/journeys), then instrument the parts of your product you want to observe.
- **Build against the public API.** See the [API reference](https://www.agentrail.co/docs/api-reference/introduction) for readiness scans, leaderboard data, and agent feedback.

## SDKs

Install the SDK for each part of your stack you want to observe. Every SDK sends to the same workspace, and Agentrail links what they record into one journey.

| Where it runs | Package | Install | Guide |
| --- | --- | --- | --- |
| In front of your site (Cloudflare Workers, Vercel, any Fetch API runtime) | [`agentrail-edge`](https://www.npmjs.com/package/agentrail-edge) | `npm install agentrail-edge` | [Install the edge](https://www.agentrail.co/docs/guides/journeys-edge) |
| On your pages | [`agentrail-browser`](https://www.npmjs.com/package/agentrail-browser) | a script tag, or `npm install agentrail-browser` | [Install the browser script](https://www.agentrail.co/docs/guides/journeys-browser) |
| Node.js servers | [`agentrail-node`](https://www.npmjs.com/package/agentrail-node) | `npm install agentrail-node` | [Install the Node SDK](https://www.agentrail.co/docs/guides/journeys-node) |
| Go servers | [`agentrail-go`](https://github.com/agentrail-co/agentrail-go) | `go get github.com/agentrail-co/agentrail-go@latest` | [Install the Go SDK](https://www.agentrail.co/docs/guides/journeys-go) |
| Python servers (FastAPI, Django, Flask, any ASGI or WSGI app) | [`agentrail-python`](https://github.com/agentrail-co/agentrail-python) | `pip install agentrail-python` | [Install the Python SDK](https://www.agentrail.co/docs/guides/journeys-python) |

The Node, Go and Python SDKs offer the same features: incoming and outgoing HTTP, verified identity, milestones, structured logs, MCP calls and workflow tracking. The JavaScript packages live in [agentrail-js](https://github.com/agentrail-co/agentrail-js); [`agentrail-core`](https://www.npmjs.com/package/agentrail-core) holds what they share, for building your own integration.

## CLI for terminals and coding agents

The [Agentrail CLI](https://github.com/agentrail-co/agentrail-cli) gives terminals and coding agents access to the tools available to their workspace role. It is not on npm yet: the `agentrail-cli` package there is a placeholder with no executable. To try the CLI, build it from source with Node.js 24 and pnpm 11.20.0:

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

Found something that could work better? Open an issue in the repository it belongs to: [JavaScript SDKs](https://github.com/agentrail-co/agentrail-js/issues), [Go SDK](https://github.com/agentrail-co/agentrail-go/issues), [Python SDK](https://github.com/agentrail-co/agentrail-python/issues) or [CLI](https://github.com/agentrail-co/agentrail-cli/issues). A minimal reproduction, the package version or commit, and the result you expected are a useful starting point. Pull requests are welcome.
