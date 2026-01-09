# graphRAG using knowledge graph (neo4j), langchain, Phi4 (LLM)
Construction of the graphRAG agent requires three main service components: 
* a generative large language model (e.g., Phi4:14b),
* a sentence embedding model (e.g., mxbai-embed-large), and
* a graph database server (e.g., Neo4j).

Language models are accessible via API keys (potentially a paid service), Hugging Face pipelines,
or an Ollama server. The Neo4j requirement can be met either by using its cloud database services or by setting
up a local server using a container. A demonstration code for building a simple, small graph is available at
https://github.com/wdnlotm/graphRAG_neo4j_langchain_phi4

## knowledge graph database construction. 

The knowledge graph database is required to contain associated
textual data. Therefore, the input for knowledge graph construction is a corpus of texts. This corpus is processed
by the LLMGraphTransformer from LangChain, leveraging a large language model of choice. The resulting graph
elements—nodes and edges—are then stored in a Neo4j graph database. Properties for both nodes and edges
can be added to the database post hoc. This capability for post hoc database refinement is a powerful addition
to the graphRAG framework, as it allows for the precise entry of numeric values and handling of repeated terms,
areas where Large Language Models typically demonstrate weakness. The workflow schematic, along with an
example of the graph input and output, is displayed in Fig. 1.
![Fig. 1](figure/graph_building.png)
