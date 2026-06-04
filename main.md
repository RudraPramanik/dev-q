Day 1 — FastAPI Production Backend
Architecture
Why should routers not contain business logic?
What is the difference between router, service, and repository layers?
Where should AI calls live in a FastAPI application?
How would you structure a FastAPI codebase that will grow to 100+ endpoints?
Dependency Injection
What problem does Depends() solve?
Why is dependency injection better than creating DB connections inside routes?
How would you inject an authenticated user into all protected routes?
Lifespan
What should happen during startup?
What should happen during shutdown?
Why initialize vector stores and model clients during lifespan instead of per request?
Async
When should you use async vs sync?
What happens if a CPU-heavy task runs inside an async endpoint?
Why can a single blocking function hurt throughput?
Streaming
How does StreamingResponse work?
Why is streaming important for AI applications?
How would you stream token-by-token responses from an LLM?
Background Tasks
Which jobs belong in FastAPI BackgroundTasks?
Which jobs should move to a queue instead?
Day 2 — LangGraph
Fundamentals
What is state?
Why is state the most important object in LangGraph?
How does LangGraph differ from a simple prompt chain?
Nodes
What should a node do?
What should a node not do?
Why should nodes be small and deterministic?
State Management
What belongs in graph state?
What should not be stored in graph state?
How can state become a bottleneck?
Persistence
What is a checkpointer?
Why would you persist graph state?
How would you resume a workflow after a crash?
Human in the Loop
What is an interrupt?
When should a workflow stop and request approval?
What actions should never happen without approval?
Multi-Agent
When should you create another agent?
When should you NOT create another agent?
Why do many multi-agent systems become slower rather than smarter?
Day 3 — RAG
Fundamentals
What problems does RAG solve?
Why is RAG often better than fine-tuning?
What kinds of knowledge should live in RAG?
Chunking
Why do we chunk documents?
What makes a chunk "good"?
What problems occur when chunks are too large?
What problems occur when chunks are too small?
Metadata
Why is metadata important?
Which metadata fields should every chunk have?
How can metadata improve retrieval quality?
Retrieval
What happens during retrieval?
What is top-k retrieval?
Why can retrieval fail even when the correct document exists?
Reranking
What problem does reranking solve?
Why not just increase top-k forever?
Citations
Why should AI answers include citations?
How would you trace an answer back to a source chunk?
Day 4 — Qdrant
Collections
What is a collection?
When should you create multiple collections?
Vectors
Why must vector dimensions match?
Why should a collection use one embedding model?
Payload
What is payload metadata?
Why is payload filtering important?
Multitenancy
How would you separate customer data?
Collection per tenant vs payload filters?
Hybrid Search
What is dense search?
What is keyword search?
Why combine both?
Operations
What is a snapshot?
Why are aliases useful?
How would you migrate collections without downtime?
Day 5 — Embeddings + OpenAI Cookbook
Embeddings
What is an embedding?
Why do semantically similar texts produce similar vectors?
Why are embeddings generated offline instead of per request?
Embedding Pipeline
What happens from raw document → vector DB?
Where should chunking happen?
Where should embedding happen?
Updating Data
What happens when a document changes?
Why use content hashes?
Structured Outputs
Why are structured outputs better than free-form text?
What problems do JSON schemas solve?
Reliability
How would you handle retries?
How would you handle rate limits?
Why should embedding requests be batched?
Day 6 — Observability (Langfuse)
Fundamentals
Why is observability different from logging?
What questions should observability answer?
Traces
What is a trace?
What should a trace contain?
AI Pipeline
Which steps should be traced?
User
 ↓
Retriever
 ↓
Reranker
 ↓
LLM
 ↓
Response
Failure Analysis
How would you determine if a bad answer came from:
retrieval?
reranking?
prompting?
model?
Metrics
What metrics would you track?
What metrics matter to business stakeholders?
What metrics matter to engineers?
Production
How would tracing help debug a customer complaint?
Day 7 — Evaluation
Foundations
Why is manual testing insufficient?
What is a golden dataset?
Retrieval Evaluation
How do you know retrieval is working?
How do you measure retrieval quality?
RAG Evaluation
What is faithfulness?
What is answer relevance?
What is context precision?
What is context recall?
Regression Testing
What is a regression?
Why should evaluations run in CI/CD?
Production Evaluation
What happens when retrieval quality drops after deployment?
How would you catch that automatically?
Startup-Level Thinking
What should block deployment?
What should trigger an alert?
What metrics would indicate your AI system is getting worse?
Final "Senior Engineer" Check

If after these 7 days you can confidently answer:

Why retrieval failed
Why chunking failed
Why an agent got stuck
Why latency increased
Why answers hallucinated
Why deployment degraded quality
How to measure and prevent all of the above

then you've moved beyond "AI app builder" territory and into the foundations of a production AI/backend engineer.

Those are exactly the kinds of questions that come up when you're responsible for shipping and maintaining a real AI startup system