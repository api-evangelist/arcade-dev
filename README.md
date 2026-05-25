# Arcade.dev (arcade-dev)

Arcade.dev (formerly Arcade AI) is the MCP runtime for production AI agents — a platform that lets agents safely take real-world actions across SaaS apps with per-user authorization, governed tool execution, and audit logging. The Arcade Engine exposes a Tools API for listing / authorizing / executing agent tools, an Authorization API that brokers OAuth and API-key grants across 40+ providers, an OpenAI-compatible LLM endpoint, Workers and MCP Gateways for routing, Hooks for governance, and an Admin API for control-plane configuration. Arcade ships with 7,000+ pre-built integrations across Google, Microsoft, Slack, GitHub, Salesforce, HubSpot, and more, plus an MCP server framework (`arcade-mcp`) and SDKs in Python, TypeScript, Go, Java/Kotlin, and .NET. Available as Arcade Cloud, VPC, on-prem, or air-gapped.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/arcade-dev/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI, Agents, Tools, MCP, Tool Calling, Authorization, OAuth, Identity, Governance, Agent Runtime

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Plans

| Plan | Price | Highlights |
|---|---|---|
| Hobby | Free | 100 user challenges, 1,000 standard executions, 50 pro executions, 1 hosted MCP server, community support |
| Growth | $25/mo + overage | 600 challenges ($0.05 each after), 2,000 std executions ($0.01 each after), 100 pro executions ($0.50 each after), hosted MCP server runtime at $0.05/hr, email SLA |
| Enterprise | Custom | Dedicated infra, RBAC, SSO/SAML, audit logs, tenant isolation, VPC / on-prem / air-gapped, custom SLA |

## APIs

### Arcade Tools API
List, inspect, authorize, execute, and schedule Arcade tools. Tools are user-scoped agent actions addressed by fully qualified name (`Toolkit.Name@version`) and executed against a stable `user_id` with Arcade-managed authorization tokens.

**Human URL:** [https://docs.arcade.dev/home/tools](https://docs.arcade.dev/home/tools)

- [OpenAPI](openapi/arcade-tools-api-openapi.yml)
- [JSON Schema — Tool](json-schema/arcade-tool-schema.json)
- [JSON Schema — Tool Execution](json-schema/arcade-tool-execution-schema.json)
- [JSON Structure — Tool](json-structure/arcade-tool-structure.json)
- [Example — List Tools](examples/arcade-tools-list-example.json)
- [Example — Execute Tool](examples/arcade-tools-execute-example.json)
- [Example — Authorize Tool](examples/arcade-tools-authorize-example.json)
- [Naftiko Capability — Tools](capabilities/tools-tools.yaml)

### Arcade Authorization API
Authorize end-users against 40+ identity providers (Google, Microsoft, Slack, GitHub, Salesforce, HubSpot, and more). Issues user-scoped grants and surfaces authorization status so agents act as the end-user rather than a shared service account.

**Human URL:** [https://docs.arcade.dev/home/auth](https://docs.arcade.dev/home/auth)

- [OpenAPI](openapi/arcade-auth-api-openapi.yml)
- [JSON Schema — Authorization](json-schema/arcade-authorization-schema.json)
- [JSON Structure — Authorization](json-structure/arcade-authorization-structure.json)
- [Example — Authorize](examples/arcade-auth-authorize-example.json)
- [Example — Status](examples/arcade-auth-status-example.json)
- [Naftiko Capability — Authorization](capabilities/auth-auth.yaml)

### Arcade LLM API
OpenAI-compatible chat completions endpoint that lets agents call LLMs through Arcade with tools attached. The Engine handles tool selection, end-user authorization, and tool execution so agents need only speak the OpenAI Chat Completions protocol.

**Human URL:** [https://docs.arcade.dev/home/chat-overview](https://docs.arcade.dev/home/chat-overview)

- [OpenAPI](openapi/arcade-llm-api-openapi.yml)
- [Example — Chat Completion](examples/arcade-llm-chat-completions-example.json)
- [Naftiko Capability — LLM](capabilities/llm-llm.yaml)

### Arcade Workers API
Register, manage, health-check, and authorize workers that host Arcade toolkits or MCP servers behind the Arcade Engine. Self-hosted workers let customers keep tool execution (and end-user tokens) inside their own perimeter.

**Human URL:** [https://docs.arcade.dev/home/workers](https://docs.arcade.dev/home/workers)

- [OpenAPI](openapi/arcade-workers-api-openapi.yml)
- [JSON Schema — Worker](json-schema/arcade-worker-schema.json)
- [JSON Structure — Worker](json-structure/arcade-worker-structure.json)
- [Example — Create Worker](examples/arcade-workers-create-example.json)
- [Naftiko Capability — Workers](capabilities/workers-workers.yaml)

### Arcade Gateways API
Create and manage MCP gateways scoped to organizations and projects. Gateways expose curated tool catalogs to MCP clients (Cursor, Claude Desktop, Claude Code, VS Code, Microsoft Copilot Studio, GitHub Copilot).

**Human URL:** [https://docs.arcade.dev/guides/mcp-gateways](https://docs.arcade.dev/guides/mcp-gateways)

- [OpenAPI](openapi/arcade-gateways-api-openapi.yml)
- [Example — Create Gateway](examples/arcade-gateways-create-example.json)
- [Naftiko Capability — Gateways](capabilities/gateways-gateways.yaml)

### Arcade Hooks API
Manage lifecycle hooks that fire on tool authorization, tool execution, worker health, and audit events. Hooks are the primary integration point for SIEM forwarding, audit logging, and downstream governance pipelines.

**Human URL:** [https://docs.arcade.dev/guides/audit-logs](https://docs.arcade.dev/guides/audit-logs)

- [OpenAPI](openapi/arcade-hooks-api-openapi.yml)
- [JSON Schema — Hook](json-schema/arcade-hook-schema.json)
- [Example — Create Hook](examples/arcade-hooks-create-example.json)
- [Naftiko Capability — Hooks](capabilities/hooks-hooks.yaml)

### Arcade Admin API
Administer Arcade auth providers, organization secrets, user connections, and session verification settings. The control plane behind tool authorization and end-user identity.

**Human URL:** [https://docs.arcade.dev/home/auth-providers](https://docs.arcade.dev/home/auth-providers)

- [OpenAPI](openapi/arcade-admin-api-openapi.yml)
- [Example — Set Secret](examples/arcade-admin-secrets-set-example.json)
- [Naftiko Capability — Admin](capabilities/admin-admin.yaml)

### Arcade Plugins API
Manage plugins that extend the Arcade Engine with custom auth providers, transformers, and tool sources. Plugins let teams bring their own integrations behind the Arcade governance and auth layer.

- [OpenAPI](openapi/arcade-plugins-api-openapi.yml)
- [Naftiko Capability — Plugins](capabilities/plugins-plugins.yaml)

### Arcade Operations API
Operational endpoints exposing service health, engine runtime configuration, and the OpenAPI / swagger description of the Arcade Engine.

- [OpenAPI](openapi/arcade-operations-api-openapi.yml)
- [Example — Health](examples/arcade-operations-health-example.json)
- [Naftiko Capability — Operations](capabilities/operations-operations.yaml)

## Common Properties

- [Portal — arcade.dev](https://arcade.dev)
- [Documentation — docs.arcade.dev](https://docs.arcade.dev)
- [API Reference](https://docs.arcade.dev/references/api)
- [GettingStarted](https://docs.arcade.dev/home)
- [Pricing](https://arcade.dev/pricing)
- [Blog](https://arcade.dev/blog)
- [Changelog](https://docs.arcade.dev/home/release-notes)
- [Sign Up](https://api.arcade.dev/dashboard/auth/login)
- [GitHubOrganization — ArcadeAI](https://github.com/ArcadeAI)
- [SDK — Python (arcadepy)](https://github.com/ArcadeAI/arcade-py)
- [SDK — TypeScript / JavaScript](https://github.com/ArcadeAI/arcade-js)
- [SDK — Go](https://github.com/ArcadeAI/arcade-go)
- [SDK — Java / Kotlin](https://github.com/ArcadeAI/arcade-java)
- [SDK — .NET](https://github.com/ArcadeAI/arcade-dotnet)
- [SDK — arcade-mcp (MCP Server Framework)](https://github.com/ArcadeAI/arcade-mcp)
- [SDK — arcade CLI](https://docs.arcade.dev/home/install/cli)
- [CodeExamples — agent-templates](https://github.com/ArcadeAI/agent-templates)
- [CodeExamples — safeword](https://github.com/ArcadeAI/safeword)
- [Tool — blueprint-mcp](https://github.com/ArcadeAI/blueprint-mcp)
- [Tool — agent-library](https://github.com/ArcadeAI/agent-library)
- [Documentation — Auth Providers (40+)](https://docs.arcade.dev/home/auth-providers)
- [Documentation — Pre-built Tools (7,000+)](https://docs.arcade.dev/home/tools)
- [Documentation — Build Custom Tools](https://docs.arcade.dev/home/build-tools)
- [Documentation — MCP Gateways](https://docs.arcade.dev/guides/mcp-gateways)
- [Documentation — Audit Logs](https://docs.arcade.dev/guides/audit-logs)
- [Documentation — Contextual Access](https://docs.arcade.dev/guides/contextual-access)
- [Documentation — Deployment (Cloud / VPC / On-Prem / Air-Gapped)](https://docs.arcade.dev/guides/deployment)
- [Documentation — Security Program](https://docs.arcade.dev/home/security)
- [Documentation — Arcade Registry (Beta)](https://arcade.dev/registry)
- [Documentation — Model Context Protocol](https://modelcontextprotocol.io)
- [Forum — Discord](https://discord.gg/arcadedev)
- [X — TryArcade](https://x.com/TryArcade)

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Arcade Tools API](openapi/arcade-tools-api-openapi.yml)
- [Arcade Authorization API](openapi/arcade-auth-api-openapi.yml)
- [Arcade LLM API](openapi/arcade-llm-api-openapi.yml)
- [Arcade Workers API](openapi/arcade-workers-api-openapi.yml)
- [Arcade Gateways API](openapi/arcade-gateways-api-openapi.yml)
- [Arcade Hooks API](openapi/arcade-hooks-api-openapi.yml)
- [Arcade Admin API](openapi/arcade-admin-api-openapi.yml)
- [Arcade Plugins API](openapi/arcade-plugins-api-openapi.yml)
- [Arcade Operations API](openapi/arcade-operations-api-openapi.yml)

### JSON Schema

- [Arcade Tool](json-schema/arcade-tool-schema.json)
- [Arcade Tool Execution](json-schema/arcade-tool-execution-schema.json)
- [Arcade Authorization](json-schema/arcade-authorization-schema.json)
- [Arcade Worker](json-schema/arcade-worker-schema.json)
- [Arcade Hook](json-schema/arcade-hook-schema.json)

### JSON Structure

- [Arcade Tool](json-structure/arcade-tool-structure.json)
- [Arcade Authorization](json-structure/arcade-authorization-structure.json)
- [Arcade Worker](json-structure/arcade-worker-structure.json)

### JSON-LD

- [Arcade.dev Context](json-ld/arcade-dev-context.jsonld)

### Capabilities (Naftiko)

- [Tools](capabilities/tools-tools.yaml)
- [Authorization](capabilities/auth-auth.yaml)
- [LLM](capabilities/llm-llm.yaml)
- [Workers](capabilities/workers-workers.yaml)
- [Gateways](capabilities/gateways-gateways.yaml)
- [Hooks](capabilities/hooks-hooks.yaml)
- [Admin](capabilities/admin-admin.yaml)
- [Plugins](capabilities/plugins-plugins.yaml)
- [Operations](capabilities/operations-operations.yaml)

### Examples

- [Tools — List](examples/arcade-tools-list-example.json)
- [Tools — Execute](examples/arcade-tools-execute-example.json)
- [Tools — Authorize](examples/arcade-tools-authorize-example.json)
- [Auth — Authorize](examples/arcade-auth-authorize-example.json)
- [Auth — Status](examples/arcade-auth-status-example.json)
- [LLM — Chat Completion](examples/arcade-llm-chat-completions-example.json)
- [Workers — Create](examples/arcade-workers-create-example.json)
- [Gateways — Create](examples/arcade-gateways-create-example.json)
- [Hooks — Create](examples/arcade-hooks-create-example.json)
- [Admin — Set Secret](examples/arcade-admin-secrets-set-example.json)
- [Operations — Health](examples/arcade-operations-health-example.json)

### Rules

- [Spectral Ruleset](rules/arcade-dev-rules.yml)

### Vocabulary

- [Arcade.dev Vocabulary](vocabulary/arcade-dev-vocabulary.yml)

### Commercial artifacts

- [Plans / Pricing](plans/arcade-dev-plans-pricing.yml)
- [Rate Limits / Quotas](rate-limits/arcade-dev-rate-limits.yml)
- [FinOps Definition](finops/arcade-dev-finops.yml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
