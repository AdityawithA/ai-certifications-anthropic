# Introduction to Subagents — Notes

**Course:** Anthropic Academy — *Introduction to Subagents*
**Track:** Developer / Claude Code (agentic track)
**Format:** Self-paced, hands-on within Claude Code
**Status:** ✅ Completed

## What the Course Is About

This course covers sub-agents in Claude Code — one of the most practical tools for getting more out of longer, more complex Claude Code sessions. As a Claude Code conversation grows (exploring a codebase, running multiple tasks, gathering lots of intermediate output), the main context window fills up with noise. Sub-agents solve this by letting you delegate a task to an isolated assistant that does its work in a *separate* context window and reports back only the relevant summary — keeping the main conversation clean and focused.

## Key Concepts

### 1. How Sub-Agents Work
- When Claude Code spins up a sub-agent, it opens a **separate context window** distinct from the main conversation
- Inputs flow into that isolated context, the sub-agent does its work there, and only a **summary** flows back to the main session
- This means the main conversation's context isn't polluted by every intermediate step, tool call, or exploration the sub-agent did along the way

### 2. Creating Custom Sub-Agents
- Sub-agents are built using the **`/agents`** command
- You can tailor a sub-agent to a specific workflow — examples given in the course include a **code reviewer** and a **documentation generator**
- Each sub-agent can be scoped to a narrow, well-defined job rather than being a general-purpose assistant

### 3. Designing Effective Sub-Agents
- **Structured output formats** — having the sub-agent return results in a consistent, predictable shape so the main session can use them reliably
- **Obstacle reporting** — designing sub-agents to clearly report when they hit a blocker, rather than silently failing or guessing
- **Limiting tool access** — scoping down which tools a sub-agent can use, so it stays focused on its specific job and doesn't take unintended actions

### 4. When to Use Sub-Agents (and When Not To)
- Practical guidance on where delegation genuinely helps — typically longer or more complex tasks where isolating context matters
- Common anti-patterns: over-delegating small tasks that don't need isolation, or using sub-agents where the overhead of spinning up a separate context outweighs the benefit

## What I Learned

- The core value of a sub-agent isn't parallelism — it's **context isolation**. Keeping exploratory noise out of the main session is what makes long Claude Code sessions stay effective.
- A sub-agent is only as reliable as its output contract — designing for structured output and clear obstacle reporting matters more than making the sub-agent "smart."
- Limiting tool access is a design choice, not just a safety measure — it keeps a sub-agent focused on exactly the job it was delegated.
- Delegation isn't free — it has real overhead, so the course's anti-pattern guidance (when *not* to use a sub-agent) is just as important as knowing how to build one.

## One-Line Takeaway
> Sub-agents earn their keep by isolating context, not by doing more — the skill is knowing which tasks are worth spinning off, and designing them to report back cleanly.