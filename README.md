## Özgür Güler

**AI architect. I design agents, the tools they call, and the controls that decide what an agent is allowed to do, on Amazon Bedrock / AgentCore and Azure AI Foundry.**

These days I build agents and the tools they call. I got here through infrastructure: service-provider networks at Cisco, low-latency trading networks in London at J.P. Morgan and Automat (part of Citadel), then cloud architecture at AWS and enterprise AI at Microsoft. One question I keep coming back to is what happens when an agent asks to do something it shouldn’t.

### What happens when an agent tries to issue a refund above its limit?

```mermaid
flowchart LR
    A["Agent calls<br/>issue_refund(ticket, 600.00)"] --> B{"Valid access token?"}
    B -- no --> X1["401, tool never runs"]
    B -- yes --> C{"Token carries<br/>tickets.refund scope?"}
    C -- no --> X2["Denied, no refund recorded"]
    C -- yes --> D{"Server-side policy:<br/>limit, team, balance"}
    D -- "600 is over the 500 limit" --> X3["Rejected:<br/>execution_limit_exceeded"]
    D -- within policy --> E{"Human confirms<br/>this exact refund?"}
    E -- no --> X4["Not executed"]
    E -- yes --> F["Refund recorded"]
```

It is refused on the tool server, before a person is ever asked to approve it. The limit is not in the prompt, so the model cannot talk its way past it. The [policy](https://github.com/ozgurgulerx/production-agent-platform/blob/main/Agent-Build-01-Fundamentals/S03-AI-Agents-Tools-and-MCP/S03.03-MCP-OAuth2.1/src/check_refund_policy.py) is under thirty lines, the [tool](https://github.com/ozgurgulerx/production-agent-platform/blob/main/Agent-Build-01-Fundamentals/S03-AI-Agents-Tools-and-MCP/S03.03-MCP-OAuth2.1/src/server.py) checks scope before and after the human step, and [this test](https://github.com/ozgurgulerx/production-agent-platform/blob/main/Agent-Build-01-Fundamentals/S03-AI-Agents-Tools-and-MCP/S03.03-MCP-OAuth2.1/tests/test_refund_above_execution_limit_is_rejected.py) is the question above.

### Selected work

| | What it is | Where it stands |
| --- | --- | --- |
| **[MCP tools behind OAuth 2.1](https://github.com/ozgurgulerx/production-agent-platform/tree/main/Agent-Build-01-Fundamentals/S03-AI-Agents-Tools-and-MCP/S03.03-MCP-OAuth2.1)** | An MCP server for support tickets and refunds: JWT validation, a scope per tool, server-side policy on simulated refunds, and human confirmation before the refund is recorded. | 119 tests passing. Live refund denial and confirmation checks against the authorisation server are still to do. |
| **[Amazon Bedrock and AgentCore](https://github.com/ozgurgulerx/aws-bedrock-agentcore)** | A Bedrock Converse client with [offline tests](https://github.com/ozgurgulerx/aws-bedrock-agentcore/blob/main/tests/test_bedrock_quickstart.py) for request construction and error handling, and an [AgentCore architecture walkthrough](https://github.com/ozgurgulerx/aws-bedrock-agentcore/blob/main/skills/mindmap/references/agentcore-example.md) for an order-support agent. | In build. The agent and its tools on AgentCore come next; live inference is not yet verified. |
| **[Continuous evaluation on Azure AI Foundry](https://github.com/ozgurgulerx/azure-foundry-cont-eval)** | A harness that schedules agent evaluations, sends controlled traffic and [checks that evaluation runs appear](https://github.com/ozgurgulerx/azure-foundry-cont-eval/blob/main/scripts/verify_evaluation.py). | Working harness, used as a release-gate pattern. |

[More repositories](https://github.com/ozgurgulerx?tab=repositories)

### Writing

- [Agent Governance on Microsoft Foundry, Part II](https://medium.com/microsoft/agent-governance-on-microsoft-foundry-part-ii-your-own-mcp-server-the-agents-own-identity-and-3bcbc331907f) — What changes when an agent gets its own identity and an Entra app role for a custom MCP tool.
- [Building Production AI with Microsoft’s Agent Framework](https://medium.com/microsoftazure/building-production-ai-with-microsofts-agent-framework-credit-underwriting-case-study-a40d8335d4ed) — A credit-underwriting case study.
- [Fixing Sparse Retrieval with RAPTOR on Azure AI Search](https://medium.com/microsoftazure/fixing-sparse-retrieval-with-raptor-on-azure-ai-search-4d540dd3bd43) — Tree-structured retrieval when chunks alone miss the answer.

[Website](https://ozgurguler.org/) · [LinkedIn](https://www.linkedin.com/in/ozguler/)
