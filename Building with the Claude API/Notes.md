# Building with the Claude API — Notes

**Course:** Anthropic Academy — *Building with the Claude API*
**Track:** Developer (flagship course)
**Format:** Comprehensive video course, 7 modules, 8+ hours — the longest course in the Anthropic Academy catalog
**Status:** ✅ Completed

## What the Course Is About

This is Anthropic's flagship developer course — the definitive, most comprehensive path for anyone building real applications with Claude's API. It covers the full spectrum: fundamental API operations, advanced prompting techniques, tool integration, retrieval systems, and the architectural patterns used to build production-grade agentic systems. By the end, the goal is being able to build applications ranging from simple chat interfaces to autonomous agents — not just make isolated API calls.

## Key Concepts (by Module)

### 1. API Fundamentals
- Setting up and authenticating with the Anthropic API, including API key management and secure request configuration
- Implementing single- and multi-turn conversations with proper message formatting and context handling
- Configuring system prompts and controlling model behavior via temperature, response streaming, and structured output formats
- Understanding tokens, model selection trade-offs, and core benchmarks like MMLU

### 2. Prompt Engineering
- Techniques for writing clear, effective prompts — strong opening instructions, XML tags for structuring mixed content, multishot examples
- Assistant message prefilling to steer response direction and format
- Stop sequences for controlling exactly where generation ends

### 3. Prompt Evaluation
- Building datasets (including AI-generated test cases) to test prompts systematically rather than eyeballing a couple of runs
- Using graders — code graders, model graders — to get objective, repeatable scores on prompt performance
- Treating "it worked when I tried it twice" as a red flag rather than a green light before shipping

### 4. Tool Use
- Extending Claude beyond its training data by giving it tools to call external functions and APIs
- Writing JSON schemas that clearly describe what a tool does and its parameters
- Handling multi-turn tool use, sequential tool calls, and batch tool calling within a single response

### 5. Retrieval-Augmented Generation (RAG)
- Chunking strategies for breaking large documents into searchable pieces
- Embeddings and vector databases for semantic search
- Hybrid search combining vector similarity with BM25 lexical search (useful for exact matches like IDs)
- Reranking and contextual retrieval for improving result quality in production RAG pipelines

### 6. Model Context Protocol (MCP)
- Understanding MCP as a standardized way to connect Claude to external tools/data without writing custom integration code for each one
- The three primitives — tools, resources, prompts — and building basic MCP servers/clients

### 7. Agentic Workflows and Architectural Patterns
- **Chaining** — passing output from one step as input to the next
- **Routing** — categorizing a request first, then directing it to a specialized path
- **Parallelization** — running independent sub-tasks concurrently and combining results
- **Evaluator-optimizer** — generating output, checking it against criteria, and improving it iteratively
- **Agents** — giving Claude a goal and tools, then letting it figure out the steps itself, including "environment inspection" (observing and understanding the results of its own actions)
- Extended thinking and prompt caching for improving accuracy and efficiency on complex, repeated, or high-volume tasks

## What I Learned

- This course is really the union of everything the smaller, focused courses (Claude Platform 101, Intro to MCP, etc.) cover individually — seeing it end-to-end made clear how each piece (prompting → evaluation → tools → RAG → MCP → agent patterns) builds on the last.
- Prompt evaluation is the piece most likely to get skipped in real projects, but it's what separates "worked when I tried it" from something that survives real user input — graders turn that into something measurable rather than a gut feeling.
- The agentic workflow patterns (chaining, routing, parallelization, evaluator-optimizer, full agents) gave me a vocabulary for something I'd been doing intuitively — most complex AI systems are really combinations of these five patterns, not one big undifferentiated "agent."
- RAG is a much deeper topic than "embed and search" — chunking strategy, hybrid search, and reranking are all separate levers that materially affect answer quality in a production system.
- Building tool-enabled systems, RAG pipelines, and autonomous agents as actual hands-on projects (rather than just watching) made the architectural patterns concrete instead of abstract.

## One-Line Takeaway
> Building with the Claude API is the full arc from a single request to a production agentic system — prompting, evaluation, tools, retrieval, MCP, and workflow patterns all compounding into applications that can act, not just answer.