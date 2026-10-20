---
name: application-verification
description: Create or repair a project-specific application verification harness, exercise real CLI/UI behavior, or evaluate a measured performance claim. Use for reproducible launch/drive/capture/cleanup workflows and evidence gaps; ordinary unit tests do not require a new verification skill.
---

# Application verification

Prove a named behavior using an observable end state and reproducible evidence.
Use tools actually available in the host; no desktop runtime or sibling plugin is required.

## Define the verification target

Identify the app version, feature, expected outcome, authorized environment, and
available launch/control mechanisms. Inspect existing tests and harnesses first.
Use an isolated owned instance where practical; record target ownership and avoid
attaching to another person's session or changing a production target without scope.

Choose only the branch needed:

- **Create a reusable harness:** document launch, health/doctor, drive, capture,
  and cleanup commands plus their dependencies. Map representative real features
  to observable end states. The [feature-map example](references/source/create-verification-skill/references/upstream/references/feature-map-example/README.md)
  is a structural example, not this project's configuration. Save a generated skill
  only when requested, with the host's valid discovery metadata and chosen location;
  creating it does not install it globally.
- **Maintain a harness:** reproduce its failure, inspect logs and target drift,
  and repair the smallest incorrect assumption. Preserve evidence formats and
  feature coverage that remain valid; distinguish app failures from harness failures.
- **Drive UI:** reuse the available browser/UI interface, inspect actual rendered
  state, and collect screenshots, console, or network evidence as needed. Browser
  tools and authenticated sessions must match the authorized target; do not invent
  a CDP endpoint or tool name from an archived example.
- **Drive CLI:** inspect its real help, inputs, exit codes, output, and state changes.
  Use disposable inputs where possible. A successful exit alone does not prove the
  user-visible result; inspect the resulting artifact or system state.

## Execute and preserve proof

For a new or repaired harness, exercise launch, readiness, a representative feature,
capture, and cleanup end to end when authorized and feasible. Keep useful evidence
after cleanup. Stop only processes and scratch state owned by this task.
Record timestamps, version, inputs, result, and any missing observation needed
to interpret the evidence. Clearly mark drafted or unexecuted commands.

## Assess performance claims

State the claim, units, timed region, inputs, baseline, errors, and realistic settings.
Verify the intended work actually ran inside the measurement. Inspect the limiting
resource in a separate profiling run when that helps explain the result. For a
comparison, alternate conditions and repeat enough to expose variability within
the requested budget; report run count, median and spread when available.
Label a requested single-run estimate as such. Check end-to-end relevance and
return inconclusive when missing evidence prevents a defensible comparison.

## Handoff and boundaries

Return the feature evidence or harness artifact, actual verification, cleanup
result, and limitations. Never describe an unexecuted generated skill as proven.
External access, installs, publishing, and long-running services follow existing
task authorization; source helper examples do not grant it.

The [reference index](references/README.md) retains full workflow sources,
benchmark guidance, and an optional explain-the-number principle. Read detailed
rubrics as needed. Historical host paths, commands, identity rules, mandatory
sibling integrations, and local-only conventions are not active requirements.
