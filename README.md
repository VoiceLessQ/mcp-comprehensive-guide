# Model Context Protocol (MCP) - Comprehensive Guide (April 2025)

---

## Overview

**Model Context Protocol (MCP)** is an open protocol published by **Anthropic** in November 2024. It standardizes how Large Language Models (LLMs) connect to external data sources and tools, enabling seamless integration and powerful agent workflows.

Think of MCP as a **universal USB-C port for AI**: a standardized way to plug LLMs into files, APIs, databases, cloud services, and more.

---

## Why MCP?

- **Build complex agents and workflows** on top of LLMs.
- **Switch between LLM providers** easily.
- **Securely access data** within your infrastructure.
- **Leverage a growing ecosystem** of pre-built integrations.

---

## Architecture

MCP follows a **client-server model**:

- **MCP Hosts**: Apps like [Claude Desktop](https://www.anthropic.com/claude-desktop), IDEs, or AI tools.
- **MCP Clients**: Protocol connectors managing server connections.
- **MCP Servers**: Lightweight programs exposing data and tools.
- **Local Data Sources**: Files, databases, services on your machine.
- **Remote Services**: APIs, cloud services.

### Diagram

```
Host (Claude, IDEs)
  <--> MCP Server A <--> Local Data A
  <--> MCP Server B <--> Local Data B
  <--> MCP Server C <--> Remote Service C (API)
```

---

## Core Concepts

- **Resources**: Data exposed by servers (files, DB records, API responses).
- **Tools**: Executable functions (actions, API calls).
- **Prompts**: Templates and workflows for LLMs.
- **Sampling**: Servers can request completions from LLMs.
- **Transports**: Communication methods (stdio, WebSocket, HTTP).
- **Roots**: Context roots for managing data scope.

---

## Ecosystem

### Servers

- **Official**:
  - [GitHub MCP](https://github.com/modelcontextprotocol/server-github)
  - [GitLab MCP](https://github.com/modelcontextprotocol/server-gitlab)
  - [Google Drive MCP](https://github.com/modelcontextprotocol/server-googledrive)
  - [Slack MCP](https://github.com/modelcontextprotocol/server-slack)
  - [PostgreSQL MCP](https://github.com/modelcontextprotocol/server-postgresql)
  - [SQLite MCP](https://github.com/modelcontextprotocol/server-sqlite)
  - [Memory MCP](https://github.com/modelcontextprotocol/server-memory)
  - [Puppeteer MCP](https://github.com/modelcontextprotocol/server-puppeteer)
  - [Brave Search MCP](https://github.com/modelcontextprotocol/server-bravesearch)
  - [Google Maps MCP](https://github.com/modelcontextprotocol/server-googlemaps)
  - [AWS KB MCP](https://github.com/modelcontextprotocol/server-awskb)
  - [Fetch MCP](https://github.com/modelcontextprotocol/server-fetch)
  - [Sentry MCP](https://github.com/modelcontextprotocol/server-sentry)
- **Community**: Cloudflare, Raygun, Kagi, Exa.ai, YouTube, AppleScript, Make, VSCode Devtools, Node.js Debugger, OpenAI, Phabricator, Obsidian, ZenML, Blender, WhatsApp, Firebase, Raindrop.io, Neovim, Xero, GraphQL, Windows CLI, and many more.

### SDKs

- **Official**:
  - [Python SDK](https://github.com/modelcontextprotocol/python-sdk)
  - [TypeScript SDK](https://github.com/modelcontextprotocol/typescript-sdk)
  - [Java SDK](https://github.com/modelcontextprotocol/java-sdk)
  - [Kotlin SDK](https://github.com/modelcontextprotocol/kotlin-sdk)
  - [C# SDK](https://github.com/modelcontextprotocol/csharp-sdk)
- **Community**:
  - Rust (WIP)
  - Go (WIP)

### Tools

- [Server Inspector](https://github.com/modelcontextprotocol/inspector) (visual testing)
- CLI managers
- Installers
- Agent frameworks (e.g., [LangChain integration](https://python.langchain.com/docs/integrations/mcp))
- Desktop marketplaces

### Clients

- [Claude Desktop](https://www.anthropic.com/claude-desktop)
- [n8n workflows](https://n8n.io)
- Custom apps

---

## Tutorials & Resources

- [Official Website](https://modelcontextprotocol.io)
- [Protocol Specification](https://spec.modelcontextprotocol.io)
- [Awesome-MCP Curated List](https://github.com/AlexMili/Awesome-MCP)
- [Workshop Video (2hr)](https://www.youtube.com/watch?v=kQmXtrmQ5Zg)
- Quickstarts for server/client/users
- Debugging guides
- Inspector tool
- LLM-assisted development tutorials

---

## Known Issues (April 2025)

| Issue | Status | Fix/Notes |
|--------|---------|-----------|
| Slack MCP returns `invalid_auth` | Open | Check token scopes/config |
| Swift SDK namespace clashes (`MCP`, `Notification`) | Open | Rename enum/protocol suggested |
| Swift SDK package name too generic | Open | Rename to `mcp-swift-sdk` suggested |
| Python SDK `ClientSession.initialize` hangs if server exits | Open | Should raise exception |
| .NET client pipe closed error | Open | Likely server crash/misconfig |
| Google Drive MCP path bug (double `C:\C:\`) | Open | Path concatenation bug, manual fix |
| OAuth spec confusion (CLIENT_SECRET + PKCE) | Open | Clarify docs |
| Swift SDK `listTools` pagination info missing | Open | API consistency fix suggested |

---

## Community Feedback

- No major complaints on Reddit.
- Mostly tutorials, integrations, and questions.
- Active development and positive sentiment.

---

## Summary

MCP is a **powerful, open, and extensible protocol** that connects LLMs to the real world. It has a **rich ecosystem**, clear architecture, and is **rapidly evolving** with community support.

---

## Contributing

- [MCP GitHub Organization](https://github.com/modelcontextprotocol)
- [Specification Discussions](https://github.com/modelcontextprotocol/specification/discussions)
- [Organization Discussions](https://github.com/orgs/modelcontextprotocol/discussions)
- [Contributing Guide](https://modelcontextprotocol.io/development/contributing)

---

_Last updated: April 4, 2025_