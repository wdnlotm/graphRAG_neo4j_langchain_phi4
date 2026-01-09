# graphRAG using knowledge graph (neo4j), langchain, Phi4 (LLM)
Construction of the graphRAG agent requires three main service components: 
* a generative large language model (e.g., Phi4:14b),
* a sentence embedding model (e.g., mxbai-embed-large), and
* a graph database server (e.g., Neo4j).

Language models are accessible via API keys (potentially a paid service), Hugging Face pipelines,
or an Ollama server. The Neo4j requirement can be met either by using its cloud database services or by setting
up a local server using a container. A demonstration code for building a simple, small graph is available at
https://github.com/wdnlotm/graphRAG_neo4j_langchain_phi4
