# PeaBox Builder Ideas

> **100 product-ready software ideas: problem → users → stories → MVP → architecture → release.**

PeaBox Builder Ideas is a curated collection of practical Python and open-source product briefs. Every idea has its own build page covering target users, product differentiation, testable user stories, acceptance criteria, MVP boundaries, technical direction, delivery steps, risks, success measures, and an optional sustainable-business path.

The structure was inspired by [Florin Pop's App Ideas collection](https://github.com/florinpop17/app-ideas), then expanded for product discovery, engineering execution, responsible automation, and open-source release readiness.

## What's new in v0.2.0

- Expanded the catalogue from **50 to 100 ideas**.
- Added 50 briefs spanning developer tools, AI engineering, APIs, DevOps, self-hosting, data, OCR, privacy, and local-first productivity.
- Added category navigation alongside Starter, Intermediate, and Advanced tiers.
- Added a complete [v0.2.0 release note](RELEASE_NOTES_v0.2.0.md).
- Added evidence-status guidance so hypotheses are not confused with validated demand.

## Browse

- [Browse all 100 ideas by difficulty](CATALOG.md)
- [Browse by product category](docs/CATEGORIES.md)
- [Score an idea](docs/SCORING_GUIDE.md)
- [Propose an idea](docs/IDEA_TEMPLATE.md)

## Difficulty summary

| Tier | Definition | Count |
|---|---|---:|
| Starter | Focused utility or small local workflow; generally suitable for a weekend prototype | 15 |
| Intermediate | Multiple components, validation, storage, or a significant integration boundary | 21 |
| Advanced | Broader workflows, infrastructure, AI, security, cross-platform, or reliability complexity | 64 |
| **Total** |  | **100** |

## What makes each brief build-ready

1. A problem and target-user definition.
2. A focused product thesis rather than a generic clone.
3. MVP user stories with acceptance criteria.
4. Explicit must-haves and non-goals.
5. Python stack and architecture direction.
6. A staged delivery plan and Definition of Done.
7. Security, privacy, reliability, and scope guardrails.
8. Open-source value plus an optional sustainable-business path.

## Repository map

```text
.
├── ideas/
│   ├── starter/
│   ├── intermediate/
│   └── advanced/
├── docs/
│   ├── CATEGORIES.md
│   ├── IDEA_TEMPLATE.md
│   └── SCORING_GUIDE.md
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/
├── CATALOG.md
├── RELEASE_NOTES_v0.2.0.md
├── ideas.json
└── README.md
```

## Use the collection

1. Choose a problem you have personally observed.
2. Read its page and challenge the evidence status and assumptions.
3. Build only the **Must have** scope.
4. Release `v0.1.0` of the product with a realistic sample and testable demonstration.
5. Gather feedback before adding bonus features.
6. Share the implementation through the repository's Showcase issue form.

## Contributing

Corrections, stronger evidence, clearer acceptance criteria, implementation links, and new ideas are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## License

Content and templates are available under the [MIT License](LICENSE). External references remain subject to their owners' terms.
