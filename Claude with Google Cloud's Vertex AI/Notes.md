# Claude with Google Cloud's Vertex AI — Notes

**Course:** Anthropic Academy — *Claude with Google Cloud's Vertex AI*
**Track:** Developer / Cloud Platform Integration
**Prerequisites:** Python, experience with Google Cloud Platform, and comfort working with JSON
**Audience:** Developers/teams already inside the Google Cloud ecosystem who want to add Claude to their stack
**Format:** Self-paced, technical, hands-on implementation
**Status:** ✅ Completed

## What the Course Is About

This is the Google Cloud counterpart to *Claude with Amazon Bedrock* — comprehensive technical training on integrating and deploying Claude models through **Vertex AI**, Google Cloud's managed AI platform. It covers the full spectrum of working with Anthropic's models on Vertex AI: basic request handling through advanced features like tool use, RAG, and MCP, plus deploying Anthropic's own apps (Claude Code, Computer Use) and designing multi-step agent workflows — all within the GCP environment specifically.

## Key Concepts

### 1. Core API Implementation on Vertex AI
- Implementing Claude's API capabilities on Vertex AI, from basic request handling up
- Authentication and setup specific to Google Cloud (distinct from the direct Anthropic API or Bedrock)
- Working within GCP's project/IAM structure rather than Anthropic's own account system

### 2. Advanced Capabilities
- **Tool use** — extending Claude with custom functions inside a Vertex AI-based application
- **Retrieval-Augmented Generation (RAG)** — building retrieval-backed applications on GCP infrastructure
- **Model Context Protocol (MCP)** — integrating MCP-based tool/resource access within this deployment context

### 3. Deploying Anthropic Apps on Vertex AI
- **Claude Code** — configuring and deploying it for automated development tasks within a GCP-based workflow
- **Computer Use** — deploying it for UI automation tasks

### 4. Agent-Based Workflow Design
- Designing multi-step agent workflows using established patterns:
  - **Parallelization** — running independent sub-tasks concurrently
  - **Chaining** — passing output from one step as input to the next
  - **Routing** — directing a request to the right specialized path based on its content
- Applying these patterns to build more complex, production-grade AI systems rather than single-shot API calls

## What I Learned

- Vertex AI isn't just "the API on GCP" — like Bedrock, it changes authentication and deployment enough to warrant its own dedicated course rather than assuming the direct API course transfers cleanly.
- The agent-workflow patterns (parallelization, chaining, routing) are a genuinely useful vocabulary for structuring complex AI systems — most "agent" behavior in production breaks down into some combination of these three patterns rather than being one big autonomous loop.
- Deploying Claude Code and Computer Use specifically *through* Vertex AI (rather than directly via Anthropic) matters for teams whose infrastructure, billing, and compliance already live in the Google Cloud ecosystem.
- This course closely mirrors the Bedrock course in scope (tool use, RAG, MCP, agents) — the real differentiator is the deployment platform and its authentication/infrastructure model, not the underlying Claude capabilities.

## One-Line Takeaway
> Running Claude on Vertex AI means the same core capabilities as the direct API — tool use, RAG, MCP, agents — but wired into GCP's authentication, infrastructure, and agent-workflow patterns (parallelization, chaining, routing) for teams already living in that ecosystem.