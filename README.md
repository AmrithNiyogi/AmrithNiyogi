# Amrith Niyogi

```text
role      ai engineer ii
research  phd, context engineering for llms · christ university
paper     "analysis of asr for domain-specific content" · scmim, springer
location  bengaluru, in
focus     agent runtimes · retrieval · llm platform infrastructure
open to   open source — issues, reviews, maintenance
```

I build the systems production AI depends on, not the demos on top of them:
framework-agnostic agent runtimes, RAG and document ingestion, prompt versioning
and evaluation, and the multi-tenant data and observability layer underneath.

I care as much about how these systems fail as how they work. That's also why I'm writing a Git-like version control system from scratch - reading about content-addressed storage teaches you less than being forced to get the edge cases right.

## Systems

- A **framework-agnostic agent runtime** over CrewAI, LangChain and LangGraph - three callback models normalised into one execution-log shape, so an agent definition runs on any of them without a rewrite
- **Prompt versioning** with typed Jinja variables on a Redis-cached read path, removing a database round-trip from every LLM call
- **Evaluation that changes without a deploy** — embedding-based prompt clustering and LLM-as-a-judge with database-driven rubrics
- A **trace pipeline** off a RabbitMQ topic exchange into per-tenant ClickHouse, batched with bulk acknowledgement and moved off the request path - so the trace sink can neither slow nor fail a user-facing LLM call

## Stack


|                  |                                                                                                       |
| ---------------- | ----------------------------------------------------------------------------------------------------- |
| **agents & llm** | LangGraph · LangChain · CrewAI · LlamaIndex · LiteLLM · Langfuse · MCP servers · Claude & OpenAI APIs |
| **data**         | ClickHouse · PostgreSQL · Qdrant · Neo4j · Redis · RabbitMQ                                           |
| **platform**     | Python · FastAPI · SSE · Docker · Kubernetes · Grafana · pytest                                       |


## Open source

Three areas I want to contribute to:

- **MCP servers and agent tooling** — protocol plumbing, transport edge cases, error surfaces
- **Evaluation and observability** — harnesses and trace tooling that turn "seems fine" into a number
- **Retrieval infrastructure** — graph-backed and hybrid retrieval, chunking strategy, recall measurement

Happy to start small — triage, docs, reviews. Open an issue on any repo of mine, or mail me.

Public experiments:
[agentic graph RAG](https://github.com/AmrithNiyogi/agentic-graph-rag-poc) ·
[guardrails](https://github.com/AmrithNiyogi/guardrails-ai-poc) ·
[TOON vs JSON token cost](https://github.com/AmrithNiyogi/toon-demo) ·
[system design notes](https://github.com/AmrithNiyogi/System-Design-Learning)







## Contact

[writing](https://medium.com/@amrithniyogi) ·
[linkedin](https://linkedin.com/in/amrith-niyogi) ·
[mail](mailto:amrithniyogi25@gmail.com)