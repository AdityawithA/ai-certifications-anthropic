# Quiz Answers — Building with the Claude API

## Module: Core Concepts

**Q1:** What are tokens in the context of language models?
**Answer:** The smallest units a language model can understand

**Q2:** What does the MMLU benchmark test?
**Answer:** Knowledge across 57 different subjects

**Q3:** What are the three main criteria for selecting an AI model?
**Answer:** Capabilities, speed, and cost

**Q4:** What happens when you increase the temperature setting?
**Answer:** Claude becomes more creative and varied in responses

**Q5:** What is the main benefit of using streaming responses?
**Answer:** Users see text appear immediately instead of waiting

**Q6:** What is the main purpose of system prompts?
**Answer:** To give Claude a specific role or behavior to follow

**Q7:** What does assistant message prefilling do?
**Answer:** Provides the beginning of Claude's response to guide its direction

**Q8:** How does Constitutional AI differ from traditional AI training?
**Answer:** It embeds ethical principles directly into training from the start

**Q9:** Which Claude model is best for tasks requiring maximum speed?
**Answer:** Claude 3.5 Haiku

**Q10:** What is the main difference between pre-training and fine-tuning?
**Answer:** Pre-training creates basic language understanding, fine-tuning teaches assistant behavior

**Q11:** When does Claude stop generating text with stop sequences?
**Answer:** Immediately when it generates any of the specified stop strings

**Q12:** What is the main purpose of prompt evaluation?
**Answer:** To objectively measure and improve prompt effectiveness

**Q13:** Why don't multi-turn conversations work automatically with Claude?
**Answer:** The API doesn't store any previous messages

**Q14:** What does latency measure in AI systems?
**Answer:** The time delay between request and response

**Q15:** Why are XML tags useful in AI prompts?
**Answer:** They provide structure and clear boundaries between different sections of content in prompts

**Q16:** What is interpretability in the context of AI research?
**Answer:** A field of research aimed at making it possible for humans to understand how AI models make decisions

**Q17:** You're building a chatbot that needs to look up current weather data. What feature would help Claude access this real-time information?
**Answer:** Tool use to call weather APIs

**Q18:** You have an 800-page financial report and want to ask an AI specific questions about it. What does RAG help you do?
**Answer:** Send only the relevant sections to the AI for each question

**Q19:** Claude wants to use multiple tools in a single response. What feature allows this?
**Answer:** Batch tool use

**Q20:** In MCP architecture, what are the three main components?
**Answer:** Host, Client, and Server

**Q21:** What is Model Context Protocol (MCP)?
**Answer:** A standardized protocol that enables secure connections between AI applications and external data sources

---

## Module: Applying the Basics (Scenarios)

**Q1:** You're building a chat app and users complain that responses take too long to appear. What feature should you implement?
- ❌ Send requests faster
- ❌ Add a loading spinner
- ❌ Make the messages shorter
- ✅ Use streaming to show text as it's generated

**Q2:** You're using Claude to extract data from documents and need the same consistent format every time. What temperature setting should you use?
- ✅ Temperature close to 0 for consistent, predictable outputs
- ❌ Temperature 0.5 for balanced responses
- ❌ Temperature 1.0 for maximum creativity
- ❌ Temperature doesn't matter for data extraction

**Q3:** You want to build a customer service bot that only talks about your company's products and stays professional. What's the best approach?
- ❌ Tell users to only ask product questions
- ❌ Add "be professional" to every user message
- ✅ Use a system prompt that makes Claude act like a customer service representative
- ❌ Set the temperature to maximum creativity

**Q4:** A user asks "What's 2+2?" and then asks "Add 5 to that." What do you need to do for the second question to make sense?
- ✅ Send both the first question and Claude's previous answer along with the second question
- ❌ Restart the conversation from the beginning
- ❌ Wait 30 seconds before sending the second question
- ❌ Send only the second question to Claude

---

## Module: Prompt Evaluation

**Q1:** You need test data for evaluating your prompt, quickly, without writing it all by hand. What's the best approach?
- ❌ Use the same example over and over
- ✅ Use Claude to automatically generate test cases
- ❌ Ask your friends to write them
- ❌ Copy examples from the internet

**Q2:** What's the difference between prompt engineering and prompt evaluation?
- ❌ Prompt engineering is for beginners, prompt evaluation is for experts
- ❌ Prompt engineering tests the prompt, prompt evaluation writes it
- ✅ Prompt engineering writes better prompts, prompt evaluation measures how well they work
- ❌ They're the same thing with different names

**Q3:** In prompt evaluation, what is a "grader" used for?
- ❌ To save your prompts to a file
- ✅ To give objective scores measuring output quality
- ❌ To write better prompts automatically
- ❌ To make Claude respond faster

**Q4:** You test a prompt once, it works great, and you ship it. What's the main risk?
- ❌ The prompt will stop working after a few days
- ✅ Users will provide unexpected inputs that break it
- ❌ It will be too expensive to run
- ❌ Other developers won't understand your code

**Q5:** After creating your dataset and feeding questions through Claude, what's the next step?
- ✅ Feed the responses through a grader to get scores
- ❌ Write a completely new prompt
- ❌ Ask users what they think
- ❌ Publish your prompt immediately

**Q6:** Using another AI model to evaluate Claude's responses — what should you ask the grader to provide for better-than-random scores?
- ❌ Just "good" or "bad"
- ✅ Strengths, weaknesses, reasoning, and a score
- ❌ A rewritten version of the response
- ❌ Only a number from 1-10

**Q7:** You want to check if Claude's output contains certain keywords and has the right length. Which type of grader should you use?
- ❌ Manual grader
- ✅ Code grader
- ❌ Model grader
- ❌ Human grader

---

## Module: Prompting Techniques

**Q1:** You want an AI to write movie reviews in a specific style. What's the best way to show it exactly what you want?
- ❌ Use very strict formatting rules
- ❌ Tell it to copy famous movie critics
- ❌ Describe the style in great detail
- ✅ Give it a sample movie review as an example

**Q2:** You're improving a prompt that generates workout plans. What should you do after writing your first version?
- ✅ Test it, see how well it works, then improve it
- ❌ Use it immediately for all workouts
- ❌ Write five different versions at once
- ❌ Ask other people to guess what it does

**Q3:** You're asking an AI to analyze a long customer review mixed in with your instructions. What helps the AI understand which part is the review?
- ❌ Put the review at the very end
- ✅ Put the review between XML tags like `<review></review>`
- ❌ Write the review in a different font
- ❌ Make the review all uppercase

**Q4:** You want an AI to write a book summary. Which opening instruction works best?
- ✅ "Write a three-paragraph summary of this book"
- ❌ "What do you think about summarizing things?"
- ❌ "I was wondering if you could maybe help with something about books?"
- ❌ "Books are interesting, aren't they?"

---

## Module: Tool Use

**Q1:** What happens right after Claude asks for specific external data?
- ❌ Claude analyzes the original question again
- ❌ The user needs to approve the data request
- ✅ Your server runs code to fetch the requested information
- ❌ Claude provides the final answer immediately

**Q2:** You want to force Claude to use a specific tool for data extraction. Which `toolChoice` setting should you use?
- ❌ `{"toolChoice": {"auto": {}}}`
- ✅ `{"toolChoice": {"tool": {"name": "tool-name"}}}`
- ❌ `{"toolChoice": {"any": {}}}`
- ❌ `{"toolChoice": {"required": true}}`

**Q3:** You ask Claude "What's the weather today?" but it says it doesn't have current weather information. What would tools help Claude do?
- ✅ Access live weather data from external sources
- ❌ Ask you to check the weather yourself
- ❌ Guess the weather based on the date
- ❌ Remember previous weather conversations

**Q4:** You're writing a tool function for Claude. What's the most important thing to include in the JSON schema?
- ❌ The programming language being used
- ✅ Detailed descriptions of what the tool does and its parameters
- ❌ Your contact information
- ❌ The function's source code

---

## Module: Retrieval-Augmented Generation (RAG)

**Q1:** What is contextual retrieval?
- ✅ A technique that adds context to document chunks before storing them to improve search accuracy
- ❌ A way to reduce the size of document chunks
- ❌ A system for automatically generating new content from existing documents
- ❌ A method for searching through documents faster

**Q2:** What is a vector database in the context of RAG systems?
- ✅ A specialized database optimized for storing, comparing, and searching through numerical embeddings
- ❌ A system for backing up document files
- ❌ A regular database that stores text documents as files
- ❌ A database that only stores mathematical equations

**Q3:** You're searching for a specific incident ID "INC-2023-Q4-011" in your documents. Semantic search isn't finding it well. What search method would work better?
- ❌ Converting everything to lowercase first
- ❌ Searching only document titles
- ✅ BM25 lexical search for exact keyword matching
- ❌ Using longer text embeddings

**Q4:** You send the text "The cat sat on the mat" to an embedding model. What do you get back?
- ❌ A shorter version of the same text
- ❌ Keywords extracted from the text
- ✅ A list of about 1024 numbers representing the meaning
- ❌ A translation in another language

**Q5:** You have an 800-page financial report and want to ask an AI specific questions about it. What does RAG help you do?
- ✅ Send only the relevant sections to the AI for each question
- ❌ Make the document shorter by deleting pages
- ❌ Translate the document into simpler language
- ❌ Create a summary of the entire document

---

## Module: Prompt Caching & Extended Thinking

**Q1:** You send Claude the same long document twice in a row. What does prompt caching help with?
- ❌ It stores your conversation history permanently
- ❌ It automatically summarizes repeated content
- ❌ It reduces the document's file size
- ✅ It saves the computational work from processing the text in the document

**Q2:** You've optimized your prompt but Claude still isn't accurate enough on a complex task. What should you consider next?
- ❌ Rewrite the prompt completely from scratch
- ❌ Break the task into smaller pieces
- ✅ Use extended thinking to improve accuracy
- ❌ Switch to a different AI model

**Q3:** You want to cache a short message that's 500 tokens long. What will happen?
- ❌ It will be automatically expanded to meet requirements
- ✅ It won't be cached because it's too short
- ❌ It will be cached normally
- ❌ It will be cached at half price

**Q4:** What is an effective technique for increasing Claude's effectiveness with images?
- ❌ Uploading more images
- ✅ Using prompt engineering techniques
- ❌ Using JPEG instead of PNG images
- ❌ Providing zoomed-in images

---

## Module: Model Context Protocol (MCP)

**Q1:** You're building a chat app where users ask Claude about their GitHub data. Without MCP, what's the main problem you'd face?
- ❌ Claude can't connect to the internet
- ❌ GitHub doesn't allow API access
- ✅ You'd have to write and maintain all the GitHub tool functions yourself
- ❌ Users can't type GitHub questions

**Q2:** You're creating an MCP server tool using the Python SDK. What's the easiest way to define a new tool?
- ❌ Create a separate configuration file
- ❌ Send HTTP requests to register tools
- ❌ Write complex JSON schemas manually
- ✅ Use the `@mcp.tool` decorator on a function

**Q3:** Claude automatically decides to use a calculator tool when you ask "What's 15 × 23?" Who is controlling this tool usage?
- ❌ The MCP server providing the tool
- ❌ The application showing the chat
- ✅ Claude (the AI model) itself
- ❌ The user who asked the question

**Q4:** You just wrote an MCP server and want to test if your tools work correctly. What's the best first step?
- ❌ Ask other developers to try it
- ❌ Connect it to Claude immediately
- ❌ Write unit tests for each function
- ✅ Use the MCP Inspector in your browser

**Q5:** You want to let users type "@document_name" to automatically include document content in their message. Should you use a tool or a resource?
- ❌ Tool - because Claude needs the information
- ❌ Resource - because documents are files
- ✅ Resource - because the app fetches data for the UI
- ❌ Tool - because it involves documents

**Q6:** You're running an MCP client and server on the same computer. How do they most commonly communicate with each other?
- ❌ Using Bluetooth connection
- ✅ Through standard input/output
- ❌ Through email messages
- ❌ By writing files to disk

**Q7:** Your MCP client needs to find out what capabilities an MCP server offers. What message type should it send?
- ❌ `GetServerInfo`
- ❌ `CheckCapabilities`
- ✅ `ListToolsRequest`
- ❌ `CallToolRequest`

**Q8:** Your MCP server has tools, resources, and prompts. A user clicks a "Format Document" button in your app. Which primitive is being used?
- ❌ Resources - because it accesses documents
- ❌ Tools - because it formats something
- ❌ All three at the same time
- ✅ Prompts - because the user directly triggered it