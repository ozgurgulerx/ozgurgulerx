## Ozgur Guler

**Azure-first agentic AI architect for regulated financial services. Amazon Bedrock second. London from March 2027.**

I design and ship production agent systems: RAG and tool-using agents on Azure AI Foundry with MCP and OAuth-scoped tools, eval gates, tracing, guardrails and a human-review path — and the architecture and governance packs a regulated client needs to sign them off. Most recently I was an AI Solutions Engineer at Microsoft (Istanbul innovation hub), building and productionising GenAI systems with enterprise customers. Before that: startup Solutions Architect at AWS in London, low-latency trading systems at J.P. Morgan and Citadel's Automat, and service-provider networks as a Principal Architect at Cisco Systems UK.

[![Website](https://img.shields.io/badge/Website-ozgurguler.org-111?style=flat&logo=firefoxbrowser&logoColor=white)](https://ozgurguler.org/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ozguler/)
[![Writing](https://img.shields.io/badge/Writing-Medium-000?style=flat&logo=medium&logoColor=white)](https://medium.com/@343544)
[![X](https://img.shields.io/badge/X-000000?style=flat&logo=x&logoColor=white)](https://x.com/ozgurgulerx)

---

### What I build

- **Production agent systems** — OpenAI Agents SDK, Microsoft Agent Framework / Semantic Kernel and LangGraph; bounded tool-calling loops, handoffs, sessions, structured outputs, streaming.
- **Secure tool use** — MCP servers with OAuth 2.1 authorisation, scoped permissions, trust boundaries, red-team cases and human review on the irreversible actions.
- **Evals and release gates** — regression and safety suites, continuous evaluation on Azure AI Foundry, promptfoo / inspect-ai harnesses, eval scores as a merge gate.
- **Retrieval** — hybrid search with RRF, RAPTOR, GraphRAG, PII controls, retrieval evals on Azure AI Search.
- **Architecture and governance for regulated clients** — HLD / LLD, ADRs, NFR budgets (p95, cost per 1k requests), threat models, rollout and rollback, EU AI Act / NIST AI RMF / ISO 42001 / DPIA, FCA and PRA model-risk expectations.

---

### Proof

The target bar for active proof projects is a README with an architecture diagram, tests, CI, a Dockerfile, and an eval report with numbers. Existing repositories vary in maturity; the production agent workbench identifies its current stage, and notes are labelled below.

| Track | What it shows | Repos |
| --- | --- | --- |
| Production agent on Azure | RAG + agent on Azure AI Foundry with MCP tools, OAuth, evals, tracing, guardrails and a human-review path; eval scores, p95 and cost per 1k requests published | [secure-agent-deployment-proof](https://github.com/ozgurgulerx/secure-agent-deployment-proof) *(in build — scaffold, tests and CI first; numbers land as each stage ships)* |
| Evals | Reproducible continuous-evaluation harness for agents on Azure AI Foundry; release gates and regression suites | [azure-foundry-cont-eval](https://github.com/ozgurgulerx/azure-foundry-cont-eval) |
| Retrieval | Hybrid and tree-structured retrieval, PII-safe RAG, GraphRAG | [pii-fund-rag](https://github.com/ozgurgulerx/pii-fund-rag), [ai-search-raptor](https://github.com/ozgurgulerx/ai-search-raptor), [advanced-rag-ozg notes](https://github.com/ozgurgulerx/advanced-rag-ozg), [graph-ai-tutor](https://github.com/ozgurgulerx/graph-ai-tutor) |
| Security and PII | PII detection and redaction, AI security controls and threat-model notes | [presidio-pii-ozg](https://github.com/ozgurgulerx/presidio-pii-ozg) |
| Agent frameworks | Microsoft Agent Framework samples, durable long-running workflows, Foundry Agent Service memory | [agent-framework-ozg](https://github.com/ozgurgulerx/agent-framework-ozg), [af-durable-harness-examples](https://github.com/ozgurgulerx/af-durable-harness-examples), [foundry-agent-service-memory](https://github.com/ozgurgulerx/foundry-agent-service-memory) |

Earlier public work on inference engineering, GNN retrieval and LLM reasoning (LATS) is still here under [Repositories](https://github.com/ozgurgulerx?tab=repositories); it is not the focus of what I take to clients.

---

### Writing

- [Building Production AI with Microsoft's Agent Framework: Credit Underwriting Case Study](https://medium.com/microsoftazure/building-production-ai-with-microsofts-agent-framework-credit-underwriting-case-study-a40d8335d4ed) — Microsoft Azure publication
- [Context Engineering with Microsoft Agent Framework's Context Provider API](https://medium.com/microsoftazure/context-engineering-with-microsoft-agent-frameworks-context-provider-api-dcf083daa8be) — Microsoft Azure publication
- [Fixing Sparse Retrieval with RAPTOR on Azure AI Search](https://medium.com/microsoftazure/fixing-sparse-retrieval-with-raptor-on-azure-ai-search-4d540dd3bd43) — Microsoft Azure publication
- [The Missing Piece in Graph RAG: Graph Attention Networks](https://medium.com/@343544/the-missing-piece-in-graph-rag-graph-attention-networks-f50cb9857895)
- [Tackle Complex LLM Decision-Making with Language Agent Tree Search (LATS) and GPT-4o](https://medium.com/data-science/tackle-complex-llm-decision-making-with-language-agent-tree-search-lats-gpt4-o-0bc648c46ea4) — Towards Data Science

---

### How I work

Spec and tests first, typed Python (pydantic, pytest, ruff, mypy, uv), small commits on branches with PRs, Dockerfile and GitHub Actions as the standard for active builds. Agent-assisted development with Claude Code and Codex, every generated change reviewed line by line before it merges.

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white)
![Azure](https://img.shields.io/badge/-Azure%20AI%20Foundry-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![AWS](https://img.shields.io/badge/-Amazon%20Bedrock-232F3E?style=flat&logo=amazonaws&logoColor=white)
![OpenAI](https://img.shields.io/badge/-OpenAI%20Agents%20SDK-412991?style=flat&logo=openai&logoColor=white)
![MCP](https://img.shields.io/badge/-MCP-000?style=flat)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/-GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/-OpenTelemetry-000?style=flat&logo=opentelemetry&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
