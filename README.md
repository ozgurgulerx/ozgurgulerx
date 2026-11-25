## Ozgur Guler

[![Total GitHub stars](https://img.shields.io/github/stars/ozgurgulerx?style=flat&label=Total%20stars)](https://github.com/ozgurgulerx?tab=repositories&sort=stargazers)

**AI architect. I design agent and RAG systems on Amazon Bedrock / AgentCore and Azure AI Foundry, and the path that takes them from prototype to production.**

Most recently I was an AI Solutions Engineer at Microsoft's AI innovation hub: use-case workshops with enterprise customers, prototypes on Azure AI Foundry, and deployment planning with their engineering teams. Before that I was Microsoft's cloud and AI tech lead for AI-core startups, and a Solutions Architect at AWS, first for telcos and then for startups. I started in networks: low-latency trading networks at J.P. Morgan and Automat (part of Citadel), and service-provider core and data-centre networks as a Principal System Architect at Cisco.

[![Website](https://img.shields.io/badge/Website-ozgurguler.org-111?style=flat&logo=firefoxbrowser&logoColor=white)](https://ozgurguler.org/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ozguler/)
[![Writing](https://img.shields.io/badge/Writing-Medium-000?style=flat&logo=medium&logoColor=white)](https://medium.com/@343544)
[![X](https://img.shields.io/badge/X-000000?style=flat&logo=x&logoColor=white)](https://x.com/ozgurgulerx)

---

### What I work on

- **Agents on Amazon Bedrock and AgentCore** — Bedrock Converse, Guardrails, and the AgentCore runtime, gateway, identity and memory. I am building an order-support agent here stage by stage, with MCP tools behind OAuth scopes.
- **Agents on Azure AI Foundry** — Foundry Agent Service, Microsoft Agent Framework / Semantic Kernel, Azure AI Search grounding, APIM as the AI gateway, Entra agent identity.
- **Secure tool use** — MCP servers with OAuth 2.1 authorisation, scoped permissions, and human approval on the actions that cannot be undone.
- **Evals and release gates** — regression suites and continuous evaluation, with eval scores used as a merge gate.
- **Retrieval** — hybrid search with RRF, RAPTOR, GraphRAG, PII controls and retrieval evals.

---

### Repos

Two builds are active; the rest is earlier supporting work. Each active repo has a stage table that says what is merged and what is planned.

| Track | What it shows | Repos |
| --- | --- | --- |
| **Agents on AWS (active)** | Amazon Bedrock Converse client with offline tests, AgentCore architecture notes for an order-support agent (model loop, tools, session context, runtime), and a SageMaker inference guide. The agent build with MCP tools and OAuth is in progress. | [aws-bedrock-agentcore](https://github.com/ozgurgulerx/aws-bedrock-agentcore) |
| **Agent platform on Azure (active)** | Support-operations agent on Azure AI Foundry: MCP tools behind OAuth scopes with Entra as the authorisation server, guardrails and a human-approval path, RAG with an eval gate in CI, tracing. Built in stages; numbers are published as each stage lands. | [production-agent-platform](https://github.com/ozgurgulerx/production-agent-platform) |
| Timed Python | Daily timed Python exercises: no AI during the timer, tests given, commit when the timer ends. | [python-reps](https://github.com/ozgurgulerx/python-reps) |
| Evals | Continuous-evaluation harness for agents on Azure AI Foundry; release gates and regression suites. | [azure-foundry-cont-eval](https://github.com/ozgurgulerx/azure-foundry-cont-eval) |
| Retrieval | Hybrid and tree-structured retrieval, PII-safe RAG, GraphRAG. | [pii-fund-rag](https://github.com/ozgurgulerx/pii-fund-rag), [ai-search-raptor](https://github.com/ozgurgulerx/ai-search-raptor), [advanced-rag-ozg notes](https://github.com/ozgurgulerx/advanced-rag-ozg), [graph-ai-tutor](https://github.com/ozgurgulerx/graph-ai-tutor) |
| Security and PII | PII detection and redaction, AI security controls and threat-model notes. | [presidio-pii-ozg](https://github.com/ozgurgulerx/presidio-pii-ozg) |
| Agent frameworks | Microsoft Agent Framework samples, durable long-running workflows, Foundry Agent Service memory. | [agent-framework-ozg](https://github.com/ozgurgulerx/agent-framework-ozg), [af-durable-harness-examples](https://github.com/ozgurgulerx/af-durable-harness-examples), [foundry-agent-service-memory](https://github.com/ozgurgulerx/foundry-agent-service-memory) |
| Inference | Lab notebook on LLM serving: vLLM, TensorRT-LLM and Triton benchmarks. | [inference-journal](https://github.com/ozgurgulerx/inference-journal) |

Earlier work on GNN retrieval and LLM reasoning (LATS) is under [Repositories](https://github.com/ozgurgulerx?tab=repositories).

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
![AWS](https://img.shields.io/badge/-Amazon%20Bedrock%20%2F%20AgentCore-232F3E?style=flat&logo=amazonaws&logoColor=white)
![Azure](https://img.shields.io/badge/-Azure%20AI%20Foundry-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![OpenAI](https://img.shields.io/badge/-OpenAI%20Agents%20SDK-412991?style=flat&logo=openai&logoColor=white)
![MCP](https://img.shields.io/badge/-MCP-000?style=flat)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/-GitHub%20Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/-OpenTelemetry-000?style=flat&logo=opentelemetry&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
