# Quiz Answers — Building with the Claude API (Part 3)

## Module: API Fundamentals & Tool Use Overview

**Q1:** What is a tool function in the context of Claude's tool use system?
**Answer:** A plain function that gets executed when Claude needs additional information or needs to perform an action

**Q2:** You're improving a prompt that isn't working well. What should you do after applying a prompt engineering technique?
**Answer:** Use prompt evaluations to see if it actually improved

**Q3:** You're making a math tutoring app. You want Claude to give hints instead of direct answers. What should you use?
**Answer:** A system prompt explaining Claude should act like a tutor

**Q4:** You want Claude to write very creative, unpredictable stories. What temperature setting should you use?
**Answer:** 1.0 (very high)

**Q5:** You want an AI to write a product description. Which opening is most clear and direct?
**Answer:** "Write a product description for running shoes."

**Q6:** You want to measure how well your AI prompt actually works in practice. Which approach should you focus on?
**Answer:** Prompt evaluation with automated testing

**Q7:** You're building a web app that talks to Claude. Where should you store your API key?
**Answer:** On your server, hidden from users

**Q8:** What is a model grader in prompt evaluation?
**Answer:** Another AI model used to assess the quality of outputs

**Q9:** You're asking an AI to analyze both customer reviews and sales data. How should you organize this information in your prompt?
**Answer:** Use XML tags like `<reviews>` and `<sales_data>` to separate them

**Q10:** You want to send a message to Claude through the API. Which four things do you absolutely need to include?
**Answer:** API key, model name, messages, and max tokens

**Q11:** What is the primary purpose of tool use in Claude?
**Answer:** To allow Claude to access real-time information and external systems beyond its training data

**Q12:** You're running a prompt evaluation. After getting responses from Claude, what's the next step in the typical workflow?
**Answer:** Feed the responses through a grader for scoring

**Q13:** You ask Claude "What is pizza?" and it answers. Then you ask "What toppings are popular?" but Claude doesn't know you're still talking about pizza. What's the problem?
**Answer:** You need to send the whole conversation history with each request

**Q14:** What is the primary difference between an MCP Server and an MCP Client in terms of their roles?
**Answer:** MCP Servers contain tools, prompts, and resources while MCP Clients act as the communication bridge to access those tools

**Q15:** Which of the following best describes Computer Use in the context of Claude?
**Answer:** A capability that lets Claude interact directly with desktop environments like a human would

**Q16:** What does "transport agnostic" mean in the context of MCP communication?
**Answer:** MCP clients and servers can communicate using different methods like HTTP or standard input/output

**Q17:** What is the primary purpose of a batch tool in Claude's tool system?
**Answer:** To accept multiple tool calls and execute them simultaneously

**Q18:** Claude responds to your request with both explanatory text and a tool use block. What type of message structure is this?
**Answer:** A multi-block message with different content types

**Q19:** You're building an app where users need to verify information Claude provides from documents. What feature should you enable?
**Answer:** Citations

**Q20:** When should you choose workflows over agents for handling user tasks?
**Answer:** When you can picture the exact flow or steps Claude should go through to solve a problem

**Q21:** Which of the following best describes why environment inspection is crucial for AI agents?
**Answer:** It allows agents to observe and understand the results of their actions

**Q22:** What is the Model Context Protocol (MCP)?
**Answer:** A communication layer that provides Claude with context and tools without requiring tedious integration code

**Q23:** You keep sending the same long document to Claude with different questions. How can you make this faster and cheaper?
**Answer:** Use prompt caching with cache breakpoints

---

## Module: API Basics (Scenarios)

**Q1:** You want to send a request to Claude's API. What's the minimum information you must include?
- ❌ Only the API key and your question
- ❌ Just your message text
- ✅ API key, model name, messages, and max tokens
- ❌ Your name, email, and message

**Q2:** You ask Claude "What is pizza?" and it answers. Then you ask "What toppings are popular?" but Claude doesn't understand what you're referring to. What's the problem?
- ❌ Your internet connection is slow
- ❌ Claude is broken
- ❌ You asked too quickly
- ✅ Claude doesn't remember previous messages

**Q3:** When Claude processes your text, what's the first thing it does?
- ❌ Generates a response immediately
- ❌ Checks if it's appropriate content
- ✅ Breaks it into smaller chunks called tokens
- ❌ Translates it to another language

**Q4:** Users complain your chat app feels slow because they wait 20 seconds staring at a loading spinner, then all the generated text appears at once. What can fix this?
- ❌ Asking shorter questions
- ❌ Using a faster internet connection
- ✅ Enabling response streaming
- ❌ Using a different web browser

**Q5:** You're building a web app that talks to Claude. Where should you store your API key?
- ❌ In your mobile app that users install
- ❌ In a text file on the user's computer
- ✅ On your server that users can't access
- ❌ In your JavaScript code that users download

**Q6:** You're building a math tutor bot. You want Claude to give hints instead of direct answers. What should you use?
- ❌ Setting a very low word limit
- ❌ Using all capital letters in your messages
- ✅ A system prompt explaining the tutor role
- ❌ Asking users to be more specific

**Q7:** You want Claude to give very predictable, consistent answers for a factual Q&A app. What temperature setting should you use?
- ❌ Temperature doesn't matter for facts
- ✅ Low temperature (near 0.0)
- ❌ Medium temperature (around 0.5)
- ❌ High temperature (near 1.0)

**Q8:** You're building an app that needs clean JSON from Claude with no extra text or formatting. How do you get just the raw JSON?
- ❌ Send the request multiple times and pick the best one
- ❌ Ask Claude very nicely to only return JSON
- ✅ Combine prefilled messages and stop sequences
- ❌ Use a very high temperature setting

---

## Module: Prompt Evaluation

**Q1:** You wrote a prompt and tested it once. It worked fine, so you deployed it to production. What's the main risk with this approach?
- ✅ Users will provide unexpected inputs that break it
- ❌ The prompt will become too expensive
- ❌ The prompt will work too slowly
- ❌ Other developers won't understand it

**Q2:** You need test cases for your prompt evaluation. Which model should you use for generation?
- ❌ The most expensive model available
- ❌ Multiple models combined
- ✅ A faster model like Haiku
- ❌ The same model you're testing

**Q3:** You're running a prompt evaluation workflow. You've used Claude to generate some responses. What's the next step?
- ❌ Deploy to production
- ❌ Rewrite the original prompt
- ❌ Create more test questions
- ✅ Feed the responses through a grader

**Q4:** You want to measure how well your prompts actually work in practice. Which approach should you focus on?
- ❌ Using more examples
- ❌ Prompt engineering techniques
- ❌ Writing longer prompts
- ✅ Prompt evaluation methods

**Q5:** You're using a model grader to evaluate responses. To get better scores than just middle-range numbers, what should you ask for alongside the score?
- ❌ Just the numerical score
- ❌ Comparison to other responses
- ✅ Strengths, weaknesses, and reasoning
- ❌ A longer explanation

**Q6:** Which type of grader uses another AI model to assess the quality of outputs?
- ✅ Model grader
- ❌ Human grader
- ❌ Syntax grader
- ❌ Code grader

---

## Module: Prompting Techniques

**Q1:** You want Claude to create a workout plan. Which opening line works better?
- ✅ "Create a 30-minute workout plan for beginners"
- ❌ "Do you know anything about exercise?"
- ❌ "I was wondering about workouts and fitness stuff"
- ❌ "What kind of workout should I do?"

**Q2:** Claude keeps missing sarcastic comments when analyzing social media posts. What's the best way to fix this?
- ❌ Ask it to guess when something might be sarcastic
- ✅ Provide examples showing sarcastic posts labeled as negative
- ❌ Tell it to "be more careful about sarcasm"
- ❌ Make the prompt longer with more instructions

**Q3:** What is prompt engineering?
- ❌ Training AI models on new datasets
- ✅ Improving a prompt to get more reliable, higher-quality outputs
- ❌ Programming AI models from scratch using code
- ❌ Building the hardware infrastructure for AI systems

**Q4:** "Providing sample input/output pairs to guide AI responses" describes which prompt engineering technique?
- ❌ Being clear and direct
- ❌ Iterative refinement
- ❌ XML structuring
- ✅ One-shot or multi-shot prompting

**Q5:** What is the main purpose of using XML tags in prompts?
- ❌ To reduce the token count of prompts
- ❌ To increase the processing speed of AI models
- ✅ To add structure and clarity, especially when including large amounts of content
- ❌ To make prompts look more professional

---

## Module: Tool Use Deep Dive

**Q1:** How can you tell if Claude wants to make another tool call in a conversation?
- ❌ Check if the response contains the word "tool"
- ❌ Check if the response is longer than usual
- ✅ Look at the `stop_reason` field for "tool_use"
- ❌ Count the number of message blocks

**Q2:** When Claude uses a tool, what type of message structure does it return?
- ✅ Multi-block messages with text and tool use blocks
- ❌ Simple text-only responses
- ❌ JSON data without any text
- ❌ Error messages only

**Q3:** What is the main purpose of a JSON schema when working with Claude tools?
- ❌ To format the final response for users
- ✅ To tell Claude what arguments your function expects and how to use it
- ❌ To store the results of tool function calls
- ❌ To encrypt data between Claude and your server

**Q4:** What problem does the batch tool solve?
- ❌ It makes tools run faster
- ❌ It translates tool results into different languages
- ✅ It reduces the number of back-and-forth communications when multiple tools are needed
- ❌ It automatically fixes errors in tool responses

**Q5:** What is the correct sequence of steps in the tool use workflow?
- ✅ Initial Request → Tool Request → Data Retrieval → Final Response
- ❌ Tool Request → Initial Request → Final Response → Data Retrieval
- ❌ Final Response → Initial Request → Tool Request → Data Retrieval
- ❌ Data Retrieval → Tool Request → Initial Request → Final Response

**Q6:** Claude can only access information from its training data by default. What allows Claude to get current, real-time information?
- ❌ Making educated guesses based on patterns
- ❌ Searching through its training data more carefully
- ❌ Asking the user to provide more details
- ✅ Using tools to access external information

**Q7:** What makes Claude's built-in text editor and web search tools different from custom tools?
- ✅ Claude provides the schema, but you may still need to implement some functionality
- ❌ They require special API keys
- ❌ They only work with specific file types
- ❌ They cost more to use

---

## Module: Files, Caching, Citations & Extended Thinking

**Q1:** What is the Files API used for?
- ❌ Scanning files for viruses and malware
- ❌ Compressing large files to reduce API costs
- ❌ Converting files between different formats automatically
- ✅ Uploading files ahead of time and referencing them later instead of encoding them directly in messages

**Q2:** You're making many requests with the same large system prompt. What feature would make your requests faster and cheaper?
- ❌ PDF processing
- ❌ Citations
- ❌ Extended thinking
- ✅ Prompt caching

**Q3:** What is the primary purpose of citations in Claude?
- ✅ To create a clear trail from Claude's response back to specific parts of source documents
- ❌ To compress large documents for faster processing
- ❌ To count the number of words in a document
- ❌ To automatically generate footnotes for academic papers

**Q4:** When Claude uses extended thinking, what two parts do you get in the response?
- ✅ Reasoning process and final answer
- ❌ Problem and solution
- ❌ Input and output
- ❌ Question and answer

**Q5:** You want Claude to analyze a PDF document. What's the main difference from sending an image?
- ✅ Change the type to "document" and media_type to "application/pdf"
- ❌ PDFs cost more to process
- ❌ You can only send text, not images in PDFs
- ❌ PDFs require special permission

**Q6:** What is a key limitation of Claude's Code Execution tool?
- ❌ It can only run JavaScript code
- ✅ It has no network access and runs in an isolated Docker container
- ❌ It requires users to provide their own execution environment
- ❌ It can only process text files

**Q7:** You want to cache your system prompt. What's the minimum requirement for caching to work?
- ❌ You must make at least 5 requests
- ❌ You must use extended thinking
- ❌ The content must be under 500 tokens
- ✅ The content must be at least 1024 tokens long

---

## Module: Model Context Protocol (MCP)

**Q1:** You've created an MCP server and want to test your tools before connecting them to Claude. What's the best way to do this?
- ❌ Testing isn't needed for tools, Claude can figure out how to use them
- ❌ Connect to Claude immediately
- ✅ Use the MCP Inspector in your browser
- ❌ Test in production

**Q2:** You're building a document system where users can type @document_name to reference files. What MCP feature is best for exposing the document contents?
- ❌ Tools
- ❌ Clients
- ❌ Prompts
- ✅ Resources

**Q3:** Your MCP server and client need to communicate. What's the most common way they connect during development?
- ❌ Through a database
- ❌ Over the internet
- ✅ Through standard input/output on the same machine
- ❌ Using email

**Q4:** You're building a chatbot that needs to access GitHub data. What is the main benefit of using MCP instead of writing your own GitHub integration?
- ❌ MCP requires less memory
- ✅ MCP handles the tool definitions and execution for you
- ❌ MCP only works with GitHub
- ❌ MCP makes your chatbot run faster

**Q5:** You want to create a tool for your MCP server that reads document contents. Using the Python SDK, what's the easiest way to define this tool?
- ❌ Write a complex JSON schema manually
- ❌ Send an HTTP request
- ✅ Use the `@mcp.tool` decorator on a function
- ❌ Create a separate configuration file

**Q6:** You want to provide users with a high-quality, pre-tested instruction for formatting documents. What MCP feature should you use?
- ❌ Resources
- ❌ Sessions
- ❌ Tools
- ✅ Prompts

---

## Module: Agentic Workflow Patterns

**Q1:** You're building an agent with tools. Which approach will give Claude the most flexibility to handle unexpected requests?
- ❌ Give Claude only one powerful tool
- ❌ Provide very specific tools like "write_python_function" and "debug_code"
- ✅ Provide abstract tools like "read_file", "write_file", and "run_command"
- ❌ Provide tools that only work for planned scenarios

**Q2:** You want Claude to write a report, then check if it's good enough, and improve it if needed. What pattern are you using?
- ❌ Chaining workflow
- ✅ Evaluator-Optimizer pattern
- ❌ Parallelization workflow
- ❌ Routing workflow

**Q3:** Your app generates different types of social media content. Programming topics need educational scripts, while sports topics need entertainment-focused content. What pattern should you use?
- ✅ Route requests to specialized processing pipelines
- ❌ Use the same prompt for everything
- ❌ Ask users to write their own content
- ❌ Always use the entertainment approach

**Q4:** Claude keeps ignoring some of your rules when you give it a long prompt with many requirements. What workflow approach would help?
- ❌ Make the prompt even longer with more rules
- ❌ Run everything in parallel
- ❌ Use a routing workflow to categorize first
- ✅ Chain the task into focused sequential steps

**Q5:** You need Claude to recommend the best material for a part by considering metal, plastic, ceramic, and wood options. Each material has different criteria. What's the best approach?
- ❌ Chain the evaluations one after another
- ❌ Ask Claude to pick randomly
- ✅ Send separate requests for each material type in parallel
- ❌ Put all criteria in one big prompt

**Q6:** You need to choose between a workflow and an agent for your app. Reliability and predictable results are most important to you. Which should you pick?
- ❌ Always use an agent for maximum flexibility
- ✅ Use a workflow since it's more reliable and testable
- ❌ Combine both approaches equally
- ❌ Use whichever is easier to code

**Q7:** You're building an app where users upload photos of damaged car parts and always get repair cost estimates. You know exactly what steps are needed each time. What should you use?
- ❌ Multiple agents working together
- ❌ A single complex prompt
- ❌ An agent with many specialized tools
- ✅ A workflow with predetermined steps