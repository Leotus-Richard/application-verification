> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

---
name: control-cli
description: "Drive an owned local CLI/TUI using repeatable input and captured output."
metadata:
  version: "1.0.0"
  profile: "local-task-toolkit"
  invocation: "task-specific"
  integration-status: "portable-instructions-host-untested"
---

# Control Cli

## Scope

Read `references/local-execution-contract.md` at task start. This skill is task-specific and local-only. Do not activate remote integrations, persistent modes, hooks or unrelated implementation.

## Workflow

1. Reuse the project test/demo harness or a small local PTY/tmux harness.
2. Provide deterministic input and observe the exact user-facing output/state.
3. On a hang, capture evidence before interrupting the owned process.
4. Clean up only owned sessions and retain the reproduction/proof artifact.

## Default output

Repeatable CLI check, observed output and cleanup result.

## Failure boundary

Report the missing input or capability; do not fabricate evidence or broaden the task.

## Upstream resources

The full original skill and its resources are preserved under `references/upstream/`. Read `references/upstream/ORIGINAL-SKILL.md` for detailed rubrics, templates and examples when its branch is relevant. Resolve its relative resource paths from that directory. Its tool names, model IDs, publication steps, transcript paths and persistent modes are source-specific examples, not permission to execute them. Follow this hub and the local execution contract when those instructions conflict.

## Provenance

Adapted from [cursor-team-kit:control-cli](https://github.com/cursor/plugins/blob/1e5c90a4b6f249917bd21fe361b3a2a7deb741b8/cursor-team-kit/skills/control-cli/SKILL.md). The original MIT notice is bundled. This is a local-only adaptation, not an endorsement or a claim of native host support.
