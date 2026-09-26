# Sufler: an internal assistant for one team's tools

**Where:** BIAP, Intelligent Technologies division · **Role:** Intern · **When:** July to September 2026
**Status:** deployed as a pilot in one team. **Code:** [P0w3r223/sufler](https://github.com/P0w3r223/sufler),
a copy published with the company's consent, with personal data and company infrastructure removed.

## The problem

One team worked across Claude Code, Microsoft Teams, GitHub and Jira with no shared memory. Meeting
notes and project status sat in separate files, and a question that touched two systems meant
leaving the conversation to look it up.

Most of the work went into one question: when may an agent that reads untrusted text (issue
comments, transcripts, documents) write a note, a GitHub issue or a Teams message?

## What I built

- **One core, several entry points.** All logic lives in one core with no I/O. Claude Code (through
  MCP), Teams, a command-line client and GitHub are thin adapters over the same tool catalogue, so a
  new tool is written once. The rule that the core never imports an adapter is checked by
  import-linter in CI.
- **A bridge between GitHub and Teams.** GitHub events (issues, pull requests, reviews, CI) go into an
  append-only event store with deduplication; a notifier posts them to a channel or a 1:1 chat, and
  a reply in Teams can open an issue or answer in the GitHub thread, behind a write gate.
- **Read-only Jira.** "What are my open tasks" is answered in the conversation. There is no write path
  to Jira in the code, and the Jira account is never chosen by the model.
- **Meeting notes from transcripts.** The agent turns a Teams meeting transcript into a structured
  note; participants are counted from the transcript, not by the model.

## What did not work (yet)

- **Adoption.** On 2026-09-07 the pilot had seen 4 user turns in the 17 days since the demo, 64 tool
  calls in total, and 2 people had used it. The team has not yet made it part of daily work.
- **The HTTP deployment on the company server** is still open.
- **Dense retrieval** is built and switched off until it passes a small evaluation threshold; search
  runs on BM25 over Polish lemmas.

## Details

<details>
<summary><strong>Safety model</strong></summary>

- Every capability that writes is off by default and has to be opened by the operator. A test
  discovers the gates by reflection and checks the configuration templates as well.
- Editing a note goes through an independent judge model, a snapshot before the change, and a human
  confirmation step. Deletion has its own gate and is closed in the pilot deployment.
- Shell commands from the model run in a separate container with no network, created per
  conversation and able to see only that conversation's scratch space.
- The MCP tool surface is frozen: 5 tools plus 3 that appear only under specific configuration,
  held by a golden test. Adding a tool breaks that test and needs a decision record first.
- Tool descriptions have byte ceilings (2048 B per tool, 8000 B in total), so the agent's context
  cost cannot grow unnoticed.

</details>

<details>
<summary><strong>By the numbers</strong></summary>

| | |
|---|---|
| Decision records | 75 |
| Test files | 209, including a security suite (injection, path traversal, secret leakage) |
| Agent tools | 8 with the shell enabled, 14 without it |
| Commits | 652 on the main branch |
| Monorepo migration | four sub-projects under one CI matrix; one imported with its full 36-commit history |

</details>

<details>
<summary><strong>Deployment</strong></summary>

The service ships as a base image delivered as a `docker save` archive, so it cannot be pinned
by registry digest. The deployment package I wrote layers fixes over that image as checksum-gated
patches: if an upstream bump touches a patched line, the build fails instead of silently dropping the
fix. It also backs up the SQLite state volumes through a helper container, because a plain copy can
lose the write-ahead log. An archived smoke run passed 17 of 17 checks.

</details>
