> Archived source reference, repackaged by Leotus-Richard on 2026-10-20. This is not an active skill or execution policy. Use the domain hub for current task scope and available capabilities; host commands, integrations, local-only rules, identity rules, and publishing steps below are historical examples. Modifications: discovery filename and local links normalized where needed, machine paths replaced where present; source substance retained.

---
name: control-ui
description: "Drive an owned local UI with an existing browser/CDP harness; no remote or personal authenticated browser session."
metadata:
  version: "1.0.0"
  profile: "local-task-toolkit"
  invocation: "task-specific"
  integration-status: "portable-instructions-host-untested"
---

# Control Ui

## Scope

Read `references/local-execution-contract.md` at task start. This skill is task-specific and local-only. Do not activate remote integrations, persistent modes, hooks or unrelated implementation.

## Workflow

1. Reuse an existing local verification harness. Start only an owned isolated local app instance.
2. Drive the actual UI feature, inspect state/console/network as needed and capture fresh evidence.
3. Keep ports, profiles and data dirs isolated; do not attach to another user session.
4. Clean up only the processes and scratch state you created while retaining proof.

## Default output

Local UI behavior evidence, instance ownership and cleanup result.

## Failure boundary

Report the missing input or capability; do not fabricate evidence or broaden the task.

## Upstream resources

The full original skill and its resources are preserved under `references/upstream/`. Read `references/upstream/ORIGINAL-SKILL.md` for detailed rubrics, templates and examples when its branch is relevant. Resolve its relative resource paths from that directory. Its tool names, model IDs, publication steps, transcript paths and persistent modes are source-specific examples, not permission to execute them. Follow this hub and the local execution contract when those instructions conflict.

## Provenance

Adapted from [cursor-team-kit:control-ui](https://github.com/cursor/plugins/blob/1e5c90a4b6f249917bd21fe361b3a2a7deb741b8/cursor-team-kit/skills/control-ui/SKILL.md). The original MIT notice is bundled. This is a local-only adaptation, not an endorsement or a claim of native host support.
