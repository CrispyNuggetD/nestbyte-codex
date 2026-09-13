# Reusable Project-Starting Prompt

Copy this prompt into a new Codex task and replace the bracketed fields.

```text
Create a self-contained project at projects/[project-name].

Goal: [what the project should accomplish]
Audience: [who will use it]
Technology constraints: [language, framework, hosting, or "recommend an appropriate stack"]
First milestone: [smallest useful version]

Before coding:
1. Read the repository AGENTS.md and relevant files under instructions/.
2. Identify unclear requirements and state any reasonable assumptions.
3. Propose a compact implementation and deployment plan.

During implementation, keep all project-specific code, tests, configuration, and documentation inside the project directory. Add a README with setup, development, testing, and deployment commands. Do not add secrets; use documented environment variables and an .env.example when needed. Run appropriate checks, review the resulting diff, and summarize decisions and follow-up improvements.
```
