# Moving a desktop agent setup to a company system

Kortix is the open-source AI Operating System. You do not migrate a desktop agent by copying a database. You describe the work once, as files, and let the platform run it.

## What carries over

- **The agents.** Re-write each desktop agent as one markdown file under `agents/`. What it does, in plain language, plus the tools it may reach.
- **The skills.** Each repeatable procedure becomes a file under `skills/`. These are the same routines, now shared by every agent and every session.
- **The models.** Point `kortix.yaml` at the providers you already use. Kortix is model-agnostic: any provider, your own keys, chosen per agent, per session or per message.

## What changes

- **Where work runs.** Instead of one desktop, each session boots its own isolated cloud computer with the repo and tools already on it.
- **How work lands.** The agent proposes; a change request records exactly what it changed; a person merges. Nothing else reaches the default branch.
- **How tools are reached.** Connectors are wired once in the repo and scoped per agent, with per-tool allow / ask / block rules — down to the arguments of a call.

## A practical order

1. Create the Kortix project and commit `kortix.yaml`.
2. Move the two or three agents you rely on most; leave the long tail until they earn their place.
3. Wire connectors and set an **Ask** rule on anything that sends or spends — the agent stops and waits for a person.
4. Run both setups for a week on your lowest-risk task, and compare the change requests to what the desktop produced.

See the [setup guide](setup.md) to get the project live.
