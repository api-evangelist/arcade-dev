# arcade-dev (arcade-dev)

Arcade.dev (formerly Arcade AI) is the MCP runtime for production AI agents — a platform that lets agents safely take real-world actions across SaaS apps with per-user authorization, governed tool execution, and audit logging. The Arcade Engine exposes a Tools API for listing / authorizing / executing agent tools, an Authorization API that brokers OAuth and API-key grants across 40+ providers, an OpenAI-compatible LLM endpoint, Workers and MCP Gateways for routing, Hooks for governance, and an Admin API for control-plane configuration. Arcade ships with 7,000+ pre-built integrations across Google, Microsoft, Slack, GitHub, Salesforce, HubSpot, and more, plus an MCP server framework (arcade-mcp) and SDKs in Python, TypeScript, Go, Java/Kotlin, and .NET. Available as Arcade Cloud, VPC, on-prem, or air-gapped.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/arcade-dev/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/arcade-dev/refs/heads/main/apis.yml)

## Scope

- **Position:** Producing

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### Arcade Tools API

List, inspect, authorize, execute, and schedule Arcade tools. Tools are user-scoped agent actions addressed by fully qualified name (Toolkit.Name@version) and executed against a stable user_id with Arcade-managed authorization tokens.

- **Human URL:** [https://docs.arcade.dev/references/api](https://docs.arcade.dev/references/api)

#### Tags

- Tools
- Agents
- AI
- Execution

#### Properties

- [Documentation](https://docs.arcade.dev/home/tools)
- [OpenAPI](openapi/arcade-tools-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arcade-tools-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arcade-tools-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/arcade-tool-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/arcade-tool-execution-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/arcade-tool-structure.json)
- [Example](examples/arcade-tools-list-example.json)
- [Example](examples/arcade-tools-execute-example.json)
- [Example](examples/arcade-tools-authorize-example.json)

### Arcade Authorization API

Authorize end-users against 40+ identity providers (Google, Microsoft, Slack, GitHub, Salesforce, HubSpot, and more). Issue user-scoped grants, poll authorization status, and confirm users so agents can call tools as the end-user rather than a shared service account.

- **Human URL:** [https://docs.arcade.dev/home/auth](https://docs.arcade.dev/home/auth)

#### Tags

- Authorization
- OAuth
- Identity
- Agents

#### Properties

- [Documentation](https://docs.arcade.dev/home/auth)
- [OpenAPI](openapi/arcade-auth-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arcade-auth-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arcade-auth-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/arcade-authorization-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/arcade-authorization-structure.json)
- [Example](examples/arcade-auth-authorize-example.json)
- [Example](examples/arcade-auth-status-example.json)

### Arcade LLM API

OpenAI-compatible chat completions endpoint that lets agents call LLMs through Arcade with tools attached. The engine handles tool selection, end-user authorization, and tool execution so agents need only speak the OpenAI Chat Completions protocol.

- **Human URL:** [https://docs.arcade.dev/home/chat-overview](https://docs.arcade.dev/home/chat-overview)

#### Tags

- LLM
- AI
- Chat
- OpenAI Compatible

#### Properties

- [Documentation](https://docs.arcade.dev/home/chat-overview)
- [OpenAPI](openapi/arcade-llm-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arcade-llm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arcade-llm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/arcade-llm-chat-completions-example.json)

### Arcade Workers API

Register, manage, health-check, and authorize workers that host Arcade toolkits or MCP servers behind the Arcade Engine. Self-hosted workers let customers keep tool execution (and end-user tokens) inside their own perimeter.

- **Human URL:** [https://docs.arcade.dev/home/workers](https://docs.arcade.dev/home/workers)

#### Tags

- Workers
- MCP
- Infrastructure
- Agents

#### Properties

- [Documentation](https://docs.arcade.dev/home/workers)
- [OpenAPI](openapi/arcade-workers-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arcade-workers-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arcade-workers-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/arcade-worker-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/arcade-worker-structure.json)
- [Example](examples/arcade-workers-create-example.json)

### Arcade Gateways API

Create and manage MCP gateways scoped to organizations and projects. Gateways expose curated tool catalogs to MCP clients (Cursor, Claude Desktop, Claude Code, VS Code, Microsoft Copilot Studio, GitHub Copilot).

- **Human URL:** [https://docs.arcade.dev/guides/mcp-gateways](https://docs.arcade.dev/guides/mcp-gateways)

#### Tags

- Gateways
- MCP
- Agents

#### Properties

- [Documentation](https://docs.arcade.dev/guides/mcp-gateways)
- [OpenAPI](openapi/arcade-gateways-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arcade-gateways-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arcade-gateways-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/arcade-gateways-create-example.json)

### Arcade Hooks API

Manage lifecycle hooks that fire on tool authorization, tool execution, worker health, and audit events. Hooks are the primary integration point for SIEM forwarding, audit logging, and downstream governance pipelines.

- **Human URL:** [https://docs.arcade.dev/guides/audit-logs](https://docs.arcade.dev/guides/audit-logs)

#### Tags

- Hooks
- Webhooks
- Events
- Agents

#### Properties

- [Documentation](https://docs.arcade.dev/guides/audit-logs)
- [OpenAPI](openapi/arcade-hooks-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arcade-hooks-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arcade-hooks-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/arcade-hook-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [Example](examples/arcade-hooks-create-example.json)

### Arcade Admin API

Administer Arcade auth providers, organization secrets, user connections, and session verification settings. The control plane behind tool authorization and end-user identity.

- **Human URL:** [https://docs.arcade.dev/references/api](https://docs.arcade.dev/references/api)

#### Tags

- Administrative
- Secrets
- Identity
- Agents

#### Properties

- [Documentation](https://docs.arcade.dev/home/auth-providers)
- [OpenAPI](openapi/arcade-admin-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arcade-admin-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arcade-admin-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/arcade-admin-secrets-set-example.json)

### Arcade Plugins API

Manage plugins that extend the Arcade Engine with custom auth providers, transformers, and tool sources. Plugins let teams bring their own integrations behind the Arcade governance and auth layer.

- **Human URL:** [https://docs.arcade.dev/references/api](https://docs.arcade.dev/references/api)

#### Tags

- Plugins
- Agents
- Extensibility

#### Properties

- [OpenAPI](openapi/arcade-plugins-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arcade-plugins-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arcade-plugins-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Arcade Operations API

Operational endpoints exposing service health, engine runtime configuration, and the OpenAPI / swagger description of the Arcade Engine.

- **Human URL:** [https://docs.arcade.dev/references/api](https://docs.arcade.dev/references/api)

#### Tags

- Operations
- Health
- Configuration

#### Properties

- [OpenAPI](openapi/arcade-operations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/arcade-operations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/arcade-operations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Example](examples/arcade-operations-health-example.json)

## Common Properties

- [Portal](https://arcade.dev)
- [Documentation](https://docs.arcade.dev)
- [Getting Started](https://docs.arcade.dev/home)
- [Sign Up](https://api.arcade.dev/dashboard/auth/login)
- [Pricing](https://arcade.dev/pricing)
- [Blog](https://arcade.dev/blog)
- [Changelog](https://docs.arcade.dev/home/release-notes)
- [GitHub Organization](https://github.com/ArcadeAI)
- [SDK](https://github.com/ArcadeAI/arcade-py)
- [SDK](https://github.com/ArcadeAI/arcade-js)
- [SDK](https://github.com/ArcadeAI/arcade-go)
- [SDK](https://github.com/ArcadeAI/arcade-java)
- [SDK](https://github.com/ArcadeAI/arcade-dotnet)
- [SDK](https://github.com/ArcadeAI/arcade-mcp)
- [Code Examples](https://github.com/ArcadeAI/agent-templates)
- [Tool](https://github.com/ArcadeAI/blueprint-mcp)
- [Tool](https://github.com/ArcadeAI/agent-library)
- [Code Examples](https://github.com/ArcadeAI/safeword)
- [Documentation](https://github.com/ArcadeAI/docs)
- [Documentation](https://modelcontextprotocol.io)
- [Documentation](https://docs.arcade.dev/references/api)
- [SDK](https://docs.arcade.dev/home/install/cli)
- [Documentation](https://docs.arcade.dev/home/auth-providers)
- [Documentation](https://docs.arcade.dev/home/tools)
- [Documentation](https://docs.arcade.dev/home/build-tools)
- [Documentation](https://docs.arcade.dev/guides/mcp-gateways)
- [Documentation](https://docs.arcade.dev/guides/audit-logs)
- [Documentation](https://docs.arcade.dev/guides/contextual-access)
- [Documentation](https://docs.arcade.dev/guides/deployment)
- [Documentation](https://docs.arcade.dev/home/security)
- [Documentation](https://arcade.dev/registry)
- [Forum](https://discord.gg/arcadedev)
- [X (Twitter)](https://x.com/TryArcade)
- [Plans](plans/arcade-dev-plans-pricing.yml)
- [Rate Limits](rate-limits/arcade-dev-rate-limits.yml)
- [Fin Ops](finops/arcade-dev-finops.yml)
- [Spectral Rules](rules/arcade-dev-rules.yml)
- [JSON-LD](json-ld/arcade-dev-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Vocabulary](vocabulary/arcade-dev-vocabulary.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
