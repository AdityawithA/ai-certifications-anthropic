# Introduction to Model Context Protocol — Notes

**Course:** Anthropic Academy — *Introduction to Model Context Protocol (MCP)*
**Track:** Developer / Engineering
**Format:** Self-paced, hands-on, build servers/clients from scratch in Python
**Status:** ✅ Completed

## What the Course Is About

MCP (Model Context Protocol) is an open standard from Anthropic that lets AI systems connect to external tools and data sources through one unified interface, instead of every integration being a custom one-off. The course teaches how to build both sides of that connection — an MCP server and an MCP client — from scratch, so you understand what's actually happening under the hood rather than just plugging in a pre-built connector.

## Key Concepts

### 1. Why MCP Exists
- Without a standard, every AI-to-tool integration needs its own custom schema and glue code
- MCP gives a structured, reliable, secure way for models to reach databases, APIs, files, and other systems through a common protocol
- Learn how MCP **clients** and MCP **servers** actually communicate with each other

### 2. The Three Core Primitives
- **Tools** — model-controlled actions the AI can invoke, like querying a database or making an API request
- **Resources** — application-controlled, read-only data the AI can pull in, like config files or documents
- **Prompts** — pre-defined instruction templates for common tasks (e.g., "review this code")

### 3. Building an MCP Server
- Setting up a Python project for an MCP server from scratch
- Defining tools the server exposes
- Testing and debugging the server using the **MCP Server Inspector** in the browser

### 4. Building an MCP Client
- Implementing a client that connects to a server
- Accessing resources and working with prompts through the client
- Integrating everything into a complete, working application

## What I Learned

- MCP separates *who controls what*: tools are things the model decides to call, resources are things the app decides to expose — that distinction shapes how you design an integration.
- Standardizing the tool/resource/prompt interface means you don't have to reinvent the wiring every time you connect Claude to a new system.
- Building a server and client from scratch (rather than just using a pre-built connector) made it much clearer what's actually happening in the request/response cycle.
- The Inspector tool is genuinely useful for debugging — you can see exactly what's being exposed and called before wiring it into a real application.

## One-Line Takeaway
> MCP turns "connect AI to this specific tool" into "expose this tool through a standard interface" — building one from scratch is the fastest way to understand why that distinction matters.