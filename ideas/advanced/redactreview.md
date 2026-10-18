# RedactReview

> **Tier:** Advanced · **Estimated MVP effort:** 2–3 wk · **Idea #49**

## One-line pitch

Local visual redaction assistant that proposes—not automatically trusts—email, phone and ID regions and permanently verifies removal.

## Problem

Sharing PDFs/screenshots safely requires slow manual checking.

## Who it is for

- Primary: developers, technical operators, or small teams directly experiencing this workflow.
- Secondary: maintainers and team leads who need repeatability, auditability, or safer hand-offs.
- Early adopter: a user currently solving the problem with scripts, spreadsheets, or several disconnected tools.

## Product thesis and differentiation

Local visual redaction assistant that proposes—not automatically trusts—email, phone and ID regions and permanently verifies removal.

This project should remain focused. It wins by making one difficult workflow understandable, previewable, and reproducible rather than becoming a broad platform.

## MVP user stories

1. **Story:** As a user, I want to configure RedactReview without editing source code, so that I can adapt it safely to my environment.
   - **Acceptance:** Given a valid configuration, when the app starts, then it validates settings and reports actionable errors.
2. **Story:** As a user, I want local visual redaction assistant that proposes—not automatically trusts—email, phone and ID regions and permanently verifies removal, so that I can complete the core job in one reproducible workflow.
   - **Acceptance:** Given representative input, when the workflow runs, then it produces the expected output and records what happened.
3. **Story:** As a user, I want a dry-run or preview before destructive changes, so that I can review the impact.
   - **Acceptance:** No source data is altered during preview; the final action requires an explicit command or confirmation.
4. **Story:** As a user, I want clear success, warning, and failure messages, so that I know what to fix next.
   - **Acceptance:** Errors identify the affected item, probable cause, and a next step; the process returns an appropriate exit status.
5. **Story:** As a user, I want results exported in a portable format, so that I can use them in CI, documentation, or another tool.
   - **Acceptance:** The MVP exports JSON plus a human-readable Markdown or HTML report.
6. **Story:** As a maintainer, I want deterministic tests and sample fixtures, so that changes do not silently break existing behavior.
   - **Acceptance:** Automated tests cover the happy path, invalid input, empty input, and one recovery scenario.
7. **Story:** As a privacy-conscious user, I want processing to remain local by default, so that sensitive data is not uploaded.
   - **Acceptance:** Network access is disabled unless the user enables a documented integration.
8. **Story:** As a repository maintainer, I want a CI-friendly mode, so that checks can run on every pull request.
   - **Acceptance:** The command supports non-interactive execution, machine-readable output, and documented exit codes.

## MVP scope

### Must have
- One documented installation path and a five-minute quick start.
- Core workflow with sample data or fixtures.
- Input validation and actionable error handling.
- Preview or dry-run for risky operations.
- Machine-readable and human-readable output.
- Automated tests for critical paths.

### Not in the first release
- Multi-tenant SaaS administration.
- Enterprise SSO, billing, or complex role hierarchies.
- Mobile applications unless essential to the core workflow.
- Automatic destructive action without review and rollback guidance.

## Suggested technical approach

**Python stack:** PyMuPDF, OCR, Presidio, Streamlit

Suggested structure:

```text
src/redactreview/
├── domain/          # core rules and models
├── services/        # use cases and orchestration
├── adapters/        # filesystem, API, database, CLI/UI
└── app.py            # composition root

tests/
├── fixtures/
├── unit/
└── integration/
```

Design guidance:
- Keep domain logic independent from the UI framework.
- Represent configuration with typed models.
- Log structured events without secrets or personal data.
- Make integrations replaceable through small adapter interfaces.
- Ship examples that can run offline where practical.

## Delivery plan

1. **Discovery:** define three representative inputs, expected outputs, and explicit non-goals.
2. **Walking skeleton:** package layout, CLI or minimal UI, configuration, logging, and one end-to-end test.
3. **Core engine:** implement the primary workflow and dry-run behavior.
4. **Reliability:** malformed-input handling, recovery, idempotency where relevant, and security review.
5. **Release:** documentation, screenshots, sample project, changelog, and tagged `v0.1.0`.

## Bonus features

- Plugin or connector SDK with one example adapter.
- Saved recipes, templates, or reusable policy packs.
- Comparison across two runs with a clear change report.
- Container image and GitHub Actions workflow.
- Accessibility pass for any graphical or web interface.
- Optional telemetry that is disabled by default and contains no sensitive payloads.

## Success measures

- A new user completes the core workflow from the README without source-code changes.
- Representative sample inputs produce deterministic outputs.
- Failures are diagnosable from the report without opening a debugger.
- The core workflow is covered by automated tests.
- At least three external users can describe the value proposition and complete the MVP task.

## Risks and guardrails

- **Scope creep:** protect the single core workflow and move adjacent features to the roadmap.
- **Unsafe automation:** default to preview, explicit confirmation, backups, or reversible quarantine where applicable.
- **Platform variance:** document supported operating systems and test the smallest credible matrix.
- **Security/privacy:** redact secrets from logs, minimize data retention, and perform local processing by default when feasible.
- **Maintenance load:** prefer stable dependencies and isolate optional integrations.

## Open-source and optional business path

H; secure enterprise edition

Keep the open-source core useful on its own. Monetization, if pursued, should come from hosting, collaboration, managed connectors, policy packs, support, or organization-wide reporting rather than crippling the local edition.

## Evidence and references

- No external evidence URL was embedded in the source workbook. Add a primary source before claiming validated demand.

## Definition of done for v0.1

- [ ] Core user stories implemented and acceptance criteria demonstrated
- [ ] Installation and quick-start instructions verified from a clean environment
- [ ] Sample input and expected output included
- [ ] Unit and integration tests passing
- [ ] Security and privacy assumptions documented
- [ ] License, changelog, contribution guide, and release notes present
- [ ] One screenshot, terminal recording, or short demo added
