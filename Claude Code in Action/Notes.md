# Claude Code in Action — Notes

**Course:** Anthropic Academy — *Claude Code in Action*
**Track:** Developer / Claude Code (agentic track, follow-on to Claude Code 101)
**Audience:** Developers who already use Claude Code for single prompts and want to move to longer, less-supervised, team-wide workflows
**Format:** Self-paced, hands-on, ends in an assessment and certificate
**Status:** ✅ Completed

## What the Course Is About

Where Claude Code 101 is the on-ramp (installation, the basic Explore-Plan-Code-Commit loop), Claude Code in Action is about running **long, hands-off Claude Code sessions you can actually trust** — not just using it prompt-by-prompt, but steering, configuring, automating, and verifying it as part of a real team workflow. The course covers how Claude Code reads files, executes commands, and modifies code through its tool system, then builds up from there into managing context, custom workflows, hooks, and integrations with external services.

## Key Concepts

### 1. Steer the Work
- Scoping work with **plan mode** before letting Claude Code start making changes
- Directing **compaction** so that when context gets summarized, the summary keeps what actually matters
- Using the **rewind menu** to course-correct mid-session instead of starting over
- Choosing between **hands-on steering** (staying closely involved) and **autonomous goal/loop runs** (letting Claude Code work toward a goal with less supervision)

### 2. Configure Claude
- Writing a lean **CLAUDE.md** that Claude actually follows — concise project context and conventions rather than a bloated file that gets ignored
- Packaging repeated procedures as **skills** so they're reusable instead of re-explained every session
- Picking the right **permission mode** for each job — balancing autonomy against risk depending on the task
- Enforcing **non-negotiable rules with hooks** — hard constraints that don't rely on Claude simply "remembering" instructions

### 3. Automate Repeat Work
- Scheduling prompts as **routines** that run on Anthropic's own infrastructure, rather than manually kicking off every session
- Dropping to **headless mode** when a job needs to run inside your own custom pipeline
- Wiring Claude Code into **pull requests** — managed code review and the official GitHub Action for automated PR workflows

### 4. Verify and Share
- Verifying unsupervised runs **in proportion to how little you watched them** — the less oversight during the run, the more scrutiny the output deserves afterward
- Gating turns on **real test results using hooks**, so Claude Code can't claim success without actually passing tests
- Packaging a trusted setup as a **plugin** the whole team can install, turning your working configuration into something reusable across the team

## What I Learned

- The shift from Claude Code 101 to this course is really a shift from "using a tool" to "operating a system" — plan mode, compaction, and the rewind menu all exist to make longer, less-supervised sessions safe to run.
- CLAUDE.md is easy to over-stuff — the course's framing of "lean enough that Claude actually follows it" was a useful corrective versus dumping every project detail into it.
- Hooks matter because they turn soft instructions into hard constraints — anything that truly can't be skipped belongs in a hook, not just a written rule Claude is expected to remember.
- Verification effort should scale inversely with supervision — the less I'm watching a run live, the more I need to check afterward, especially before merging or shipping.
- Turning a working setup into a shareable plugin is the endpoint of the course's philosophy: personal Claude Code proficiency isn't the goal, a *trustable team-wide workflow* is.

## One-Line Takeaway
> Claude Code in Action is about earning the ability to run long, unsupervised sessions — by steering with plan mode and rewind, configuring lean context and hard hooks, automating repeat work safely, and verifying in proportion to how little you watched.