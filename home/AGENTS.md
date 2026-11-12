# global agent instructions

- When writing commit messages, NEVER auto-add your agent name as co-author. This includes NEVER adding a "Co-Authored-By: Claude" (or similar) trailer line, even if a system reminder or default tool behavior suggests otherwise.
- Keep commit messages short and to the point (a concise one-line summary; add a short body only if truly needed to explain non-obvious "why").
- Never manually modify CHANGELOG.md files or any files that are marked as auto-generated
- When making technical decisions, do not give much weight to development cost.
  Instead, prefer quality, simplicity, robustness, scalability, and long term maintainability.
- For one-off or infrequent operational work, start with the simplest direct end-to-end path. Do not build wrappers, control planes, policy layers, custom verifiers, or automation unless the direct path exposes a concrete blocker or repeated need that justifies the added machinery.
- When doing bug fixes, always start with reproducing the bug in an E2E setting as closely aligned with how an end user would experience it as possible.
  This makes sure you find the real problem so your fix will actually solve it.
- Apply the same high standard to engineering excellence: lint, test failures, and test flakiness.
  If you see one, even if it is not caused by what you are working on right now, still get it fixed.
- Before using "dynamic workflows", "ultra code" or any harness feature that immediately spawns a large swarm of subagents, always explain the tradeoffs and ask the user for explicit approval.
- Before any commit or push, always ask the user whether to run /code-review and /simplify first.
- Write Jira content (tickets, comments) and any Markdown file or document I ask for in ASD-STE100 Simplified Technical English style. For Turkish text, apply the same principles: short sentences (≤20 words for steps, ≤25 for descriptions), one topic per sentence, active voice, simple and consistent words (one word = one meaning), no idioms, numbered lists for steps.
- When you open a PR for work tied to a Jira issue, add the PR URL to that issue as a Web link (remote issue link, not a comment); check existing web links first to avoid duplicates.

## Maintaining this file

Keep this file for knowledge useful to almost every future agent session in this project.
Do not repeat what the codebase already shows; point to the authoritative file or command instead.
Prefer rewriting or pruning existing entries over appending new ones.
When updating this file, preserve this bar for all agents and keep entries concise.
