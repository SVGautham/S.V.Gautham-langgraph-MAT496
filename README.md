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
