# Model Context Protocol: Advanced Topics — Notes

**Course:** Anthropic Academy — *Model Context Protocol: Advanced Topics*
**Track:** Developer / MCP (follow-on to Introduction to Model Context Protocol)
**Prerequisite:** Introduction to Model Context Protocol
**Format:** Self-paced, ~3 hours, ends in an assessment and certificate
**Status:** ✅ Completed

## What the Course Is About

Where the introductory MCP course covers the three core primitives (tools, resources, prompts) and building a basic server/client from scratch, this course goes deeper into the parts of MCP that make servers genuinely production-capable: sampling, notifications, roots (secure file system access), and the technical realities of different transport mechanisms. It's aimed at developers who already understand MCP's basics and want to build servers that are more capable, responsive, and deployable beyond local development.

## Key Concepts

### 1. Sampling
- Lets an MCP **server** request a completion from a language model *through the client* — effectively giving the server access to AI capabilities without the server needing its own model integration
- Useful for servers that need some AI reasoning as part of their own logic, without duplicating model access separately

### 2. Notifications
- A mechanism for servers to provide **real-time feedback** to clients as work happens, rather than the client only getting a response once everything is finished
- Makes long-running server operations feel responsive instead of opaque

### 3. Roots
- A way for MCP servers to securely access parts of the **file system**, with boundaries set by the client/user rather than the server having unrestricted access
- Balances giving a server real filesystem capability against keeping that access scoped and safe

### 4. MCP's Communication Layer
- Understanding the underlying **JSON message types** that make up MCP's protocol
- **stdio transport** — the standard approach for local development, where client and server communicate over standard input/output on the same machine
- **StreamableHTTP** — the more complex transport used for remote deployments, where client and server aren't running on the same machine
- Understanding the trade-offs and added complexity that come with moving from local (stdio) to remote (StreamableHTTP) deployments

## What I Learned

- Sampling is a clever inversion of the usual model — instead of the *client* always being the one with AI access, a server can borrow reasoning capability through the client via sampling, which opens up more sophisticated server-side logic.
- Notifications matter more than they initially seem to — for anything long-running, silence until a final response feels broken even if the server is working correctly; real-time feedback is a UX requirement, not a nice-to-have.
- Roots is a good example of security-by-design in MCP — servers get real filesystem power, but the boundaries are set outside the server's own control, which is a meaningfully safer default than trusting the server to self-limit.
- The jump from stdio to StreamableHTTP is where MCP servers actually become "production" — local development hides a lot of complexity (network reliability, streaming, remote auth) that only shows up once you deploy remotely.

## One-Line Takeaway
> Advanced MCP is about making servers production-ready — sampling for borrowed AI reasoning, notifications for responsiveness, roots for safe filesystem access, and StreamableHTTP for the jump from local to remote deployment.