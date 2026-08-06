# Quiz Answers — Claude Code in Action

**Question 1:** You can describe exactly what "done" looks like for a task (all tests in a package pass, the type checker reports zero errors) better than you can list the steps to get there. Which approach fits best?
- ❌ Run the task in plan mode and read the plan
- ✅ Use `/goal` to set a completion condition so Claude keeps working until a fast evaluator confirms it
- ❌ Use loop to re-run the prompt on a fixed interval
- ❌ Use `/compact` with instructions so the summary keeps what matters

---

**Question 2:** Your team has a hard rule: never push to main. Where should it live so Claude cannot skip it?
- ❌ In the project CLAUDE.md as an "IMPORTANT" rule
- ❌ In the local CLAUDE.md so it is scoped to you
- ✅ In a pre-tool use hook that stops the push
- ❌ In a skill's reference.md file

---

**Question 3:** You have typed the same multi-step procedure to Claude more than once, and it includes long reference material and a helper script. How should you package it?
- ❌ Paste the whole procedure into CLAUDE.md so it always loads
- ✅ Make a skill, keep skill.md lean, and push depth into reference.md and scripts Claude runs when needed
- ❌ Put every step and the full reference inline in skill.md so nothing is missed
- ❌ Add it as an org-level managed policy

---

**Question 4:** You ask Claude in auto mode to refactor authentication and it writes broken authentication. What actually happens, and what should you add?
- ❌ The classifier blocks it because broken code is dangerous; nothing more needed
- ✅ The classifier waves it through because broken is not dangerous; pair auto mode with a stop hook that runs your tests
- ❌ Bypass permissions would have caught it; switch to that mode
- ❌ Plan mode would have caught it; switch to that mode

---

**Question 5:** You want a dependency audit to run every morning at 9am with no machine of yours staying on and no workflow file to maintain. Which tool fits?
- ❌ A headless `-p` run you trigger manually
- ❌ The Agent SDK embedded in your own application
- ✅ A routine that runs on Anthropic infrastructure on a cron trigger
- ❌ A bypass-permissions session left running overnight

---

**Question 6:** Your team wants Claude to review every pull request with inline comments and nothing to build or host, and you do not need it to approve or block the PR. Which option fits?
- ❌ The Claude Code GitHub action with a custom workflow
- ✅ Managed code review through the Claude GitHub app
- ❌ A headless `-p` run triggered by a webhook you maintain
- ❌ The `/code-review --fix` command run locally on each PR

---

**Question 7:** A job ran unattended in CI and reports success. What is the most reliable first move before you ship it?
- ❌ Read Claude's summary of the run and trust the passing claim
- ✅ Start from the diff itself and `git diff`, and confirm tests actually passed rather than were claimed
- ❌ Re-run the same prompt and compare summaries
- ❌ Switch the run to bypass permissions and run it again

---

**Question 8:** A community plugin gives you a skill you want. What should you do before enabling it?
- ❌ Install it; plugins cannot change how Claude Code behaves by default
- ❌ Install it if it passed automated review, since reviewed means trusted
- ✅ Inspect every hook, agent, and MCP server it adds, because a plugin runs code with your privileges and its hooks fire on every matching call
- ❌ Rely on namespacing, since a plugin cannot ship a settings.json