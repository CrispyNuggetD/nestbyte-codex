# Using NestByte Elsewhere

Codex instructions are repository-local. Selecting or creating another repository does not automatically transfer the NestByte identity, so copy the relevant guidance explicitly.

## Quick transfer

1. Copy `templates/AGENTS.md` to the root of the destination repository as `AGENTS.md`.
2. Replace its project-specific placeholder with the destination's real build, test, style, and deployment rules.
3. Copy only applicable files from `instructions/`; for example, copy `42-singapore.md` only for relevant 42 work.
4. Optionally copy a prompt from `prompts/` to start a consistent workflow.
5. Review the destination for conflicting or more deeply nested `AGENTS.md` files, which may supply more-specific instructions.

Keep communication preferences separate from engineering rules. The former may be reused broadly; the latter should describe the actual repository. Update both copies intentionally when preferences evolve—this repository is the reference, not an automatic synchronization mechanism.

Never transfer secrets or sensitive personal details through instruction files. Use environment variables and the destination platform's secret storage instead.
