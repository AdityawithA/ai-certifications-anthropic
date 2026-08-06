# Claude Platform 101 — Notes

**Course:** Anthropic Academy — *Claude Platform 101*
**Track:** Developer / Engineering
**Format:** Self-paced, hands-on with the Claude API and Console
**Status:** ✅ Completed

## What the Course Is About

This course marks the jump from *chatting* with Claude to *building* with Claude. There's a real gap between the two: a chat answers a question and the thread ends there, while an application sends Claude structured requests, gives it tools, lets it act on real systems, and runs that loop for one user or a million. Claude Platform 101 teaches that gap from first principles — what's actually inside an API request, how an agent decides what to do, how the context window bounds what Claude can see, and how tools and permissions control what it's allowed to touch.

## Key Concepts

### 1. The Basics of an API Request
- Sending your first request to Claude and reading the raw response (not the chat UI abstraction)
- Choosing between models (Opus, Sonnet, Haiku) based on the actual job — not just picking the "best" one, but weighing cost and latency trade-offs for the specific task

### 2. The Agent Loop
- Building an agent loop by hand: Claude acts, observes the result, and decides the next step
- Understanding this manually first, then seeing how the SDK's **Tool Runner** automates that same loop once you know what it's actually doing under the hood

### 3. Giving Claude Reach
- **Tool use** — letting Claude call functions/tools to act beyond just generating text
- **Extended thinking** — letting Claude reason through harder problems before responding
- **Anthropic's built-in tools** — web search, code execution, and web fetch, which run on Anthropic's own infrastructure rather than your own

### 4. Scaling and Reuse
- **Skills** — packaging a procedure once and reusing it across many calls instead of re-explaining it every time
- **MCP servers** — connecting Claude to third-party tools without having to hand-write a schema for each one
- **Context management** — patterns for keeping a long-running agent inside the context window and cost-effective over time

### 5. Keeping Spend Predictable
- Workspaces and usage limits in the Console
- Using the **Console Workbench** to test and tune requests before shipping them

## What I Learned

- Prompting well and *building* well are different skills — the platform layer is about structure, control, and cost, not just wording a good prompt.
- An "agent" isn't magic — it's a loop of act → observe → decide, and the SDK tooling just automates a pattern you can build by hand.
- Model choice is a real engineering decision (cost/latency/quality trade-off), not just "use the smartest one."
- Scaling an agent responsibly means thinking about context window limits and spend from the start, not bolting them on later.

## One-Line Takeaway
> Building on the Claude Platform means designing the loop — requests, tools, context, and cost — not just writing a good prompt.