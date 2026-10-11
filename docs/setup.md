# Setup — an Eigent alternative you own

Kortix is the open-source AI Operating System. This is the self-hosted path for a company-wide agent system. It runs on your own infrastructure, with your own model keys, and the whole configuration lives in one git repo.

## 1 · Install the CLI

```bash
curl -fsSL https://kortix.com/install | bash
```

## 2 · Scaffold the project

```bash
kortix init
```

`kortix init` creates `kortix.yaml` plus your `agents/`, `skills/` and runtime config. Every agent, every skill, the company memory and the machine image are files you can read, diff and roll back.

## 3 · Bring it live

```bash
kortix ship
```

This pushes the repo and brings the whole system up in the cloud. Each session then boots its own isolated Linux sandbox with your repo and tools already on it.

## 4 · Start an agent

```bash
kortix sessions new --prompt "Summarize this week's commits and open a change request"
kortix cr ls        # review what an agent proposes — merge to keep it
kortix chat         # talk to a session's agent from your terminal
```

Work reaches the default branch only through a change request you review. Merge is default-deny for agents.

## Self-host or cloud

- **Self-host:** `kortix self-host start` runs one Docker Compose stack on your own box.
- **Cloud:** sign up at [kortix.com](https://kortix.com), create a project and start a session — nothing to install.

Either way the repo is the source of truth. Moving between them is a clone.

## Next

- [Kortix vs Eigent — the full comparison](https://eigentalternative.com/kortix-vs-eigent)
- [What you actually own when you self-host](https://eigentalternative.com/self-hosting-eigent-alternative)
