# Profile README audit, 14 Oct 2026

Standard: Azure-first agentic AI architect for regulated financial services, Bedrock second, London from March 2027; proof is production-agent-platform and python-reps; prose is Ozgur's; one CI badge at most; no meta-phrasing; tables only where read.

Mechanical fixes (sections 1 and 3) are applied in this PR. Everything else is listed for Ozgur.

## 1. Links

All 12 GitHub links resolve (200). ozgurguler.org 200, x.com 200.

- Medium links return 403 to curl and LinkedIn returns 999: both are bot blocks, not dead links. Checked in a browser they load. No change.
- **Mismatch, fixed:** profile said production-agent-platform is at "S1 MCP tools in build". The repo's own stage table (README on main, after PR #2) says S0 done, S1 **planned**. Profile now says "S0 scaffold with CI merged; S1 MCP tools planned". When P1 runs and the repo table flips to "in build", flip the profile.
- python-reps: table says "25–45 min, no AI during the timer, tests given, commit when the timer ends" and "Agents SDK primitives rebuilt from memory and diffed against source". The repo README states the same rule. The drills folder holds only a README (no drills recorded yet); the table wording "rebuilt from memory" describes the practice, not a result. See 2.
- Supporting rows: each repo exists and is unarchived; descriptions match the row text. Last pushes: Dec 2025 to Apr 2026. None labelled with a date on the profile.

## 2. Claims not backed by a repo file today

| Claim on page | Where it stands | File that should back it |
|---|---|---|
| "eval scores as a merge gate", "promptfoo / inspect-ai harnesses" (What I build) | azure-foundry-cont-eval has a harness; no CI merge gate exists in any repo | production-agent-platform `evals/` + CI step (S3) |
| "MCP servers with OAuth 2.1 authorisation, scoped permissions" | platform S1 server is stdio, no auth; no repo has OAuth-scoped MCP | `src/pap/api/`, `docs/architecture/api-security.md` (S5) |
| "human review on the irreversible actions" | not implemented anywhere | S4 approval gate + test |
| "HLD / LLD, ADRs, NFR budgets, threat models ... EU AI Act / NIST / ISO 42001 / DPIA, FCA and PRA" | one ADR exists (ADR-0001); docs/architecture and docs/governance are empty | `docs/architecture/*`, `docs/governance/*` (S8) |
| "RAPTOR, GraphRAG, hybrid search with RRF" | ai-search-raptor, advanced-rag-ozg, graph-ai-tutor exist (Dec 2025 to Feb 2026) | backed; add dates if kept |
| "continuous evaluation on Azure AI Foundry" | azure-foundry-cont-eval (Mar 2026) | backed |
| Flagship row: "tracing with cost per 1k requests and p95 published" | nothing measured; stated as the target with "numbers land from S3" | `docs/evidence/production-evidence.md` (S6) |
| Flagship row: "RAG with an eval gate in CI" | not yet | S3 |
| python-reps row: "Agents SDK primitives rebuilt from memory and diffed against source" | `drills/sdk-recall/README.md` only; no drill committed | first `drills/sdk-recall/<primitive>/DIFF.md` |
| python-reps row: "commit timestamps are the evidence" | one commit, by the scaffolding session, not a timed run | the first `rN/<name>` branch with LOG.md filled |
| Proof intro: "the bar for the two is a README with an architecture diagram, tests, CI, a Dockerfile and an eval report" | platform: tests, CI, Dockerfile yes; architecture diagram is a placeholder; no eval report. python-reps: tests and CI yes; diagram and eval report do not apply | platform `README.md` architecture section (S2), `docs/evidence/eval-report.md` (S3) |
| "How I work": "Dockerfile and GitHub Actions as the standard for active builds" | true for the platform; python-reps has CI, no Dockerfile (not needed) | fine |

The "What I build" bullets read as capabilities held, while the repos today show them as planned stages. Either date-stamp the supporting repos that do back a bullet, or phrase the bullets as what the platform is being built to do. Prose, so yours.

## 3. Ornament (fixed)

- Removed the nine-badge technology wall under "How I work" (Python, Azure AI Foundry, Bedrock, Agents SDK, MCP, Docker, GitHub Actions, OpenTelemetry, PostgreSQL). The paragraph above it already names the tools.
- Replaced the four shields.io link badges (Website, LinkedIn, Medium, X) with one plain-text link line. Same four destinations, no images.
- No stats card, visitor counter or emoji present. No CI badge present; the platform repo's CI badge could be added later if wanted (at most one).

## 4. Voice

Not rewritten. Questions whose answers would make each paragraph yours.

**Bio paragraph (line 5).** Uniform long clauses, stacked abstractions ("eval gates, tracing, guardrails and a human-review path").
1. Which one customer system at the Istanbul hub went to production, and what broke in it first?
2. What did the AWS startup work teach you that the Microsoft work did not?
3. Which part of the trading-systems years still shapes how you design an agent (latency budget, kill switch, audit trail)?

**"What I build" bullets.** Every bullet is a comma-separated list of nouns; nothing only you would know.
1. Which client pattern made you add the human-approval gate at 500 GBP rather than at every refund?
2. Which of these have you run in front of a sceptical reviewer, and what did they push back on?
3. If you had to drop two bullets, which two, and why do the other three survive?

**Proof intro (line 26).** Contains "say honestly", which the standard forbids as meta-phrasing. Otherwise fine.
1. What is the one number you most want on this page by December, and from which stage does it come?
2. Why two repos rather than one?
3. What does "supporting work" mean to a reader: safe to ignore, or read after the flagship?

**Flagship row.** A full sentence of planned capabilities in a table cell.
1. What does the agent refuse to do, and why that line?
2. Which single policy document gave the scenario its shape?
3. Which stage are you least sure you can finish, and what would you cut?

**"How I work" (line 53).** Tool list plus a process claim ("reviewed line by line").
1. What is your rule for which code you type yourself versus what the agent scaffolds (the `[human]` / `[pair]` / `[agent]` commit tags)?
2. What did Claude Code or Codex get wrong last week that the review caught?
3. How long is a typical build block, and what ends it?

## 5. Missing (listed only)

- No link to the build log (production-agent-platform `docs/log/` and `CHANGELOG.md`) or to the stage table itself.
- No contact route beyond LinkedIn; no email or booking link for agencies.
- Availability line gives a month but not a form (contract, inside/outside IR35, day rate band, hybrid or on-site).
- "How I work" does not state the human/agent split in one sentence or name the commit-tag convention.
- Writing has no dates; latest piece is not marked.
- No one-line "what I am doing this week" or last-updated stamp, so a reader cannot tell the page is live.
- No CV or one-page summary link for recruiters who will not read a repo.
- Sector evidence: nothing names a regulated-FS engagement, even anonymised.

## 6. Freshness

- **Bio field on GitHub says "London from January 2027"; README says "March 2027".** Pick one and fix the bio in Settings (not in this repo).
- GitHub location field: Istanbul. Fine if true today; revisit when the move date is firm.
- Company field: empty. Good (the plan asked for Microsoft to be cleared).
- "Most recently I was an AI Solutions Engineer at Microsoft": no end date on the page. A reader cannot tell if that was last month or 2024.
- Supporting repos last pushed Dec 2025 to Apr 2026; none marked with a date, so "earlier" is unquantified.
- Writing: newest piece undated; the LATS article is 2024-era.
