# Quiz Answers — Introduction to Model Context Protocol

**Question 1:** You're building an MCP client to connect your application to an MCP server. What are the two main components you need?
- ❌ A frontend and a backend
- ❌ A database and a web server
- ❌ A REST API and a GraphQL endpoint
- ✅ An MCP Client class and a Client Session

---

**Question 2:** Your MCP client needs to find out what tools are available from an MCP server. What message type should it send?
- ✅ ListToolsRequest
- ❌ CallToolRequest
- ❌ ToolDiscoveryRequest
- ❌ GetToolsMessage

---

**Question 3:** You've built an MCP server and want to test if your tools work correctly before connecting to a full application. What's the easiest way to do this?
- ❌ Write separate test scripts for each tool
- ❌ Test everything manually in the terminal
- ✅ Use the built-in MCP Inspector with `mcp dev mcp_server.py`
- ❌ Connect directly to Claude first

---

**Question 4:** You're building a chat app where users ask Claude about their GitHub data. Without MCP, what's the main problem you'd face?
- ❌ GitHub doesn't allow API access
- ✅ You'd have to write and maintain all the GitHub tool code yourself
- ❌ Claude can't understand GitHub data
- ❌ Users can't ask questions about repositories

---

**Question 5:** You're deciding how to implement a new feature in your MCP server. Users should be able to click a button to trigger a "summarize document" workflow. Which MCP primitive should you use?
- ❌ Resources - because you need to fetch document data
- ❌ Functions - because it involves processing
- ✅ Prompts - because users control when to start the workflow
- ❌ Tools - because the AI needs new capabilities

---

**Question 6:** You're using the Python MCP SDK to create a tool that reads files. What's the easiest way to define this tool?
- ✅ Use the `@mcp.tool()` decorator on a Python function
- ❌ Create a separate configuration file
- ❌ Write JSON schemas manually
- ❌ Send HTTP requests to register the tool

---

**Question 7:** You want to create a resource that fetches different documents based on their ID, like `docs://documents/report.pdf`. What type of resource should you use?
- ✅ A templated resource with parameters in the URI
- ❌ A tool instead of a resource
- ❌ A direct resource with a static URI
- ❌ A database query resource