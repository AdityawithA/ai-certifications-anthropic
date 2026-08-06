# Claude with Amazon Bedrock — Notes

**Course:** Anthropic Academy — *Claude with Amazon Bedrock*
**Track:** Developer / Cloud Platform Integration
**Audience:** Developers building production AI applications on AWS infrastructure
**Format:** Self-paced, technical, hands-on implementation patterns
**Status:** ✅ Completed

## What the Course Is About

This is a technical, developer-focused course on running Claude through **Amazon Bedrock** rather than Anthropic's direct API. The premise: building production AI applications requires more than just API access — you need infrastructure for retrieval, tool use, caching, and scale. Bedrock provides that managed infrastructure inside the AWS ecosystem, and this course walks through implementing Claude's capabilities specifically within that environment, from basic requests to full autonomous agent systems.

It overlaps conceptually with *Building with the Claude API*, but the focus here is Bedrock-specific: deployment, authentication, and AWS-native patterns rather than Anthropic's direct API surface.

## Key Concepts

### 1. Core API Implementation on Bedrock
- Utilizing Anthropic models on Bedrock for multi-turn conversations
- System prompt configuration within the Bedrock environment
- Building and evaluating prompts using Bedrock's tooling
- Authentication and setup differences compared to the direct Anthropic API

### 2. Tool Use / Function Calling
- Extending Claude with custom tools and functions inside a Bedrock-based application
- Function calling patterns, multi-turn tool interactions, and batch tool calling
- Leveraging built-in utilities available through the Bedrock integration

### 3. Retrieval-Augmented Generation (RAG)
- A full implementation guide for production RAG systems, covering:
  - Text chunking strategies
  - Embeddings
  - Hybrid search combining vector search with **BM25**
  - Multi-index architectures
  - Reranking
  - Contextual retrieval techniques
- Building conversational AI pipelines that combine retrieval with generation

### 4. Autonomous Agents
- Developing autonomous agents for tasks like code generation and debugging
- Applying **Claude Code** and **Computer Use** together as two tools in an agentic workflow — Claude Code for development workflows, Computer Use for automating UI interactions
- MCP (Model Context Protocol) integration patterns within an agent architecture: defining custom tools/resources and implementing MCP servers and clients in this context

### 5. Performance & Production Readiness
- Performance optimization techniques, including caching
- Scalable architecture design for real-world, production-grade applications
- Practical implementation patterns suited to AWS-hosted deployments specifically (vs. generic API usage)

## What I Learned

- Bedrock isn't just "the API on AWS" — it changes authentication, deployment, and some tooling patterns enough that it's worth a dedicated course rather than assuming the direct API course transfers 1:1.
- Production RAG is a much bigger topic than "embed and retrieve" — chunking strategy, hybrid search (vector + BM25), reranking, and contextual retrieval all materially affect answer quality, and they're separate design decisions.
- Tool use and autonomous agents build directly on the RAG and API foundations — an agent is really just a system that combines retrieval, tool calling, and iterative reasoning in a loop.
- Combining Claude Code and Computer Use in one agentic workflow was a useful reminder that "agent" isn't a single tool — it's often several capabilities (code editing, UI automation, retrieval, custom tools) composed together toward a task.
- Caching and scalable architecture aren't afterthoughts — they're treated as first-class parts of taking something from "working demo" to "production system" on AWS infrastructure.

## One-Line Takeaway
> Running Claude on Bedrock means designing for AWS-native deployment, retrieval, and scale from the start — the same core Claude capabilities (tool use, agents) but wired into production-grade AWS infrastructure.