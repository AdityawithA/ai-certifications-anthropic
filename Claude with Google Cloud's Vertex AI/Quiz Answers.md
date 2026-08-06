# Quiz Answers — Building with the Claude API (Part 2)

## Module: Core Concepts Review

**Q1:** You're using Claude to brainstorm creative story ideas and want more variety in the suggestions. What should you do?
**Answer:** Increase the temperature setting

**Q2:** You wrote a prompt and tested it twice with your own inputs. It worked perfectly both times, so you deployed it to production. What risk does this approach carry?
**Answer:** Users will provide unexpected inputs that break the prompt

**Q3:** You want to improve your prompt's first line. Instead of "Can you help me with something about solar panels?" what would be better?
**Answer:** "Write three paragraphs explaining how solar panels work"

**Q4:** You're asking Claude to analyze a large data file mixed with your instructions. What's the best way to keep things organized?
**Answer:** Use XML tags like `<data>` and `<instructions>`

**Q5:** You've written a prompt for Claude and want to know if it actually works well. What should you use to get objective measurements of its performance?
**Answer:** Prompt evaluation methods

**Q6:** You want Claude to generate clean JSON without any markdown formatting or extra text. What's the best approach?
**Answer:** Prefill with "```json" and use "```" as a stop sequence

**Q7:** You ask Claude "What is pizza?" then want to follow up with "Tell me more." What do you need to do so Claude remembers the first question?
**Answer:** Send both the original question and Claude's answer with your new question

**Q8:** You need to check if an AI model's output contains valid Python code. Which type of grader would work best for this task?
**Answer:** Code grader

**Q9:** You want Claude to write a 500-word blog post with three main sections. Which approach gives you the most control over the output?
**Answer:** Provide specific guidelines about length and structure

**Q10:** You're building a chat app where Claude takes 20 seconds to respond. Users complain about staring at a loading screen. What's the best solution?
**Answer:** Enable response streaming to show text as it generates

**Q11:** You want Claude to act like a friendly teacher instead of giving generic responses. What should you use?
**Answer:** A system prompt

**Q12:** You ask Claude "Is tea or coffee better?" but want it to argue for coffee specifically. What should you add to your messages?
**Answer:** Add an assistant message saying "Coffee is better because"

**Q13:** You're making your first API call to Claude. Which four things must you include in every request?
**Answer:** API Key, Model, Messages, Max Tokens

**Q14:** You need test cases for your prompt evaluation but don't want to write them all by hand. What's an efficient alternative mentioned in the content?
**Answer:** Generate test cases automatically using Claude

**Q15:** You're building a web app that talks to Claude. Where should you put your API key?
**Answer:** On your secure server

**Q16:** What is the primary purpose of tool use in Claude?
**Answer:** To extend Claude's capabilities beyond its training data by accessing external information

**Q17:** You want Claude to detect sarcasm in social media posts. What technique would help Claude understand this tricky task?
**Answer:** Show examples of sarcastic posts with correct labels

**Q18:** A user asks Claude "What's the current temperature in New York?" Without tools, what happens?
**Answer:** Claude says it doesn't have access to current weather information

**Q19:** A user asks "What are the company's main risks?" Your vector database finds cosine similarity scores of 0.95 and 0.3. Which chunk should be retrieved?
**Answer:** The chunk with 0.95 similarity (more similar)

**Q20:** You're building a conversation loop with Claude. How do you know when Claude is finished and doesn't need more tools?
**Answer:** When the `stop_reason` is not `"tool_use"`

**Q21:** You have a 500-page company report and want to ask Claude questions about it. What does RAG help you do?
**Answer:** Include only the most relevant sections for each question

**Q22:** When Claude uses a tool, what type of response structure does it return instead of simple text?
**Answer:** Multi-block messages with text and tool use blocks

**Q23:** Which temperature setting would be most appropriate for factual responses and coding assistance?
**Answer:** Low temperature (0.0 - 0.3)

**Q24:** What is Retrieval Augmented Generation (RAG)?
**Answer:** A technique that helps work with large documents by finding and including only the most relevant sections for each question

---

## Module: Applying the Basics (Scenarios)

**Q1:** You're building a chat app that talks to Claude. Where should you put your API key?
- ❌ In the user's browser
- ✅ On your secure server
- ❌ In your website's JavaScript code
- ❌ In a public GitHub repository

**Q2:** What is the primary purpose of a system prompt when working with Claude?
- ❌ To authenticate API requests to the Anthropic service
- ✅ To provide instructions that customize Claude's tone, style, and approach
- ❌ To limit the number of tokens Claude can generate in a response
- ❌ To store the conversation history between multiple requests

**Q3:** Your users complain that your chat app feels slow because they wait 20 seconds staring at a loading spinner, then a bunch of generated text suddenly appears. What feature should you add?
- ❌ Shorter prompts
- ✅ Response streaming
- ❌ Multiple chatbots
- ❌ Faster internet connection

**Q4:** You want Claude to generate only clean JSON code without any explanations or markdown formatting. Which combination of techniques works best?
- ❌ Request shorter responses
- ❌ Ask nicely in the prompt
- ❌ Use high temperature and long prompts
- ✅ Prefill with `"{"` and use `"```"` as a stop sequence

**Q5:** You're building a chatbot to answer factual questions about your company. You want consistent, reliable answers every time. What temperature setting should you use?
- ✅ 0.1 (low temperature)
- ❌ It doesn't matter
- ❌ 0.8 (high temperature)
- ❌ 1.0 (high temperature)

**Q6:** Claude reads your message "I love quantum physics." What happens first?
- ✅ Claude breaks the text into smaller pieces called tokens
- ❌ Claude researches quantum physics
- ❌ Claude writes a response immediately
- ❌ Claude translates it to another language

**Q7:** You ask Claude "What's the best programming language?" but you want it to specifically argue for Python. What technique helps you control this?
- ❌ Use a higher temperature setting
- ❌ Ask the question multiple times
- ❌ Make the text bigger
- ✅ Add an assistant message starting with "Python is the best because"

---

## Module: Prompt Evaluation

**Q1:** You've learned techniques for writing better prompts, but now you want to measure how well they actually work. What do you need?
- ❌ More prompt engineering techniques
- ✅ Prompt evaluation methods
- ❌ More training data
- ❌ A faster AI model

**Q2:** You need test cases for your prompt evaluation but don't want to write them all by hand. What's a good alternative?
- ❌ Ask users to create test cases
- ❌ Only test with one example
- ❌ Skip testing and deploy immediately
- ✅ Use Claude to generate test cases automatically

**Q3:** You write a prompt and test it twice with your own inputs. It looks good, so you deploy it. What's the main risk?
- ❌ The prompt will work too slowly
- ❌ The prompt will become too expensive
- ❌ The AI model will stop working
- ✅ Users might provide unexpected inputs that break it

**Q4:** In a typical evaluation workflow, what happens right after you feed your prompts through Claude?
- ❌ You change the prompt and start over
- ✅ You feed the responses through a grader
- ❌ You create a new dataset
- ❌ You deploy the prompt to production

---

## Module: Prompting Techniques

**Q1:** You're giving your AI a long document to analyze along with your instructions. What would help the AI understand your prompt better?
- ❌ Put everything in one big paragraph
- ❌ Write the document in all capital letters
- ✅ Use XML tags like `<document>` and `<instructions>`
- ❌ Separate sections with lots of blank lines

**Q2:** You want your AI to write a book review. Which approach would be more helpful?
- ✅ "Write a book review that's 300 words, includes plot summary, mentions two characters, and gives a rating"
- ❌ "Write a book review that's good and interesting"
- ❌ "Tell me what you think about books in general"
- ❌ "Write something about the book I just read"

**Q3:** You want to improve a prompt that isn't working well. What should you do first after writing your initial prompt?
- ✅ Test it and measure how well it performs
- ❌ Add more examples immediately
- ❌ Rewrite it completely from scratch
- ❌ Make it longer and more detailed

**Q4:** Your evaluation report shows your prompt scored poorly on "missing calorie information" across multiple test cases. What does this tell you?
- ❌ You should ignore this feedback and try something else
- ✅ You need to specifically tell your prompt to include calorie information
- ❌ The test cases are too hard
- ❌ The evaluation system is broken

**Q5:** You want your AI to detect sarcasm in social media posts, but it keeps missing sarcastic comments. What would help most?
- ❌ Tell it to "try harder" to find sarcasm
- ❌ Use bigger fonts in your prompt
- ✅ Show it examples of sarcastic posts with correct labels
- ❌ Ask it to guess when posts might be sarcastic

**Q6:** Why is the first line of your prompt considered the most important part?
- ❌ It determines which AI model will be used
- ❌ It determines how fast the AI will respond
- ✅ It sets the stage for everything that follows and should be clear and direct
- ❌ It controls the length of the AI's response

---

## Module: Tool Use

**Q1:** When Claude wants to use a tool, it sends back a response that's different from usual. What does this response contain?
- ❌ Error messages only
- ✅ Both text blocks and tool use blocks
- ❌ Only tool requests with no text
- ❌ Only text like normal

**Q2:** You want to create a tool that gets the current time. What type of code do you need to write?
- ✅ A regular Python function
- ❌ A web page
- ❌ A database query
- ❌ A complex AI algorithm

**Q3:** A user asks Claude "What day will it be 30 days from today?" To answer this, Claude needs to use multiple tools. What happens?
- ❌ Claude asks the user to do the math
- ❌ Claude uses one tool and guesses the rest
- ✅ Claude calls tools in sequence - first getting today's date, then adding 30 days
- ❌ Claude gives up and says it can't help

**Q4:** Sarah asks Claude "What's the weather like today?" but Claude says it doesn't have current weather data. What would solve this problem?
- ❌ Waiting for Claude to update itself
- ✅ Giving Claude access to tools that fetch current data
- ❌ Asking Claude to guess the weather
- ❌ Training Claude on more weather information

**Q5:** You're building a chat app with Claude. A user asks for today's stock prices, but Claude responds "I don't have access to current stock information." What's the core problem?
- ❌ The user asked the wrong question
- ❌ Claude is broken
- ✅ Claude only knows information from its training data
- ❌ Claude needs to be restarted

**Q6:** You want to give Claude the ability to search the web for current information. What do you need to implement?
- ✅ Just a simple schema - Claude handles the searching
- ❌ Your own search engine
- ❌ A complex web scraping system
- ❌ Permission from Google

**Q7:** You've written a Python function for Claude to use. What else do you need so Claude knows how to call it?
- ❌ Permission from Claude
- ✅ A JSON schema describing the function
- ❌ A special license
- ❌ A user manual

---

## Module: Retrieval-Augmented Generation (RAG)

**Q1:** You're setting up a system to handle large documents. Instead of using everything at once, you break documents into smaller pieces and search for relevant ones. What is this approach called?
- ✅ The chunking approach
- ❌ File splitting
- ❌ Text summarization
- ❌ Document compression

**Q2:** You try to include a massive 800-page document directly in your Claude prompt. What problems will you likely face?
- ✅ There are hard limits on text length, reduced effectiveness, and higher costs
- ❌ The document will be perfectly processed
- ❌ Claude will work faster than normal
- ❌ Only the cost will increase slightly

**Q3:** You have an 800-page financial report and want to ask Claude specific questions about it. What does RAG help you do?
- ❌ Ask only yes/no questions
- ❌ Put the entire document into each prompt
- ❌ Summarize the whole document first
- ✅ Find and include only the relevant sections for each question

**Q4:** You send the text "The cat is happy" to an embedding model. What do you get back?
- ❌ A summary of the text
- ❌ A translation in another language
- ❌ A list of keywords
- ✅ A long list of numbers

**Q5:** What problem does contextual retrieval solve in RAG systems?
- ❌ It makes search queries run faster
- ❌ It reduces the storage space needed for embeddings
- ✅ It addresses the issue of chunks losing their connection to broader document context when documents are split
- ❌ It eliminates the need for vector databases

**Q6:** You have search results from both semantic search and BM25 search. They use different scoring systems. How do you combine them into one ranked list?
- ✅ Use Reciprocal Rank Fusion (RRF) based on rank positions
- ❌ Take the average of both scores
- ❌ Add the scores together directly
- ❌ Use only the semantic search results

**Q7:** What is the purpose of re-ranking in RAG pipelines?
- ❌ To compress the vector database for faster searches
- ❌ To generate better embeddings for text chunks
- ✅ To use an LLM to intelligently reorder search results after initial retrieval
- ❌ To split documents into more appropriate chunk sizes

**Q8:** You're searching for a specific incident ID like "INC-2023-Q4-011" in your documents. Semantic search isn't finding it well. What additional search method would help?
- ❌ Bigger vector database
- ✅ BM25 lexical search for exact term matching
- ❌ Longer embeddings
- ❌ More chunks

---

## Module: Extended Thinking, Caching & Citations

**Q1:** When Extended Thinking is enabled, what two parts will Claude's response contain?
- ❌ A summary block and a detail block
- ✅ A thinking block and a text block
- ❌ A draft block and a final block
- ❌ A question block and an answer block

**Q2:** You ask Claude "How many marbles are in this image?" but get the wrong count. What's the best way to improve accuracy?
- ❌ Ask the question in all capital letters
- ❌ Send a higher quality image
- ❌ Upload the image multiple times
- ✅ Provide detailed counting steps and methodology

**Q3:** What's the minimum amount of content needed for caching to work?
- ❌ Any amount of text
- ❌ 500 tokens
- ✅ 1024 tokens
- ❌ 2000 tokens

**Q4:** You want to cache your tool definitions. Where should you place the cache breakpoint?
- ✅ On the last tool in your list
- ❌ On the middle tool in your list
- ❌ On every tool in your list
- ❌ On the first tool in your list

**Q5:** How does prompt caching work?
- ❌ It makes Claude remember conversations forever
- ❌ It prevents Claude from making mistakes
- ✅ It reuses computational work from previous requests
- ❌ It translates messages into different languages

**Q6:** You're building an app where users ask questions about documents. What's the main benefit of enabling citations?
- ❌ It reduces the cost of each request
- ✅ It shows users exactly where information came from
- ❌ It makes Claude's responses longer
- ❌ It makes the app run faster

---

## Module: Model Context Protocol (MCP)

**Q1:** User-controlled workflows that are triggered through UI interactions like button clicks or slash commands. This definition describes which MCP primitive?
- ❌ Resources
- ❌ Sessions
- ❌ Tools
- ✅ Prompts

**Q2:** What does "transport agnostic" mean in the context of MCP communication?
- ❌ MCP automatically chooses the fastest available network connection
- ❌ MCP requires specific hardware to function properly
- ❌ MCP only works with HTTP connections
- ✅ MCP clients and servers can communicate using different methods like HTTP, WebSockets, or standard input/output

**Q3:** What are Resources in the context of MCP?
- ✅ App-controlled data access for UI purposes or adding context to conversations
- ❌ Model-controlled functions for performing calculations
- ❌ User-triggered commands that start predefined workflows
- ❌ Server configuration settings that control performance

**Q4:** In MCP architecture, what is the relationship between MCP Clients and MCP Servers?
- ❌ MCP Clients generate AI responses while MCP Servers handle user input
- ❌ MCP Clients store data while MCP Servers process requests
- ✅ MCP Clients connect to MCP Servers that contain tools, prompts, and resources
- ❌ MCP Clients and MCP Servers are the same component with different names

**Q5:** What is Model Context Protocol (MCP)?
- ❌ A programming language specifically designed for AI applications
- ✅ A communication layer that provides Claude with context and tools without requiring tedious integration code
- ❌ A security protocol for encrypting AI model responses
- ❌ A database management system for storing AI conversations

**Q6:** What is the MCP Server Inspector?
- ❌ A command-line tool for monitoring server performance
- ❌ A code editor specifically designed for writing MCP servers
- ❌ A security tool for scanning MCP servers for vulnerabilities
- ✅ A browser-based interface for testing and debugging MCP servers in real-time

**Q7:** Which of the following correctly describes Tools in MCP?
- ❌ App-controlled data that populates UI elements
- ❌ Static configuration files that define server behavior
- ❌ User-controlled workflows that can be triggered on demand
- ✅ Model-controlled functions that Claude decides when to call

---

## Module: Agentic Workflow Patterns

**Q1:** You want Claude to analyze a product image for 6 different materials at once. Instead of one huge prompt, what should you do?
- ❌ Write a longer, more detailed prompt
- ✅ Send 6 separate requests in parallel, then combine results
- ❌ Ask the user to pick one material first
- ❌ Use an agent with material tools

**Q2:** You're building a system where Claude creates content, then checks if it's good enough, then improves it if needed. What pattern is this?
- ❌ Parallelization
- ✅ Evaluator-optimizer
- ❌ Routing
- ❌ Chaining

**Q3:** You're building an app where users upload photos and always get the same 4-step process to enhance them. Which approach should you use?
- ❌ An agent with photo tools
- ❌ A single complex prompt
- ❌ Multiple agents working together
- ✅ A workflow with predefined steps

**Q4:** Your app needs to handle both "cooking recipes" and "workout routines" with completely different styles. What pattern helps?
- ❌ Combine both styles in one prompt
- ❌ Use the same prompt for both
- ✅ Routing - categorize first, then use specialized prompts
- ❌ Always ask users to specify the category

**Q5:** What defines an agent when working with Claude?
- ❌ A predetermined sequence of steps that Claude must follow exactly
- ✅ A setup where Claude is given a goal and tools, then figures out how to complete the goal
- ❌ A system that categorizes user requests into different types
- ❌ A method for breaking complex tasks into parallel subtasks

**Q6:** What is environment inspection in the context of AI agents?
- ❌ The process of categorizing user requests into different workflow types
- ❌ The technique of running multiple specialized tasks simultaneously
- ❌ A method for breaking large tasks into smaller sequential steps
- ✅ Claude's ability to observe and understand the results of its actions

**Q7:** You're building an agent. In general, should you give it a "Refactor Code" tool or basic tools like "read file" and "write file"?
- ❌ "Refactor Code" tool - it's more specific
- ✅ Basic tools - they're more flexible
- ❌ Both tools together
- ❌ Neither - agents don't need tools