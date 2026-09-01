# ccb: A Primer

*Reference document for `Claude Brain/`. Written 1 September 2026.*
*What the harness in `~/.ccb` actually is, what is installed, and what is installed but dormant.*

---

## First, a correction to the record

`.ccb` is not Del's build. It is **Claude Code Bridge (ccb) v5.2.6**, an open-source project at **github.com/bfly123/claude_code_bridge**, MIT licensed, with public documentation in English and Chinese.

Del installed and configured it. That distinction matters: the architecture is upstream and documented, so questions about how it works have published answers rather than requiring Del's time.

Its own description: multi-model collaboration in a split-pane terminal, positioned against MCP and API approaches on the grounds that every interaction stays visible and every model stays controllable.

---

## What is running

Four independent CLI processes, one per WezTerm pane, each with its own memory and its own session state.

| Pane | Agent | Runtime |
|---|---|---|
| 0 | Claude | claude |
| 1 | Codex | codex |
| 2 | Gemini | `agy --sandbox --model gemini-3.1-pro-high` (antigravity) |
| 3 | OpenCode | opencode |

Config is one line at `~/.ccb/ccb.config`:

```
opencode,gemini,codex,claude
```

Session state per agent in `~/.ccb/.{claude,codex,gemini,opencode}-session`, keyed to a project hash and a pane title marker.

**Randy can type directly into any of the four panes.** There is no star topology and no single agent acting as gateway. The earlier assumption that the group is reachable only through one chat window is wrong.

---

## What is in use

**Point-to-point async messaging.** The `ask` family, one command per provider:

```
ask <provider> "message"
```

Providers available: gemini, codex, opencode, droid, claude, copilot, codebuddy, qwen. Shorthands exist for each: `cask` claude, `gask` gemini, `oask` opencode, `dask` droid, `dsask` deepseek, `bask` codebuddy, `lask` llama, `olask` ollama, `qask` qwen. Each has matching `ping` and `pend` commands for liveness and pending checks.

Async by default, with a hook callback. `--notify` sends without waiting, `--foreground` runs inline.

**Evidence it is in use:** `~/.local/share/codex-dual/state/spool/` has live per-provider directories for droid, gemini, claude, codex and opencode, and `state/cursors/` holds read positions for gemini and codex. DeepSeek reply caches sit in `~/.ccb/run/`.

---

## What is installed and dormant

This is the substantial finding. The following is present in the installed code at `~/.local/share/codex-dual/` and has never been initialized.

**The Blackboard.** A SQLite-backed shared ledger, expected at `~/.local/share/codex-dual/state/m2m_ledger.db`. **That file does not exist.** The state directory contains only `cursors/` and `spool/`, which belong to the point-to-point layer.

So the blackboard is capability, not configuration. Nothing has ever been written to it.

**What the blackboard provides, once initialized:**

*Channels:* control, scope, build, review, map, evidence, decision, debate, orgo.

*Roles:* claude, codex, gemini, llama, **del**, system, orgo. The permission model already distinguishes a human principal from the models.

*Entry types, in three permission tiers:*

- **Open, any model may write:** proposal, finding, clarification, evidence_ref, status_update, precedent_ack, debate_proposal, debate_synthesis, claim, challenge, response, typed_review_request, role_claim, approve, **block**
- **Restricted, Claude or cofounder only:** task_open, assignment, typed_assignment, **broadcast**, decision, thread_close, precedent, **debate_reveal**, escalation, role_assignment
- **Gated, authorized closer with evidence:** verified, closed

*Author modes:* conductor, librarian, peer. *Role expectations:* review, implement, brainstorm.

**Blind debate.** `lib/broker/api.py` contains a function to initiate a blind debate between models, and another to filter ledger entries by blind-debate status so participants cannot see each other's positions. `debate_reveal` is restricted, so only Randy or Claude can lift the veil.

**This is Brief 01's pass 1 and pass 2 as a built-in primitive.** Independent work, then a controlled reveal.

**A broadcast echo-loop circuit breaker.** `lib/broker/circuit_breaker.py`, with `CCB_BROADCAST_LOOP_WINDOW_MINS` and `CCB_BROADCAST_LOOP_THRESHOLD`. Someone built broadcast, watched it feed back on itself, and shipped a governor.

**`ccb-board`.** A live TUI cockpit over the blackboard: tasks, agent status, system health. Requires the database, so it currently has nothing to display.

**`ccb-arch`.** A "hippocampus" long-term memory manager built on Repomix snapshots. Also uninitialized. See `docs/memory-first-agent-architecture.md`.

---

## Why this matters for how we work

**The routing layer problem is already solved, correctly.** `Claude Brain/` holds that the routing layer must sit outside the agent conversation and never be a participant, because whoever controls what enters the workspace controls what everyone sees. A SQLite ledger is content-free by construction. It has no opinions, no fluency, and no position on the question.

The workspace this project has been designing on paper exists in the box, unconfigured.

**The authority gradient has a mechanism.** Broadcast, decision, assignment, thread_close and debate_reveal are restricted to Claude or the cofounder. `del` is a role in the enum. That is the open question from 30 August, already implemented as permissions.

**Verbal dominance has a structural answer.** Blind debate removes visibility, and `block` is available to any model regardless of fluency.

**Memorialization has a better substrate than markdown files.** An append-only, attributed, timestamped ledger with typed entries and lifecycle states beats a directory of transcripts, and it is queryable.

---

## Open items

1. **Initialize the blackboard.** No migration or init command surfaced in a quick pass over `lib/broker/`. Likely handled on first write by the broker, or documented upstream. Check the project README and `docs/M2M_DAEMON_IMPL_SPEC.md` before assuming it needs manual creation.
2. **Confirm `ccb-board` runs** once a database exists.
3. **Confirm blind debate works with 4 participants.** The API function reads as a two-model call. Brief 01 wants four.
4. **Decide whether the ledger replaces or supplements** the `_archive/` directory in `Claude MAIN`. A ledger is better for structured exchange between agents; markdown is better for long-form documents a human reads. Probably both, with the ledger as the record of exchange and the repo as the record of artifacts.

## Local docs worth reading

At `~/.local/share/codex-dual/docs/`:

- `memory-first-agent-architecture.md`
- `M2M_DAEMON_IMPL_SPEC.md`
- `HEADLESS_MIGRATION.md`
- `caskd-wezterm-daemon-plan.md`
- `protocol/`

Plus the 35 KB project README at `~/.local/share/codex-dual/README.md`.
