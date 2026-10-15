# Eigent alternative — a company-wide agent system you own, on Kortix

**Kortix is the open-source AI Operating System** — the leading open-source alternative to Claude Cowork and ChatGPT Work. This starter runs the kind of multi-agent work Eigent does on your desktop, for a whole team, from one git repo you control.

Eigent ([eigent-ai/eigent](https://github.com/eigent-ai/eigent)) is a strong open-source Cowork desktop app. It is Apache-2.0 licensed, built on CAMEL-AI, and gives one power user a multi-agent workforce on their own machine — parallel agents, local model support, browser and terminal toolkits. This repo is for the step after that: when the same agents have to work for a team, on shared infrastructure, with a person approving what they change.

## Kortix vs Eigent

| | Eigent | Kortix |
|---|---|---|
| Open source | Yes (Apache-2.0) | **Yes** |
| What it is | Desktop Cowork app | Open-source AI Operating System |
| Agents, skills, memory | Inside the app | **Files in one git repo you own** |
| Where an agent runs | Your machine (local-first) | **Its own cloud computer per session, on its own branch** |
| Review before it acts | App-level | **Per-tool allow / ask / block; every change lands as a change request you merge** |
| Reaches your tools | Browser + terminal toolkits | **3,000+ apps, plus MCP, OpenAPI, GraphQL and raw HTTP — credentials brokered server-side** |
| Models | Model-agnostic | **Any provider, your own keys — per agent, per session, per message** |
| Best when | One person wants a local multi-agent desktop | **A team wants the whole company's agents in one system it owns** |

Kortix takes you past the desktop: the agents, the skills they share, the company memory and every connector are text files in one repo you version and diff, and each session runs on a disposable cloud computer — so thousands run in parallel, isolated from one another, and nothing reaches your default branch until a person reviews the change request.

## What's in this repo

- `kortix.yaml` — the project manifest: connectors, triggers and the machine image.
- `agents/researcher.md` — an example agent in plain markdown.
- `skills/weekly-brief.md` — an example skill the agent reuses.
- `docs/` — setup, the full comparison, and how to move off a desktop tool.

## Quickstart

```bash
# 1 · Install the Kortix CLI
curl -fsSL https://kortix.com/install | bash

# 2 · Scaffold a project from this starter
kortix init

# 3 · Ship it — pushes the repo and brings the whole thing live
kortix ship
```

Prefer zero setup? Sign up at [kortix.com](https://kortix.com), create a project, and start a session — nothing to install.

## Learn more

- [Kortix vs Eigent — the full comparison](https://eigentalternative.com/kortix-vs-eigent)
- [Open-source Eigent alternatives, compared](https://eigentalternative.com/eigent-alternatives)
- [Self-hosting an Eigent alternative: what you actually own](https://eigentalternative.com/self-hosting-eigent-alternative)
- [Eigent pricing vs an open-source system](https://eigentalternative.com/eigent-pricing)
- [Eigent vs OpenHands](https://eigentalternative.com/eigent-vs-openhands)
- [Eigent vs OpenWork](https://eigentalternative.com/eigent-vs-openwork)
- [Eigent vs Manus](https://eigentalternative.com/eigent-vs-manus)
- [Eigent on GitHub: where the repo lives and how to run it](https://eigentalternative.com/eigent-github)

Kortix is the open-source AI Operating System. Self-host for free, or use Kortix Cloud.
