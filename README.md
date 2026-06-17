Why I built this project?
I wanted to understand how tool calling works in Claude API
before moving to bigger real world projects like WMS and Excel automation.
Started with simple math — add, multiply, divide — so I can focus
on understanding the concept without getting lost in complexity.

What this project covers:

- How to make Schematic and call tools
- Difference between JSON schema and JSON payload
- Why messages list is needed every single API call
- How to handle multiple tool calls in one user message

What I learned:

- No bind_tools needed in Claude — tools go directly into each .create() call or use Langchain to use .invoke()
- role and content keys are not random — Claude specifically looks for these words
- tool_use_id is like a tracking number to match results back to the right tool call

How to run:

1. Open in Google Colab
2. Add your Anthropic API key to Colab Secrets as `ANTHROPIC_API_KEY`
3. install anthropic
4. Run the code and type your math question

Example questions to try:

- what id the addition of 12753 and 83638
- can you give add and multiply 287 and 356
- Divide 100 by 0
- what is the difference between division and percentage? (some out of tool questions)

Next steps:

- Move towards creating tool to call python codes and use these codes to run on given excel sheet to perform any mathematical task.
- Will create agent to help me for real world use cases like analyzing high velocity inventory, efficient slotting by providing data in excel sheet attaching it to llm.
