# Pilot: measuring the curve directly

## Question and population

Among first-year professional software developers working on unfamiliar existing code, how does access to a coding agent change minutes spent by phase? Use recent graduates or students only as a separately labeled convenience pilot if recruiting employees is not feasible. Analyze onboarding, labor-market demand, and proficiency separately; age is not a substitute for tenure.

## Design

Compare randomized agent access vs. no agent access on matched maintenance tasks in a seeded repository. With a crossover, randomize and counterbalance order and tasks, use disjoint issues, and check for period and carryover effects; a parallel design avoids cross-condition carryover in the main study. Standardize tooling, time caps and documentation access; log agent version and adherence. Both groups receive the same requirements and automated acceptance criteria. Tasks should include an ambiguous requirement, a bug or feature, tests, and a release/monitoring step if Operate is a target. Sample more than one task type. Codebase familiarity, prior experience, and agent literacy are baseline variables.

Record timestamped mutually exclusive **human active** intervals:
- Specify: clarify scope, constraints, or acceptance criteria.
- Design: compare solution structures or decide interfaces.
- Build: implement or edit; prompting an implementation maps here when that is the purpose.
- Verify: inspect behavior, reproduce defects, test, review output, or diagnose root cause. Editing a fix is Build; checking a fix is Verify.
- Operate: release, configure deployments, observe running systems, or respond to incidents.
- Other/unclear: retain rather than force classification. Break and idle are recorded separately.

Ramp is a cross-cutting flag, not a mutually exclusive SDLC phase: e.g., reading docs to understand a dependency can be Verify + Ramp. Agent work and waiting are separate timelines. Background agent runtime can overlap human activity; do not add the timelines to a single denominator. Record coding confidence, independently double-code a sample, report agreement/reconciliation, and preserve a frozen rubric before analyzing conditions.

## Outcomes and analysis

Primary candidate: active human minutes per assigned task by phase, including timed-out tasks; estimate paired or randomized differences and uncertainty by participant. Prespecify handling of missing telemetry and censored tasks. Report absolute minutes and shares, total elapsed time, completion, and blind acceptance scores. A rising share alone can result from shorter Build time even when Verify minutes also fall. Report the denominator and use participant-level resampling or an appropriate repeated-measures model. Treat phase-specific secondary tests with a multiplicity plan. Size the main study from pilot variation, not the illustrative percentages.

Measure skill formation separately with a delayed, unaided transfer task covering bug diagnosis and explanation; include a baseline and a blinded scoring rubric. A second stage could randomize delegation vs. explanation-first agent practices. No intervention should affect hiring or grades. Before recruitment or workplace data collection, seek institutional human-subjects guidance and establish consent, minimum logging, access controls, and retention. Do not collect employer code or real credentials in the pilot.

## Separate current work from historical change

A two-week field diary with random prompts across the workday, including meetings and on-call, can estimate the current workweek mix in participating teams. Pair each response with a de-identified task key where possible. It cannot supply a pre-agent baseline. A historical claim requires comparable pre-adoption diaries or a phased rollout panel, checks of pretrends, stable work and team definitions, and consideration of concurrent hiring and process changes. Do not treat an agent-off session today as a historical reconstruction.
