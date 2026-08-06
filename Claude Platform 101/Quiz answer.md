# Quiz Answers — Claude Platform 101

**Question 1:** Which three parameters does the `messages.create` call itself require?
- ❌ A model, a system prompt, and an API key
- ✅ A model, a max tokens limit, and a list of messages
- ❌ A system prompt, a temperature, and a list of messages
- ❌ An API key, a workspace, and a max tokens limit

---

**Question 2:** When Claude decides to use a tool, who actually executes it?
- ❌ Claude runs it inside the model during the response
- ❌ Anthropic runs it on their servers automatically
- ✅ Your code runs it and sends the result back
- ❌ The SDK blocks the request until a human approves it

---

**Question 3:** Why does context management matter for long-running agents?
- ❌ Claude refuses requests that use more than half the window
- ❌ Old messages are deleted automatically after ten turns
- ✅ The window is finite and you pay for what's in it — so the goal is fitting the right things in
- ❌ Bigger contexts always improve quality, so you want them full

---

**Question 4:** Which jobs are the best fit for a managed agent?
- ❌ Single questions that need one fast answer
- ✅ Long-running, sandboxed, or background work
- ❌ High-volume classification at the lowest cost
- ❌ Anything where you need to inspect every tool call yourself

---

**Question 5:** In Claude Code, which slash command invokes the built-in skill for working with the Claude API?
- ❌ `/anthropic-api`
- ❌ `/claude-sdk`
- ✅ `/claude-api`
- ❌ `/api-tools`

