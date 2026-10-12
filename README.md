# Halil Kuzu

AI Engineer based in Erlangen, Germany. M.Sc. in Artificial Intelligence from FAU Erlangen-Nürnberg.

I build applied AI software: retrieval-augmented generation, LLM agents and tool servers, text classification, ML services and machine learning on industrial sensor data.

## Projects

**[rag-doc-qa](https://github.com/ihkuzu/rag-doc-qa)**: question answering over PDFs with page-level citations. Python, FastAPI, PostgreSQL with pgvector, Docker, GitHub Actions. Includes a retrieval evaluation (hit@k, MRR) and works with local or hosted models.

**[sql-agent](https://github.com/ihkuzu/sql-agent)**: tool-using LLM agent that answers questions about a SQLite database. Tool loop with error recovery, read-only guards, a 12-question evaluation (a small local model went from 17% to 67% after fixing the failures it exposed) and 72 tests that need no model. Python, Ollama or Gemini, Docker, GitHub Actions.

**[german-news-classifier](https://github.com/ihkuzu/german-news-classifier)**: German news topic classification done three ways on one test set. A TF-IDF baseline reaches 88.7% accuracy in seconds, a fine-tuned German BERT 90.7% (mean of four runs), a zero-shot prompt to a small local LLM 48%, with training and inference cost measured for each. Python, scikit-learn, PyTorch, Hugging Face Transformers, GitHub Actions.

**[async-inference-service](https://github.com/ihkuzu/async-inference-service)**: queue-based ML inference service. Jobs go through a FastAPI endpoint into a Redis queue; a worker groups them into batches, retries failures, dead-letters the hopeless ones and shuts down gracefully. Idempotency keys, Prometheus metrics, a benchmark (without batching one worker tops out at 43 jobs/s, with batches of 8 it keeps up with 150 jobs/s at p95 under 100 ms, measured with a simulated model) and 41 tests that run against a real Redis. Python, Redis, Docker Compose, GitHub Actions.

**[mcp-knowledge-server](https://github.com/ihkuzu/mcp-knowledge-server)**: MCP server that lets LLM clients search internal documents, query a sales database and submit jobs to the inference service above. Typed tool schemas, read-only SQL enforced by the database engine (read-only file, authorizer, timeouts and size caps), errors the model can recover from, bearer-token auth for HTTP, a search evaluation with unanswerable questions and 61 tests including a real stdio session. Python, MCP SDK, SQLite, Docker, GitHub Actions.

**[MADE-Project](https://github.com/ihkuzu/MADE-Project)**: data pipeline that analyzes how weather affects traffic accidents in New York City. Python, pandas, SQLite, automated tests and CI.

## Experience

- Software & AI Engineer, BIMraum GmbH (2026 to now): full-stack features with Next.js and NestJS for an AI-driven quantity take-off platform.
- Software & AI Engineer, Innomotics (2024 to 2025): data pipelines and predictive models for industrial converter systems.

## Tech

Python, PyTorch, scikit-learn, TypeScript, C#, SQL, FastAPI, MCP, PostgreSQL, Redis, Docker, Next.js, NestJS, Linux, Git
