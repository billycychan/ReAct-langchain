# ReAct LangChain Example: Text Length Tool Integration

This example demonstrates how to integrate a custom tool (get_text_length) into a ReAct LangChain agent. 

**Here's a breakdown:**

* **Custom Tool (`get_text_length`):** This function calculates the length of a given text string in characters.
* **ReAct Agent Setup:**
    *  A `ChatOpenAI` instance with GPT-4o-mini model is used as the language model.
    * A `PromptTemplate` defines the structure for agent interaction, including instructions to use available tools and format responses.
    * Tools are rendered into a description string and included in the prompt.
    *  The `ReActSingleInputOutputParser` is used to parse the agent's output into structured steps (Thought, Action, etc.).
* **Agent Workflow:**
    * The agent receives an input question ("What is the length of the word: DOG?").
    * It analyzes the question and determines the action needed.
    * In this case, the action is to call the `get_text_length` tool with the word "DOG" as input.
    * The tool's output (the length of the word) is returned to the agent.
    * The agent processes the observation and continues its thought process until it arrives at a final answer.

**Key Features:**

* **Tool Integration:**  The example demonstrates how to seamlessly integrate custom tools into ReAct agents.
* **Structured Interaction:**  ReAct's structured output format allows for clear understanding of the agent's reasoning process.
* **Flexibility:** You can easily add more tools and modify the prompt template to suit your specific use case.


