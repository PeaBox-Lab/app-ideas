# Cron Observatory

> **Idea #76** · **Category:** DevOps & Cloud · **Tier:** Advanced · **Estimated MVP effort:** 2–3 wk

## One-line pitch

Track job executions, output, heartbeats, missed schedules, and failure notifications in one dashboard.

## Problem

Scheduled jobs commonly lack centralized visibility into missed runs, duration, and failures.

## Target users

- **Primary user:** the developer, operator, analyst, or knowledge worker who directly performs this workflow.
- **Secondary user:** a maintainer or team lead who needs repeatability, visibility, and safer hand-offs.
- **Early adopter:** someone already solving the problem with scripts, spreadsheets, manual checklists, or disconnected tools.

## Product thesis and differentiation

Track job executions, output, heartbeats, missed schedules, and failure notifications in one dashboard.

The product should stay deliberately focused: explain what happened, preserve user control, and make the result reproducible. It should not become a broad platform before the core workflow is proven.

## MVP user stories

1. **Story:** As a primary user, I want to complete the core Cron Observatory workflow from one documented interface, so that I replace a fragile manual process.
   - **Acceptance criteria:** Given representative sample input, when the workflow runs, then the expected output is produced with a traceable result.
2. **Story:** As a new user, I want configuration to be validated before execution, so that setup failures are understandable.
   - **Acceptance criteria:** Invalid or missing settings identify the affected field, accepted format, and corrective action; secrets are never echoed.
3. **Story:** As a cautious user, I want a preview or dry run before risky changes, so that I can review impact.
   - **Acceptance criteria:** Preview mode performs no destructive writes and clearly distinguishes planned actions from completed actions.
4. **Story:** As an operator, I want machine-readable and human-readable results, so that I can use the tool interactively and in automation.
   - **Acceptance criteria:** The same run can emit JSON plus Markdown, HTML, terminal, or UI output with documented exit states.
5. **Story:** As a maintainer, I want deterministic fixtures and automated tests, so that changes do not silently break supported behavior.
   - **Acceptance criteria:** Tests cover the happy path, malformed input, empty input, cancellation or recovery, and one platform or integration boundary.
6. **Story:** As a privacy-conscious user, I want local-first processing and explicit network controls, so that I understand where data goes.
   - **Acceptance criteria:** The documentation lists every outbound connection; optional integrations are disabled until configured.

## MVP scope

### Must have
- One verified installation path and a five-minute quick start.
- Core workflow with realistic sample input and expected output.
- Typed configuration, actionable validation, and structured logging.
- Preview or dry-run behavior for risky operations.
- Local persistence only where it adds clear value.
- Exportable results and documented exit states.
- Unit and integration tests for the critical path.

### Not in v0.1 of the product
- Enterprise SSO, billing, multi-tenancy, or complex role hierarchies.
- Large plugin marketplace or broad no-code workflow builder.
- Automatic destructive remediation without review and recovery guidance.
- Cloud dependency when a local implementation can satisfy the main use case.

## Suggested technical approach

**Python stack:** FastAPI, SQLite or PostgreSQL, APScheduler

```text
src/cron_observatory/
├── domain/          # models, rules, and domain errors
├── services/        # application workflows
├── adapters/        # files, APIs, databases, processes
├── interfaces/      # CLI, desktop, or web presentation
└── app.py            # dependency composition

tests/
├── fixtures/
├── unit/
└── integration/
```

Implementation principles:
- Keep domain logic independent from the presentation framework.
- Use typed models at all external boundaries.
- Treat filesystem, network, process, and model access as replaceable adapters.
- Redact credentials and personal data from logs and reports.
- Design non-interactive operation and exit codes early, even if the first interface is graphical.

## Suggested delivery plan

1. **Problem contract:** define three representative inputs, expected outputs, failure modes, and non-goals.
2. **Walking skeleton:** package layout, configuration, logging, one interface, and one end-to-end fixture.
3. **Core workflow:** implement the primary transformation, analysis, or orchestration path.
4. **Reliability:** add preview, malformed-input handling, idempotency where relevant, and security tests.
5. **Release:** publish documentation, demonstration assets, changelog, and tagged `v0.1.0`.

## Bonus features

- Plugin or connector SDK with one reference adapter.
- Saved recipes, templates, or reusable policy packs.
- Comparison between two runs with a clear change report.
- Container image and GitHub Actions example.
- Accessibility and keyboard-navigation pass for user interfaces.
- Optional telemetry that is disabled by default and excludes payload content.

## Success measures

- A new user completes the core workflow from the README without modifying source code.
- Representative fixtures produce deterministic and explainable results.
- A failed run identifies the affected item, probable cause, and next action.
- The critical path has automated test coverage and a documented support matrix.
- Three external users can complete the task and explain why the product is preferable to their current workaround.

## Risks and guardrails

- **Scope creep:** protect the single core workflow and defer adjacent workflows.
- **Unsafe automation:** default to preview, explicit approval, backups, and reversibility when applicable.
- **False confidence:** expose uncertainty, evidence, exclusions, and unverified assumptions.
- **Security and privacy:** minimize retention, redact secrets, use least privilege, and document every network boundary.
- **Platform variance:** publish the tested operating-system and dependency matrix.
- **Maintenance burden:** prefer stable dependencies and isolate optional integrations.

## Open-source and optional business path

VH; hosted monitoring

The open-source edition should remain useful by itself. Sustainable paid value may come from hosting, shared workspaces, managed connectors, policy packs, fleet-wide reporting, support, or compliance evidence, not from disabling the fundamental local workflow.

## Evidence status

This is a proposed product hypothesis added in v0.2.0. Before presenting demand as validated, add primary research, issue/forum evidence, competitor analysis, or interviews with at least three target users.

## Definition of done

- [ ] Core user stories and acceptance criteria demonstrated
- [ ] Clean-environment installation verified
- [ ] Sample input and expected output included
- [ ] Unit and integration checks passing
- [ ] Security, privacy, and network assumptions documented
- [ ] License, changelog, contribution guide, and release notes included
- [ ] Screenshot, terminal recording, or short demonstration added
