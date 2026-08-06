# Claude Code 101 — Notes

**Course:** Anthropic Academy — *Claude Code 101*
**Track:** Developer (coding agent track)
**Audience:** New developers learning AI-assisted workflows from the start, and experienced engineers who haven't tried a coding agent yet
**Format:** Self-paced, installation through advanced customization
**Status:** ✅ Completed

## What the Course Is About

Claude Code 101 is the entry point into Anthropic's coding-agent track. Unlike Claude 101 (chat-based everyday use) or Claude Platform 101 (building with the API), this course is specifically about **Claude Code** — an agentic coding tool that works directly in your terminal/IDE on real codebases, not just answering isolated coding questions. It's built for two audiences at once: developers new to software engineering who want to learn AI-assisted workflows from day one, and experienced engineers who haven't yet tried a coding agent.

## Key Concepts

### 1. Getting Set Up
- Installing Claude Code and getting it running in your environment
- Understanding what makes it different from a regular chat interface — it can read, navigate, and modify a real codebase, run commands, and iterate

### 2. The Explore → Plan → Code → Commit Workflow
The course's core teaching model for using a coding agent well:
- **Explore** — let Claude Code look at and understand the relevant parts of the codebase first, before making changes
- **Plan** — have it lay out an approach before writing code, so you can review the plan rather than untangle a finished (possibly wrong) change
- **Code** — Claude Code implements the plan, making the actual edits
- **Commit** — review, refine, and commit the working change, treating the agent's output like a teammate's PR, not a black box

### 3. Everyday Development Workflow
- Using Claude Code for real day-to-day tasks — debugging, refactoring, writing tests, exploring unfamiliar code
- Working with it inside an existing project rather than toy examples

### 4. Advanced Customization
- Tailoring Claude Code's behavior and configuration to fit your specific workflow and project conventions
- Setting up the tool so it works well repeatedly, not just for a single one-off task

## What I Learned

- The Explore-Plan-Code-Commit structure is the main mental model to take away — resisting the urge to let the agent jump straight to writing code without first exploring context and proposing a plan leads to much better results.
- Treating Claude Code's output like a colleague's pull request (review before merging) rather than a finished product is the right posture — the workflow builds in a checkpoint for that.
- A coding agent is most valuable on real, messy codebases — understanding existing code, not just generating new code from scratch.
- This course sets the foundation that the follow-on courses (Claude Code in Action, Introduction to Agent Skills, Introduction to Subagents) build on, so it's meant to be the starting point of the developer/agentic track, not a standalone deep dive.

## One-Line Takeaway
> Claude Code works best when you follow Explore → Plan → Code → Commit — letting the agent understand and propose before it edits, and treating its output like a PR to review, not a finished product.