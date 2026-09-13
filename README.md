# NestByte

NestByte is Christopher's central workspace for building, organizing, and showcasing projects made with Codex. It also defines a portable working style for NestByte: thoughtful and supportive in conversation, technically rigorous in implementation, candid about uncertainty, and willing to challenge incorrect assumptions.

> [!WARNING]
> **This repository is public so that its GitHub Pages site can be published. Treat every file, commit, branch, pull request, issue, Actions log, and the repository's Git history as publicly visible.**
>
> Never commit plaintext health or medication data, Apple Health exports or screenshots, passphrases, API keys, credentials, personal identifiers, or other sensitive information. The medication dashboard may contain only encrypted data. Remember that deleting a secret in a later commit does not remove it from Git history; if one is committed accidentally, rotate/revoke it and clean the history promptly.

## Live websites

- [NestByte projects](https://crispynuggetd.github.io/nestbyte-codex/)
- [Family Medication Dashboard](https://crispynuggetd.github.io/nestbyte-codex/medication-dashboard/)

Personality guidance is intentionally brief. Project-specific engineering requirements belong with the project they govern so that friendliness never displaces correctness.

## Repository layout

```text
.
├── AGENTS.md                  # Instructions active throughout this repository
├── USAGE.md                   # How to reuse NestByte in another repository
├── instructions/             # Reusable, topic-specific guidance
│   └── 42-singapore.md
├── prompts/                  # Reusable prompts for common workflows
│   └── start-project.md
├── templates/                # Files intended to be copied elsewhere
│   └── AGENTS.md
└── projects/                 # Optional home for self-contained projects
```

## One repository or many?

This repository can be a **monorepo**: one GitHub repository containing many projects under `projects/`. That is a good fit when you want one link, shared conventions, and simple administration. Each project should still have its own directory, README, dependency files, tests, and deployment configuration.

For example:

```text
projects/
├── family-photo-map/
├── recipe-planner/
└── portfolio-site/
```

A separate repository becomes useful only when a project needs independent collaborators, permissions, issue tracking, release history, or deployment settings. Projects can be split out later without changing the NestByte identity files.

## Showing websites online

GitHub stores the source; a deployment service makes a web project visitable. Static sites can be published from this monorepo using GitHub Pages or another static host. Applications with a server component need an application host or a publicly reachable server.

A practical progression is:

1. Keep small projects together under `projects/`.
2. Add a landing page that links to every deployed project.
3. Deploy static projects with a managed service first.
4. Use a private home server for development, previews, and intranet tools.
5. Add a reverse proxy, domain, TLS, monitoring, and deliberate network isolation before exposing self-hosted services publicly.

WireGuard is excellent for private access, but it does not by itself publish a site for family and friends. Until public hosting is configured safely, a managed static or application host is the simplest route to shareable links.

## Adding a project

Create `projects/<project-name>/`, add a project README with its purpose and commands, and place a project-specific `AGENTS.md` there when its rules differ from the repository defaults. Start from [`prompts/start-project.md`](prompts/start-project.md) when asking Codex to scaffold it.

Do not commit secrets. Store deployment credentials in the selected host's secret manager or GitHub Actions secrets, and commit only documented environment-variable names in an example file such as `.env.example`.
