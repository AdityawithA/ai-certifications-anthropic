# Quiz Answers — Model Context Protocol: Advanced Topics

**Question 1:** Your MCP server needs to use Claude to summarize data, but you don't want the server to handle API costs. What feature should you use?
- ❌ Roots
- ❌ Progress notifications
- ❌ Logging
- ✅ Sampling

---

**Question 2:** Your MCP tool sends a "Call Tool Request" and expects to get back results. What type of message pattern is this?
- ❌ Progress message
- ❌ Notification message
- ✅ Request-result message
- ❌ Logging message

---

**Question 3:** Your StreamableHTTP server needs to send progress updates to clients, but HTTP doesn't normally allow server-initiated requests. How does StreamableHTTP solve this?
- ✅ It creates Server-Sent Events (SSE) connections
- ❌ It stores messages in a database
- ❌ It uses WebSockets instead
- ❌ It switches to stdio transport

---

**Question 4:** A user asks Claude to "convert video.mp4" but Claude doesn't know where the file is located. What MCP feature helps solve this?
- ✅ Roots
- ❌ Progress notifications
- ❌ JSON messages
- ❌ Sampling

---

**Question 5:** You want simpler HTTP responses without streaming, just getting the final result as plain JSON. Which flag should you enable?
- ❌ `streaming=False`
- ❌ `simple_mode=True`
- ❌ `stateless_http=True`
- ✅ `json_response=True`

---

**Question 6:** You're developing an MCP server locally and want the simplest way to test communication between client and server on the same machine. Which transport should you use?
- ❌ HTTP transport
- ❌ WebSocket transport
- ❌ StreamableHTTP transport
- ✅ Stdio transport

---

**Question 7:** Which transport method requires both client and server to run on the same machine?
- ❌ TCP transport
- ✅ Stdio transport
- ❌ WebSocket transport
- ❌ HTTP transport

---

**Question 8:** What are roots in MCP?
- ❌ The main configuration files for MCP servers
- ❌ Administrative users with full system access
- ✅ A system that tells MCP servers what files/folders it can access
- ❌ The primary communication endpoints between clients and servers

---

**Question 9:** What is the correct sequence for MCP connection initialization?
- ❌ Initialized Notification → Initialize Request → Initialize Result
- ❌ Initialize Request → Initialized Notification → Initialize Result
- ❌ Initialize Result → Initialize Request → Initialized Notification
- ✅ Initialize Request → Initialize Result → Initialized Notification

---

**Question 10:** What is sampling in MCP?
- ❌ A method for collecting data from multiple sources
- ✅ A way for servers to access language models through connected MCP clients
- ❌ A process for validating client credentials
- ❌ A technique for optimizing server performance