### Hi, I'm Vivek Manik Warkad 👋

I’m a third-year undergraduate at **IIT Kanpur** who loves building systems from scratch and going deep into how backend infrastructure operates under the hood. My core focus is **distributed systems, concurrency, and low-latency backend engineering in Go**, alongside **AI-integrated backend architectures**.

I’m also a systematic user of AI in my daily engineering workflow—using architectural clarity, strict failure-mode analysis, and deterministic testing harnesses to ship and verify complex systems faster.

---

### 🏗️ Featured Systems & Architectures

* **[Distributed In-Memory Cache Cluster](https://github.com/VivekWar/distributed-cache-cluster)** (`Go`, `Docker Compose`, `Consistent Hashing`, `TCP/HTTP`)  
  Fault-tolerant 5-node in-memory cache cluster using a consistent-hash ring (100 virtual nodes/node), $O(\log N)$ routing, coordinator streaming via `io.Copy`, LRU eviction + TTL expiry, and 5s heartbeat failover. Benchmarked at **13k read / 12k write RPS** ($P95 < 20\text{ms}$, $P99 < 30\text{ms}$) across 100k operations with zero errors and race-free execution under `go test -race`.

* **[Serverless Tournament Scheduling System](https://github.com/VivekWar/tournament-scheduling-manager)** (`Go`, `AWS Lambda`, `DynamoDB`, `Terraform`, `API Gateway`, `EventBridge`, `SNS`)  
  Event-driven serverless backend across 8 Go Lambdas, 6 DynamoDB tables, and REST + WebSocket gateways provisioned via Terraform IaC. Features a Saga pattern scheduler (`attribute_not_exists` venue lock $\rightarrow$ GSI overlap check $\rightarrow$ compensating rollback), optimistic concurrency control with exponential backoff, and paginated EventBridge sweeps. Benchmarked on local cloud (Floci) at **206 RPS** ($P50\ 9.1\text{ms}$, $P95\ 33\text{ms}$, 0% error rate).

* **[Materials Mind — Hybrid RAG Engine](https://github.com/VivekWar/materials-mind)** ([**Live App**](https://materials-mind.rans45v.workers.dev) | `Go (Gin)`, `PostgreSQL + pgvector`, `Redis`, `React 18`, `TypeScript`, `Docker`)  
  Concurrent Go API and React 18 SPA over a 500-material database. Fans out hybrid SQL + HNSW vector search via goroutines/channels, pairs an in-memory $O(N \times d)$ cosine semantic cache (300-item LRU, sub-5ms lookup) with SHA-256 SSE response caching, and enforces a self-healing citation guardrail (0 hallucinated citations, $P99 < 300\text{ms}$, 94% latency reduction on cache hits).

---

### 🛠️ Technical Stack

* **Languages:** Go (Golang), C++, C, Python, TypeScript, JavaScript, SQL
* **Backend & Distributed Systems:** Concurrency (Goroutines, Channels, Mutexes), Consistent Hashing, Saga Pattern, REST, WebSockets, Server-Sent Events (SSE), OAuth 2.0 / JWT
* **Cloud, Databases & Infra:** AWS (Lambda, DynamoDB, API Gateway, SNS, EventBridge), PostgreSQL (`pgvector`), Redis (Upstash), Firebase, Docker, Terraform (IaC), Linux, Git

---

### 📫 Reach Out
* **Seeking:** Winter 2026 (Remote / Hyderabad) & Summer 2027 Backend / Distributed Systems / AI-Infra Internships
* **Email:** [vivekmw24@iitk.ac.in](mailto:vivekmw24@iitk.ac.in) | [vivekwarkad017@gmail.com](mailto:vivekwarkad017@gmail.com)
* **LinkedIn:** [linkedin.com/in/vivek-warkad](https://www.linkedin.com/in/vivek-warkad/)
