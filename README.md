<img src="assets/hero.svg" alt="Vlad: fullstack, ML infrastructure and AI engineer" width="100%" />

I work across the whole stack. I build product interfaces and APIs, connect services through queues, run models on GPUs in production, and build LLM agents that work on real data. I take a feature from the first schema to the dashboard that shows it running.

### Backend and microservices

Async services in Python and Node that talk through events, scale on their own and fail without taking neighbours down.

<details>
<summary><b>How I build services</b></summary>
<br/>

- **FastAPI as the default.** Async endpoints on SQLAlchemy 2.0 and Pydantic V2, typed from the database model to the OpenAPI schema, so the client is generated rather than written by hand.
- **NestJS where the team lives in TypeScript.** Modules, guards and DTO validation, the same service boundaries as on the Python side.
- **Service boundaries first.** I split a system by data ownership: each service owns its tables and nobody reads them directly.
- **Events between services.** Kafka for streams that several consumers read, RabbitMQ for task queues with routing and dead-letter handling.
- **gRPC inside, REST outside.** Typed contracts between services, REST and OpenAPI for clients and partners, WebSocket for live updates.
- **Background jobs.** Long work moves out of the request into workers with retries and timeouts, so the API keeps answering fast.
- **SSO built from scratch.** One auth service shared by several products: JWT access and refresh tokens, OAuth2 flows, roles checked at the gateway.
- **Redis** for caching, rate limits and short-lived state.
- **Delivery included.** Docker images, CI/CD in GitHub Actions, servers set up with Ansible, metrics and logs in Prometheus, Grafana and Loki.

</details>

### AI systems

Agents on LangChain, LangGraph and Agno that call real tools, find the right context and stay within guardrails.

<details>
<summary><b>What I use and how</b></summary>
<br/>

- **LangGraph for stateful agents.** The agent is a graph with explicit states, branches and retries instead of one long prompt, so its behaviour can be read and tested.
- **Agno for multi-agent teams.** Agents with separate roles and tools that hand work to each other.
- **LangChain** for model wrappers, retrievers and integrations.
- **Tool calling and MCP.** I write tools and MCP servers that give agents access to internal APIs and data.
- **RAG on Qdrant.** Chunking and embeddings tuned for the documents at hand, metadata filters, answers with references to sources.
- **Hybrid search with reranking.** BM25 together with vector search, then a cross-encoder reranks the candidates.
- **Guardrails.** Input checks, structured output validated with Pydantic, limits on what tools an agent may call.
- **Tracing and evals.** Every agent run is traced in LangSmith or Langfuse; quality is checked on test sets and with LLM-as-judge before a change ships.

</details>

### ML in production

Models that run on GPUs in real time, wired into live video.

<details>
<summary><b>What that involves</b></summary>
<br/>

- **GPU inference.** PyTorch models exported to ONNX and compiled with TensorRT, batched and run in fp16.
- **Computer vision.** Person detection and pose estimation on every frame of a live stream.
- **Live video.** Ingest over SRT, overlays rendered on top of the video, output over SRT and HLS.
- **Measured quality.** Model thresholds are calibrated on labelled data and checked on every change.
- **Monitoring.** Latency, GPU load and detector state in Prometheus and Grafana.

</details>

### Stack

<table>
  <tr><td width="140">Web and Node</td><td><img src="assets/stack-product.svg" height="40" alt="TypeScript, React, Next.js, Tailwind, Node.js, NestJS" /></td></tr>
  <tr><td>Backend and data</td><td><img src="assets/stack-backend.svg" height="40" alt="Python, FastAPI, PostgreSQL, Redis, MongoDB, Kafka, RabbitMQ" /><br/>also SQLAlchemy 2.0, Pydantic V2, gRPC, WebSocket</td></tr>
  <tr><td>ML and AI</td><td><img src="assets/stack-ml.svg" height="40" alt="PyTorch, OpenCV, scikit-learn" /><br/>also LangChain, LangGraph, Agno, MCP, Qdrant, ONNX, TensorRT</td></tr>
  <tr><td>Infra</td><td><img src="assets/stack-ops.svg" height="40" alt="Docker, GitHub Actions, Ansible, Nginx, Prometheus, Grafana, Linux" /><br/>also Loki</td></tr>
</table>

### Contact

<a href="https://t.me/kuyltep"><img src="assets/telegram.svg" alt="Telegram @kuyltep" /></a>
<a href="mailto:vladpetlu91@gmail.com"><img src="assets/email.svg" alt="Email vladpetlu91@gmail.com" /></a>

Open to new roles. Message me on Telegram, that gets the fastest reply.
