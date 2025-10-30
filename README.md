# S.V.Gautham-langgraph-MAT496

## Module 1
**Video 1 – Motivation:**
The video talks about how traditional language model workflows, known as chains, work well but can be too limited. LangGraph was developed to make these workflows more flexible. It lets developers set up the dependable parts of a process while allowing the LLM to make decisions on its own when necessary. This makes it easier to build AI agents that are smarter and can adapt to different situations.

**Video 2 – Simple Graph:**
I learned how to create simple graphs in LangGraph, including defining states, nodes, and conditional edges, as well as constructing, visualizing, and invoking the graph.
Changes made: Added my own custom graph implementation at the end of the source code under the section titled “TWEAK.”
Source Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%201/Original%20Source%20Code/simple-graph.ipynb) 
Tweaked Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%201/simple_graph_final.ipynb)

**Video 3 – LangGraph Studio Setup**
I learned how to set up and run LangGraph Studio both locally and within the studio environment. The video covered how to use the UI to input a graph state and view the dataflow threads of the graph.
Changes made: Since I used Groq as the client, I installed the required dependencies after setting up the environment, created a .env file containing the Groq and LangSmith API keys, and updated the client in router.py and agent.py (inside the /studio directory) from ChatOpenAI() to ChatGroq() for proper tool binding.

**Video 4 – Chains**
I learned how to use chat messages as the graph state and chat models as graph nodes. It also covered binding tools to the model and executing tool calls within the graph nodes.
Changes made: Used Groq’s "openai/gpt-oss-120b" model and added my own tool-calling example at the end.
**Video 2 – Simple Graph:**
I learned how to create simple graphs in LangGraph, including defining states, nodes, and conditional edges, as well as constructing, visualizing, and invoking the graph.
Changes made: Added my own custom graph implementation at the end of the source code under the section titled “TWEAK.”
Source Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%201/Original%20Source%20Code/chain.ipynb) 
Tweaked Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%201/chain_final.ipynb)

**Video 5 – Router**
I learned about the concept of a router agent, where the chat model decides whether to give a direct response or call a tool based on the user’s input. It demonstrated how the LLM manages control flow — either by invoking a tool or replying directly to the query.
Changes made: Used Groq’s "openai/gpt-oss-120b" model, created my own router example at the end, and included screenshots of the LangGraph Studio visualization.
Source Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%201/Original%20Source%20Code/router.ipynb) 
Tweaked Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%201/router_final.ipynb)

**Video 6 – Agent**
I learned about agentic architecture, where the assistant can pass a ToolMessage back to the LLM, which then decides whether to call another tool or respond directly. I also explored how LangSmith lets us view traces of the entire conversation.
Changes made: Used Groq’s "openai/gpt-oss-120b" model, created my own agent example at the end, and added screenshots of the LangSmith traces.
Source Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%201/Original%20Source%20Code/agent.ipynb) 
Tweaked Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%201/agent_final.ipynb)

**Video 7 – Agent With Memory**
I learned how agents can retain information from previous steps using persistent memory, where a checkpointer automatically saves the graph state after each action. For my own work, I switched to Groq's "openai/gpt-oss-120b" model, implemented a custom example of an agent with memory, and included screenshots of the LangGraph Studio visualization to illustrate the graph and its state changes.
Source Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%201/Original%20Source%20Code/agent-memory.ipynb) 
Tweaked Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%201/agent_memory_final.ipynb)

**Video 8 – Deployment**
I learned how to deploy the implemented Graph models both locally in Studio and on LangGraph Cloud. I practiced by writing and running code to deploy the model locally, which is available in my GitHub repository: Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%201/deployment.ipynb). Since LangGraph Cloud is a paid feature, I was unable to test deployment on the cloud platform.

## Module 2
**Video 1 – State Schema:**
Learned how to define state schemas in LangGraph using three different approaches — TypedDict, dataclass, and Pydantic. Each method helps structure and organize the data used in the graph’s state. I also understood how these schemas facilitate managing and updating the state as the graph executes. Additionally, I observed that Pydantic is unique in providing built-in runtime validation, unlike the other two methods. Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%202/state_schema.ipynb).

**Video 2 – State Reducer:**
Explored state management in LangGraph using reducers, focusing on how they handle concurrent update ambiguities during branching. Understood default overwriting behavior, the importance of reducers in branching, and the use of built-in options like “operator.add” and “add_messages.” Also learned to create custom reducers for specialized cases, such as handling None values or modifying messages. Implemented a custom example to apply these concepts in practice. Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%202/state_reducers.ipynb).

**Video 3 – Multiple Schemas:**
Learned how to use multiple schemas in LangGraph to efficiently manage data flow. This approach enables maintaining private state within nodes and defining explicit input and output schemas to control the graph’s interface. These techniques allow precise control over what data enters, is processed inside, and exits the graph.
 Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%202/multiple_schemas.ipynb).

**Video 4 – Trim and Filter Messages:**
Learned how to manage message history in LangGraph using various techniques such as reducing the number of messages, filtering specific subsets, and trimming messages based on token limits. These strategies are essential for optimizing chatbot performance by efficiently controlling the input sent to the language model.
Changes made: Developed my own example at the end and included screenshots of LangSmith traces from my implementation.  Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%202/trim_filter_messages.ipynb).

**Video 5 – Chatbot with Summarizing Messages and Memory:**
Learned how to build a chatbot in LangGraph that utilizes message summarization to manage conversation length effectively. The video also demonstrated how to incorporate memory using LangGraph’s built-in persistence mechanism with thread IDs.
Changes made: Created my own example at the end and included screenshots of LangSmith traces illustrating the functioning of persistence and summarization.Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%202/chatbot_summarization.ipynb).

**Video 6 – Chatbot with Summarizing Messages and External Memory:**
Learned how to build a LangGraph chatbot with persistent memory using an external database (SQLite) checkpointer. The video demonstrated how to define the conversation state, create nodes for interaction and summarization, and compile a graph that stores and retrieves conversation history from a database.
Changes made: Experimented with my own set of prompts on the graph and verified the summarization and memory retention using an external database (PostgreSQL).
ode:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%202/chatbot_external_memory.ipynb).

## Module 3
**Video 1 – Streaming**
Learned how to set up a LangGraph chatbot with memory and stream outputs during execution using various streaming modes — values, updates, and astream_events — to observe the graph’s state and token flow in real time.
Changes made: Used Groq’s "openai/gpt-oss-120b" model and implemented a custom example at the end. Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%203/streaming-interruption.ipynb).

**Video 2 – Breakpoints**
Explored how to use breakpoints in LangGraph to pause an agent’s graph execution at specific nodes, enabling human-in-the-loop workflows (e.g., user approval before executing actions).
Changes made: Used Groq’s "openai/gpt-oss-120b" model and implemented a custom example at the end. Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/tree/main/Module%203).

**Video 3 – Editing State and Human Feedback**
Learned how to use LangGraph breakpoints to interrupt execution and modify the graph’s state. Demonstrated two methods: directly updating the state and using a dedicated human_feedback node for structured interaction.
Changes made: Used Groq’s "openai/gpt-oss-120b" model and implemented a custom example at the end. Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%203/edit-state-human-feedback.ipynb).

**Video 4 – Dynamic Breakpoints**
Learned about the concept of dynamic breakpoints in LangGraph using NodeInterrupt. This feature allows conditional interruptions of graph execution based on the current state. It demonstrates how to pause execution, inspect and modify the state after an interrupt, and then resume the graph with the updated state — enabling human-in-the-loop workflows for approval, debugging, and live editing. Changes made: Implemented a custom example at the end. Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%203/dynamic-breakpoints.ipynb).

**Video 5 – Time Travel**
Explored the time travel capabilities of LangGraph, which allow users to review an agent’s execution history, replay from a previous state, or fork the execution by modifying a past state and continuing from there. These tools are valuable for debugging and analyzing agent behavior.
Changes made: Added screenshots demonstrating forking tools in the agent graph within LangGraph Studio, and implemented a custom example to fork and replay states in my own graph. Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%203/time-travel.ipynb).

## Module 4
**Video 1 – Parallelization**
In this video, I explored parallel node execution in LangGraph. It shows how to run multiple nodes at the same time and how to handle state updates from these parallel branches using custom reducers and waiting mechanisms.Changes made: Switched to Groq’s "openai/gpt-oss-120b" model, Added screenshots showing how the graph works in LangGraph Studio. Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%204/parallelization.ipynb).

**Video 2 – Sub-graphs**
Explored the concept of sub-graphs in LangGraph. The session illustrates how to build reusable workflow components—sub-graphs—with their own independent state and logic, and then integrate them into a parent graph to manage more complex processes such as parallel data processing. Modifications made: Implemented a custom example to reinforce understanding. Added screenshots showcasing LangSmith traces and the graph visualization in LangGraph Studio. Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%204/sub-graph.ipynb).

**Video 3 – Map-Reduce**
Explored the map-reduce paradigm using the LangGraph library. The session demonstrates how to decompose a larger task into smaller, parallelizable sub-tasks (map phase) and subsequently aggregate their outputs (reduce phase) within a stateful graph structure. This was illustrated through examples such as joke generation and text summarization.
Modifications made: Utilized Groq’s “openai/gpt-oss-120b” model for experimentation.Added screenshots showcasing LangSmith traces and the graph visualization in LangGraph Studio.Developed and implemented a custom example to reinforce understanding.Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%204/map-reduce.ipynb).

**Video 4 – Research Assistant**
Explored the process of building a lightweight, multi-agent research assistant using LangGraph. The session highlights core LangGraph concepts such as memory management, human-in-the-loop interaction, and controllability, which enable customization of the research workflow and the generation of a comprehensive final report based on parallelized expert interviews.Modifications made:Utilized Groq’s “openai/gpt-oss-120b” and “llama-3.1-8b-instant” models.Added LangSmith trace screenshots illustrating outputs generated during key steps such as write_section, finalize_report, and others.Code:[Link](https://github.com/SVGautham/S.V.Gautham-langgraph-MAT496/blob/main/Module%204/research_assistant.ipynb).
