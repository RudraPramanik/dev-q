FastAPI Production Backend
Architecture--------------------------------
1. Why should routers not contain business logic?
2. What is the difference between router, service, and repository layers?
3. Where should AI calls live in a FastAPI application?
4. How would you structure a FastAPI codebase that will grow to 100+ endpoints?
Dependency Injection--------------------------------
1. What problem does Depends() solve?
2. Why is dependency injection better than creating DB connections inside routes?
3. How would you inject an authenticated user into all protected routes?
Lifespan--------------------------------    
1. What should happen during startup?
2. What should happen during shutdown?
3. Why initialize vector stores and model clients during lifespan instead of per request?
Async--------------------------------
1. When should you use async vs sync?
2. What happens if a CPU-heavy task runs inside an async endpoint?
3. Why can a single blocking function hurt throughput?
Streaming--------------------------------
1. How does StreamingResponse work?
2. Why is streaming important for AI applications?
3. How would you stream token-by-token responses from an LLM?
Background Tasks--------------------------------
1. Which jobs belong in FastAPI BackgroundTasks?
2. Which jobs should move to a queue instead?