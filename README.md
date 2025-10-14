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
