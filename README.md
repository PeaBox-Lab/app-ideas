# PeaBox Builder Ideas

A product-minded collection of **50 practical Python and open-source application ideas**. Each idea is a build brief, not just a title: problem framing, target users, MVP user stories with acceptance criteria, technical direction, delivery plan, risks, success measures, bonus features, and an optional sustainable-business path.

Inspired by [Florin Pop's App Ideas collection](https://github.com/florinpop17/app-ideas), but designed for developers who want to move from **idea → scoped MVP → reliable open-source release**.

## Why this collection is different

- **Evidence-aware:** distinguishes an observed problem from an unvalidated assumption.
- **Product-ready:** every page includes users, differentiation, scope, metrics, and risk controls.
- **Engineering-ready:** each concept contains a Python approach, architecture guidance, tests, and release criteria.
- **Responsible by default:** local-first processing, previews, redaction, rollback, and least privilege appear where relevant.
- **Business optional:** the open-source core remains useful; commercial extensions are clearly separated.

## Browse the collection

| Tier | Typical profile | Ideas |
|---|---|---:|
| Starter | Focused CLI, utility, or small local app; usually a weekend prototype | 9 |
| Intermediate | Multiple components, richer validation, storage, or integrations | 16 |
| Advanced | Broader workflows, infrastructure, AI, security, or cross-platform complexity | 25 |

### Starter

| # | Idea | What you build | Effort |
|---:|---|---|---|
| 3 | [EnvDoctor](ideas/starter/envdoctor.md) | Validate .env files against typed schemas; identify missing/unused variables; generate Pydantic settings and sanitized .env.example. | Weekend |
| 10 | [RepoReady](ideas/starter/repoready.md) | Audit repository readiness and generate missing LICENSE, security policy, CI, release, issue-template and contributor files. | Weekend |
| 19 | [PortPilot](ideas/starter/portpilot.md) | Scan Compose files and running processes; show conflicts and propose safe alternative ports. | Weekend |
| 33 | [PathFixer](ideas/starter/pathfixer.md) | Preflight archives, preview safe renames and create a reversible extraction manifest. | Weekend |
| 34 | [ArchiveDoctor](ideas/starter/archivedoctor.md) | Recursively inventory archives, test integrity, detect multipart sets and create verification reports. | Weekend |
| 35 | [Encoding Detective](ideas/starter/encoding-detective.md) | Compare detectors, highlight suspicious bytes, preview normalization and save a provenance report. | Weekend |
| 37 | [ContactSheet Pro](ideas/starter/contactsheet-pro.md) | Generate searchable HTML/PDF contact sheets with metadata, duplicate groups and selection export. | Weekend |
| 45 | [RetryRunner](ideas/starter/retryrunner.md) | Wrap any command with typed retry policies, timeout, circuit breaker, notifications and structured run history. | Weekend |
| 50 | [SelfHost Cost Lens](ideas/starter/selfhost-cost-lens.md) | Transparent calculator for deployment scenarios, capacity assumptions and exportable decision records. | Weekend |
### Intermediate

| # | Idea | What you build | Effort |
|---:|---|---|---|
| 4 | [SemanticDiff](ideas/intermediate/semanticdiff.md) | Semantic JSON/YAML/TOML/OpenAPI diff with identity keys, ignored paths, breaking-change rules and HTML/Markdown reports. | 1–2 wk |
| 6 | [CSV Surgeon](ideas/intermediate/csv-surgeon.md) | Local drag-and-drop data profiler with previewable repairs and a reproducible transformation recipe. | 1–2 wk |
| 11 | [DataContract Watch](ideas/intermediate/datacontract-watch.md) | Capture a lightweight data contract, compare new deliveries and emit actionable schema/drift reports. | 1–2 wk |
| 12 | [FileSafe](ideas/intermediate/filesafe.md) | Cross-platform copy/sync utility with checksums, atomic writes, restartable manifests and dry-run conflict handling. | 1–2 wk |
| 13 | [DupeSafe](ideas/intermediate/dupesafe.md) | Exact and perceptual duplicate finder with preview, reversible quarantine and “why matched” evidence. | 1–2 wk |
| 18 | [Webhook Lab](ideas/intermediate/webhook-lab.md) | Self-hosted request inbox, replay tool, transformer and signature verifier. | 1–2 wk |
| 23 | [QuickShare Vault](ideas/intermediate/quickshare-vault.md) | One-command encrypted upload with expiry, download limit and optional recipient password. | 1–2 wk |
| 25 | [HabitPlain](ideas/intermediate/habitplain.md) | Mobile-first PWA for schedules, streaks, CSV export and reminders; local-first by default. | 1–2 wk |
| 30 | [SQLite Guardian](ideas/intermediate/sqlite-guardian.md) | Discover SQLite files, run online backup, integrity-check snapshots and perform automated restore drills. | 1–2 wk |
| 32 | [Endpoint Watch](ideas/intermediate/endpoint-watch.md) | YAML-configured checks, assertion rules, history and webhook/email alerts. | 1–2 wk |
| 36 | [TimeClean](ideas/intermediate/timeclean.md) | Profile datetime columns, explain ambiguity, preview UTC conversion and output reproducible rules. | 1–2 wk |
| 38 | [LinkSentinel](ideas/intermediate/linksentinel.md) | Local crawler with redirect history, duplicate detection, archive suggestions and scheduled reports. | 1–2 wk |
| 40 | [SecretScope](ideas/intermediate/secretscope.md) | Local scanner with entropy/pattern checks, commit-history mode and guided rotation checklist. | 1–2 wk |
| 41 | [MCP Permission Linter](ideas/intermediate/mcp-permission-linter.md) | Inspect MCP manifests/tool definitions and produce least-privilege warnings and allowlists. | 1–2 wk |
| 46 | [SettingsPanel](ideas/intermediate/settingspanel.md) | Generate a local web settings UI automatically from a Pydantic model, including validation and secret masking. | 1–2 wk |
| 47 | [LineageManifest](ideas/intermediate/lineagemanifest.md) | Produce portable provenance manifests with hashes, environment, transformation steps and verification CLI. | 1–2 wk |
### Advanced

| # | Idea | What you build | Effort |
|---:|---|---|---|
| 1 | [CodeProof AI](ideas/advanced/codeproof-ai.md) | CLI/GitHub Action that generates tests, checks imports/types/security and produces an evidence-backed confidence report—not another code generator. | 3–4 wk |
| 2 | [PackForge](ideas/advanced/packforge.md) | Interactive wizard that inspects a project and generates tested PyInstaller/Nuitka specs plus GitHub Actions releases. | 3–4 wk |
| 5 | [ComposeRescue](ideas/advanced/composerescue.md) | Analyse Compose files, create app-consistent backups and prove them by restoring into temporary containers. | 3–4 wk |
| 7 | [PDF Table Workbench](ideas/advanced/pdf-table-workbench.md) | Run multiple extractors, overlay detected cells, let users correct boundaries, then export CSV plus reusable templates. | 3–4 wk |
| 8 | [TinyLog](ideas/advanced/tinylog.md) | Single-container log inbox with tailing, search, retention, simple alerts and no query language requirement. | 3–4 wk |
| 9 | [PromptLedger](ideas/advanced/promptledger.md) | Git-native prompt registry and eval runner using decorators rather than an intrusive LLM framework. | 3–4 wk |
| 14 | [API Replay Lab](ideas/advanced/api-replay-lab.md) | Record, sanitize and replay HTTP interactions; generate deterministic pytest tests and mock APIs. | 2–3 wk |
| 15 | [LicensePath](ideas/advanced/licensepath.md) | Dependency-license graph with policy rules, transitive notices and migration suggestions—without giving legal conclusions. | 2–3 wk |
| 16 | [PyMemory Timeline](ideas/advanced/pymemory-timeline.md) | Attach to a process, graph RSS/USS/object growth and compare two runs with leak candidates. | 3–4 wk |
| 17 | [SchemaMapper](ideas/advanced/schemamapper.md) | Infer schemas, visually map fields, preview coercions and export reusable mapping code. | 2–3 wk |
| 20 | [TestData Studio](ideas/advanced/testdata-studio.md) | Schema-aware generator with referential integrity, deterministic seeds and configurable masking. | 2–3 wk |
| 21 | [IssueTwin](ideas/advanced/issuetwin.md) | Local issue-clustering dashboard with explainable similarity and maintainer-approved duplicate comments. | 2–3 wk |
| 22 | [LocalNoteHub](ideas/advanced/localnotehub.md) | Files remain plain Markdown; add web editing, Git history, expiring share links and no proprietary database. | 2–3 wk |
| 24 | [MiniDesk](ideas/advanced/minidesk.md) | Email/form-to-GitHub-Issue bridge with reminders, attachments and personal queue—no full ITSM suite. | 2–3 wk |
| 26 | [OCR Review Desk](ideas/advanced/ocr-review-desk.md) | Side-by-side scan/text review, confidence highlighting, keyboard correction and searchable export. | 3–4 wk |
| 27 | [DocBatch](ideas/advanced/docbatch.md) | Template-driven image/PDF generation with CSV input, validation, approval manifest and connector plugins. | 2–3 wk |
| 28 | [SubtitleSync](ideas/advanced/subtitlesync.md) | Local subtitle alignment, drift correction and confidence review without uploading media. | 2–3 wk |
| 29 | [ConfigMigrator](ideas/advanced/configmigrator.md) | Declarative migration recipes, semantic preview, rollback and repository-wide application. | 2–3 wk |
| 31 | [CronCanvas](ideas/advanced/croncanvas.md) | Cross-platform UI/CLI that generates, validates and monitors schedules with portable YAML definitions. | 2–3 wk |
| 39 | [BugPack](ideas/advanced/bugpack.md) | Capture screenshot, redact sensitive regions and package system/app diagnostics into a GitHub-ready report. | 2–3 wk |
| 42 | [LocalLLM Bench](ideas/advanced/localllm-bench.md) | Reproducible benchmark packs for latency, memory, structured output and user-owned task sets. | 2–3 wk |
| 43 | [ModelFit](ideas/advanced/modelfit.md) | Detect hardware, estimate memory needs and benchmark a short candidate list locally. | 2–3 wk |
| 44 | [PromptShield Tests](ideas/advanced/promptshield-tests.md) | pytest-style adversarial test packs with local execution, expected policies and regression reports. | 2–3 wk |
| 48 | [AccessBatch](ideas/advanced/accessbatch.md) | Crawl sites, run deterministic checks, collect screenshots and create developer-friendly issue bundles. | 3–4 wk |
| 49 | [RedactReview](ideas/advanced/redactreview.md) | Local visual redaction assistant that proposes—not automatically trusts—email, phone and ID regions and permanently verifies removal. | 2–3 wk |

## How to use an idea

1. Pick a problem you personally understand.
2. Read the full idea page and challenge its assumptions.
3. Build only the **Must have** scope first.
4. Treat the user stories as outcome guidance, not rigid implementation instructions.
5. Publish a small `v0.1.0`, gather feedback, then choose bonus features.
6. Add your implementation to the **Showcase an implementation** issue template.

## Repository map

```text
.
├── ideas/
│   ├── starter/
│   ├── intermediate/
│   └── advanced/
├── docs/
│   ├── IDEA_TEMPLATE.md
│   └── SCORING_GUIDE.md
├── .github/
│   ├── ISSUE_TEMPLATE/
│   ├── pull_request_template.md
│   └── workflows/markdown.yml
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

## Contributing

New ideas, corrections, stronger evidence, clearer acceptance criteria, and implementation links are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) and use [the idea template](docs/IDEA_TEMPLATE.md).

## License

Content and templates are available under the [MIT License](LICENSE). External links remain subject to their respective owners' terms.
