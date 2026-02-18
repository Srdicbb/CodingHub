# Senior Developer Roadmap

> Personal roadmap for growing from Software Engineer II to Senior Developer and beyond.
> Created: 2026-02-18
>
> Legend:
> - [x] = Already have experience (from work projects)
> - [~] = Partial knowledge (used it but need deeper understanding)
> - [ ] = Need to learn from scratch
> - **PRIORITY** = High priority item to focus on

---

## Phase 1: Solidify Fundamentals (Months 1-3)

The foundation everything else builds on. Without this, you're building on sand.

### 1.1 Object-Oriented Programming (Deep Mastery)

- [~] **Four Pillars** - Encapsulation, Inheritance, Polymorphism, Abstraction **PRIORITY**
  - You use these daily in C#/.NET but need to articulate WHEN to use each and WHEN NOT to
  - Don't just know the definitions - know WHEN to use each and WHEN NOT to
- [~] **SOLID Principles** **PRIORITY**
  - Single Responsibility Principle
  - Open/Closed Principle
  - Liskov Substitution Principle
  - Interface Segregation Principle
  - Dependency Inversion Principle
  - You've applied these in .NET projects but need to formalize understanding
- [~] **Composition vs Inheritance** - why "favor composition over inheritance" exists
- [~] **Interfaces vs Abstract Classes** - when to use which and why
  - Used in C# daily, but deepen the "why" behind each choice
- [~] **Coupling and Cohesion** - tight vs loose coupling, high vs low cohesion
  - You dealt with tight coupling in the Israeli monolith - formalize this knowledge
- [x] **Dependency Injection** - constructor injection, IoC containers, why it matters for testing
  - Used AutoFac in FIS project, understand IoC containers in practice

### 1.2 Design Patterns

- [ ] **Creational Patterns** **PRIORITY**
  - Singleton (and why it's often an anti-pattern)
  - Factory Method
  - Abstract Factory
  - Builder
  - Prototype
- [ ] **Structural Patterns** **PRIORITY**
  - Adapter
  - Decorator
  - Facade
  - Proxy
  - Composite
  - Bridge
- [ ] **Behavioral Patterns**
  - Observer (you've used SignalR which is observer-like)
  - Strategy
  - Command
  - State
  - Template Method
  - Mediator
  - Iterator
- [ ] **When NOT to use patterns** - over-engineering recognition

### 1.3 Data Structures & Algorithms

- [~] **Core Data Structures**
  - Arrays, Linked Lists, Stacks, Queues
  - Hash Tables / Dictionaries (how they work internally)
  - Trees (Binary, BST, AVL, Red-Black)
  - Graphs (adjacency list vs matrix)
  - Heaps / Priority Queues
  - You use these in C# but need to understand internals
- [ ] **Algorithm Fundamentals** **PRIORITY**
  - Big O notation (Time and Space complexity)
  - Sorting algorithms (QuickSort, MergeSort, when to use which)
  - Searching (Binary Search, BFS, DFS)
  - Recursion and Dynamic Programming basics
- [~] **Practical application** - know which data structure to pick for real problems, not just theory

### 1.4 Clean Code Practices

- [~] **Naming** - variables, methods, classes that explain themselves
- [~] **Functions** - small, single purpose, minimal parameters
- [~] **Error Handling** - exceptions vs error codes, when to catch vs propagate
- [~] **Code Smells** - recognizing bad code (long methods, god classes, feature envy)
  - You refactored "poorly written services" in the Israeli project - you recognize smells
- [x] **Refactoring Techniques** - extract method, extract class, rename, move
  - Proven by your monolith-to-microservice proposal
- [~] **KISS, DRY, YAGNI** - understand the balance between them

---

## Phase 2: Software Architecture & System Design (Months 3-6)

This is what separates mid-level from senior. Seniors design systems, they don't just write functions.

### 2.1 Architectural Patterns

- [x] **Monolith vs Microservices** **PRIORITY - formalize what you already know**
  - When monolith is the RIGHT choice
  - When to migrate to microservices
  - The distributed monolith anti-pattern
  - You lived this: proposed breaking the 14-year-old Israeli monolith into microservices
- [x] **Layered Architecture** (N-Tier)
  - Presentation, Business Logic, Data Access
  - You work with this daily in FIS (Manager layer -> REST -> UI)
- [ ] **Clean Architecture / Hexagonal Architecture** **PRIORITY**
  - Domain-centric design
  - Ports and Adapters
  - Why dependency direction matters
- [~] **Event-Driven Architecture**
  - Event sourcing
  - CQRS (Command Query Responsibility Segregation)
  - Message brokers (RabbitMQ, Kafka basics)
  - You've used RabbitMQ in the crypto exchange project - deepen the concepts
- [ ] **Serverless Architecture** - when it makes sense, when it doesn't
- [ ] **Domain-Driven Design (DDD)** **PRIORITY**
  - Bounded contexts
  - Aggregates
  - Ubiquitous language
  - Domain events

### 2.2 System Design Skills

- [ ] **Scalability** **PRIORITY**
  - Horizontal vs Vertical scaling
  - Load balancing (Round Robin, Least Connections, Consistent Hashing)
  - Database sharding and partitioning
  - Read replicas
- [ ] **Caching**
  - Cache invalidation strategies (TTL, write-through, write-behind)
  - Redis / Memcached use cases
  - CDN caching
  - Application-level caching
- [x] **Databases**
  - SQL vs NoSQL - real tradeoffs, not just buzzwords
  - CAP Theorem
  - ACID properties
  - Database indexing (how indexes work, B-trees, when to index)
  - Query optimization
  - Connection pooling
  - You have deep MS SQL experience across multiple projects with EF, ADO.NET, Dapper
  - Still learn: CAP theorem, sharding, NoSQL tradeoffs
- [x] **API Design**
  - REST best practices (resource naming, status codes, versioning)
  - GraphQL - when it helps, when it hurts
  - gRPC - when to use over REST
  - API pagination, rate limiting, authentication
  - You designed REST endpoints for FIS, exposed Manager layer to UI
  - Still learn: GraphQL, gRPC, rate limiting patterns
- [ ] **System Design Practice Problems** **PRIORITY**
  - Design a URL shortener
  - Design a chat system
  - Design a notification service
  - Design a file storage system
  - Design a rate limiter

### 2.3 Distributed Systems Concepts

- [ ] **Consistency models** - eventual consistency, strong consistency
- [ ] **Consensus algorithms** - Raft, Paxos (high level)
- [ ] **Circuit Breaker pattern**
- [ ] **Retry strategies** - exponential backoff, jitter
- [ ] **Idempotency** - why it matters in distributed systems
- [ ] **Distributed tracing** - OpenTelemetry, correlation IDs

---

## Phase 3: DevOps & Infrastructure (Months 4-7)

Seniors understand the full lifecycle, not just the code.

### 3.1 Version Control (Advanced Git)

- [x] **Branching strategies** - GitFlow, trunk-based development, feature flags
  - You introduced PRs to the Israeli project team
- [~] **Rebasing vs merging** - when to use each
- [ ] **Cherry-picking, bisect, reflog** - advanced debugging with git
- [ ] **Conventional commits** - structured commit messages

### 3.2 CI/CD

- [x] **Pipeline design** - build, test, deploy stages
  - You set up Azure pipeline for daily Cypress tests
- [x] **GitHub Actions / Azure DevOps / Jenkins** (pick one, understand concepts)
  - You have Azure DevOps experience
- [x] **Automated testing in pipelines** - unit, integration, E2E
  - Configured Cypress + Cucumber in Azure pipeline
- [ ] **Deployment strategies** **PRIORITY**
  - Blue/Green deployment
  - Canary releases
  - Rolling updates
  - Feature flags for safe rollouts

### 3.3 Containers & Orchestration

- [x] **Docker**
  - Dockerfile best practices
  - Multi-stage builds
  - Docker Compose for local development
  - Image optimization
  - Used Docker in crypto exchange and other projects
- [ ] **Kubernetes (basics)** **PRIORITY**
  - Pods, Services, Deployments, ConfigMaps
  - When you need K8s vs when you don't
  - Helm charts basics

### 3.4 Cloud Services (Pick One: Azure/AWS/GCP)

- [~] **Compute** - VMs, App Services, Functions
  - You've used Azure DevOps, expand to Azure services
- [ ] **Storage** - Blob storage, queues, tables
- [ ] **Networking basics** - VNets, subnets, NSGs, load balancers
- [ ] **Monitoring & Observability** **PRIORITY**
  - Logging (structured logging, log aggregation)
  - Metrics (Prometheus, Grafana, Application Insights)
  - Alerting - what to alert on, alert fatigue
  - The three pillars: logs, metrics, traces

---

## Phase 4: Testing & Quality (Months 5-8)

Seniors write testable code and know what to test.

### 4.1 Testing Pyramid

- [~] **Unit Tests** **PRIORITY**
  - What to test, what NOT to test
  - Mocking, stubbing, faking - when to use each
  - Test naming conventions
  - Arrange-Act-Assert pattern
  - You wrote unit tests in crypto exchange project - deepen the discipline
- [~] **Integration Tests**
  - Testing with real databases (TestContainers)
  - API integration tests
  - When integration tests are more valuable than unit tests
- [x] **End-to-End Tests**
  - When to write them (sparingly)
  - Tools and frameworks
  - You set up Cypress + Cucumber E2E testing with Azure pipeline
- [ ] **Test-Driven Development (TDD)** **PRIORITY**
  - Red-Green-Refactor cycle
  - When TDD helps, when it's overkill

### 4.2 Code Quality

- [x] **Code reviews** - how to give and receive meaningful feedback
  - You introduced PRs to your team workflow
- [ ] **Static analysis tools** - linters, analyzers
- [~] **Technical debt** - identifying, measuring, communicating to stakeholders
  - You dealt with a 14-year-old monolith - you understand tech debt firsthand
- [ ] **Performance profiling** - identifying bottlenecks, memory leaks

---

## Phase 5: Security Fundamentals (Months 6-9)

Every senior must understand security. This is non-negotiable.

### 5.1 Application Security

- [ ] **OWASP Top 10** - know all of them, not just SQL injection and XSS **PRIORITY**
  - Injection (SQL, Command, LDAP)
  - Broken Authentication
  - Sensitive Data Exposure
  - XML External Entities (XXE)
  - Broken Access Control
  - Security Misconfiguration
  - Cross-Site Scripting (XSS)
  - Insecure Deserialization
  - Using Components with Known Vulnerabilities
  - Insufficient Logging & Monitoring
- [~] **Authentication & Authorization**
  - OAuth 2.0 / OpenID Connect flows
  - JWT - how they work, common mistakes
  - Session management
  - RBAC vs ABAC
  - You implemented JWT in crypto exchange project
- [ ] **Prompt Injection** (new attack vector)
  - How it works in AI-powered applications
  - Direct vs indirect prompt injection
  - Mitigation strategies
- [~] **HTTPS, TLS, Certificates** - how they actually work
  - You implemented public-private key crypto for IoT sensor data
- [x] **CORS** - what it is, why it exists, how to configure properly
  - You deal with this in Angular + .NET projects
- [ ] **Secrets management** - never hardcode secrets, use vaults

### 5.2 Secure Coding Practices

- [~] **Input validation** - whitelist over blacklist
- [x] **Parameterized queries** - always, no exceptions
  - You use EF, Dapper, ADO.NET - you know this
- [ ] **Principle of least privilege**
- [ ] **Security headers** - CSP, HSTS, X-Frame-Options
- [ ] **Dependency scanning** - keeping packages updated, vulnerability monitoring

---

## Phase 6: AI & LLM Ecosystem (Months 7-10)

This is the future. Understanding AI at an engineering level is your competitive advantage.

### 6.1 Understanding AI/LLM Fundamentals

- [ ] **How LLMs work (conceptual)** **PRIORITY**
  - Transformers architecture (high level)
  - Tokenization - what it is, why it matters
  - Context windows - what they are, limitations
  - Temperature, top-p, top-k - what these parameters do
  - Why AI "hallucinates" - understanding the probability game
- [ ] **Model types and sizes**
  - Difference between GPT, Claude, Llama, Mistral families
  - Parameters (7B, 13B, 70B) - what they mean practically
  - Quantization (Q4, Q8, GGUF) - tradeoff between quality and speed
  - Fine-tuned vs base models
- [~] **Local AI with LM Studio / Ollama**
  - Setting up local inference
  - Downloading models from Hugging Face
  - When local models make sense vs API calls
  - Hardware requirements (GPU, VRAM, RAM)
  - You discussed this with friends - already exploring
- [ ] **Prompt Engineering** **PRIORITY**
  - System prompts, user prompts, assistant messages
  - Few-shot vs zero-shot prompting
  - Chain-of-thought prompting
  - Structured output (JSON mode)

### 6.2 RAG (Retrieval-Augmented Generation)

- [ ] **What RAG is and why it exists** **PRIORITY**
  - LLM knowledge cutoff problem
  - Grounding AI responses in your data
  - RAG vs fine-tuning - when to use which
- [ ] **RAG Pipeline**
  - Document loading and chunking strategies
  - Chunk size, overlap - why they matter
  - Embedding models (OpenAI, local alternatives)
  - Retrieval strategies (similarity search, MMR, hybrid search)
  - Context stuffing and prompt construction
  - Re-ranking retrieved results
- [ ] **Building a RAG system**
  - End-to-end implementation
  - Evaluation metrics (relevance, faithfulness, answer quality)
  - Common failure modes and how to fix them

### 6.3 Vector Databases

- [ ] **What are vector embeddings** **PRIORITY**
  - How text becomes numbers (embedding models)
  - Similarity search (cosine similarity, dot product, euclidean distance)
  - Why traditional databases can't do this efficiently
- [ ] **Vector Database Options**
  - Pinecone - managed, easy to start
  - Weaviate - open source, feature rich
  - ChromaDB - lightweight, good for prototypes
  - pgvector - PostgreSQL extension (use what you know)
  - Qdrant - performance focused
  - Milvus - enterprise scale
- [ ] **Vector DB operations**
  - Indexing strategies (HNSW, IVF)
  - Metadata filtering
  - Hybrid search (vector + keyword)
  - Scaling considerations

### 6.4 MCP (Model Context Protocol)

- [ ] **What MCP is** **PRIORITY**
  - Anthropic's standard for connecting AI to external tools
  - Client-server architecture
  - Why it matters for AI application development
- [ ] **MCP Components**
  - Tools - functions AI can call
  - Resources - data AI can access
  - Prompts - reusable prompt templates
- [ ] **Building MCP Servers**
  - Setting up an MCP server
  - Defining tools with schemas
  - Connecting to Claude Desktop / Claude Code
  - Security considerations
- [ ] **Practical MCP use cases**
  - Database access through MCP
  - File system operations
  - API integrations
  - Custom business logic tools

### 6.5 AI-Augmented Development

- [~] **Using AI as a coding partner**
  - Claude Code, GitHub Copilot, Cursor - strengths and weaknesses
  - Effective prompting for code generation
  - Reviewing AI-generated code critically
  - Knowing when AI output is wrong
  - You used Lavaable AI for React frontend in ESG project
- [ ] **AI Security awareness**
  - Prompt injection attacks and defenses
  - Data leakage through AI tools
  - Supply chain risks with AI-generated code
  - Responsible AI usage in enterprise

---

## Phase 7: Soft Skills & Leadership (Ongoing)

Technical skills get you to senior. These skills keep you there.

### 7.1 Communication

- [ ] **Technical writing** - clear documentation, RFCs, design docs
- [~] **Explaining complex topics simply** - to PMs, stakeholders, junior devs
- [x] **Knowing when to push back** - saying no to bad ideas with data
  - You proposed architectural changes to the Israeli monolith and introduced PRs
- [~] **Async communication** - clear PR descriptions, Slack messages, emails

### 7.2 Mentorship & Team Impact

- [~] **Code review as teaching** - not just "approve" or "change this"
- [ ] **Pair programming** - know when to lead and when to observe
- [x] **Helping juniors grow** - this multiplies your impact
  - You mentor interns at Tiac on ESG initiatives
- [ ] **Knowledge sharing** - tech talks, documentation, brown bags

### 7.3 Project & Decision Making

- [~] **Estimation** - breaking down work, identifying unknowns
- [x] **Trade-off analysis** - speed vs quality, build vs buy
  - You evaluated ADO.NET vs Dapper migration, monolith vs microservices
- [ ] **Technical decision documentation** - ADRs (Architecture Decision Records)
- [ ] **Stakeholder management** - translating business needs to technical solutions
- [~] **Owning outcomes** - not just tasks, but the result

### 7.4 Career Strategy

- [ ] **Build a public presence** - blog, GitHub, tech talks (even small ones) **PRIORITY**
- [ ] **Understand the business** - why does your company make money?
- [~] **Network** - not for job hunting, for learning and staying current
  - You discuss tech with friends - expand this deliberately
- [x] **Stay curious** - the best seniors never stop being students
  - You're building this roadmap - that proves it

---

## Phase 8: Understanding the Full Stack (From Metal to Browser)

Knowing what happens under the hood makes you a better engineer at every level.

### 8.1 How Computers Actually Work

- [x] **Machine code** - binary instructions the CPU executes directly
  - You wrote Linux kernel drivers and worked with FPGA - you know the metal
- [x] **Assembly language** - human-readable machine code (1:1 mapping)
  - Embedded systems background at RT-RK
- [x] **Why high-level languages exist** - languages are for HUMANS, not computers
  - You discussed this with friends - you get this concept
- [~] **The compilation chain**
  - Source code -> Compiler -> Intermediate Language (IL/bytecode) -> Machine code
  - .NET: C# -> IL -> JIT compiled to machine code
  - Java: Java -> Bytecode -> JVM JIT compiled to machine code
  - Go: Go -> Machine code (ahead-of-time compiled)
  - JavaScript: Interpreted -> JIT compiled (V8 engine)
  - You know the .NET chain, learn the others
- [x] **Managed vs Unmanaged code** - garbage collection, memory management
  - You've worked in both worlds: C (unmanaged at RT-RK) and C# (managed)
- [~] **Why AI won't write machine code directly**
  - Abstraction exists for maintainability, not performance
  - The bottleneck is rarely the language, it's the design
  - Machine code is CPU-specific (x86, ARM) - not portable

### 8.2 Networking Fundamentals

- [~] **TCP/IP stack** - what happens when you type a URL
- [~] **DNS** - how domain resolution works
- [x] **HTTP/HTTPS** - request/response cycle, headers, methods
  - You build REST APIs daily
- [x] **WebSockets** - real-time communication
  - You use SignalR (WebSocket abstraction) in FIS project
- [~] **REST vs gRPC vs GraphQL** - protocol level understanding
  - You know REST deeply, learn gRPC and GraphQL

---

## Your Experience Summary

Based on your CV, here's what you bring to the table:

| Skill Area | Level | Source |
|-----------|-------|--------|
| C# / .NET | Strong | 4+ years across multiple projects |
| MS SQL Server | Strong | EF, ADO.NET, Dapper - all three ORMs |
| Angular / React / TypeScript | Solid | Frontend across multiple projects |
| Docker | Working knowledge | Used in crypto exchange, other projects |
| RabbitMQ | Basic-Intermediate | Crypto exchange project |
| SignalR / Real-time | Solid | FIS project, ESG project |
| IoT / Embedded | Unique advantage | ESP32, MQTT, sensor integration, Linux drivers |
| CI/CD (Azure DevOps) | Solid | Set up pipelines, automated tests |
| E2E Testing (Cypress) | Solid | Introduced testing culture to a team |
| Mentoring | Active | Currently mentoring interns |
| System Architecture | Growing | Proposed monolith breakup, designed IoT platform |
| Cryptography basics | Working | Public-private key for IoT data |
| Low-level programming | Background | Linux kernel drivers, FPGA, CAN communication |

**Your unique combination**: .NET full-stack + embedded systems + IoT + AI curiosity. Very few developers have this range.

---

## Daily Habits for Growth

These compound over time. Small consistent effort beats occasional sprints.

1. **Read code daily** - open source projects, your team's code, AI-generated code
2. **Write code daily** - even 30 minutes of deliberate practice
3. **Review code thoughtfully** - don't rubber stamp, actually think about design
4. **Learn one new thing weekly** - a concept, a tool, a pattern
5. **Teach something monthly** - blog post, team presentation, mentor a junior
6. **Build side projects** - apply what you learn in a low-stakes environment
7. **Question AI output** - every time AI generates code, ask "is this right? is this the best way?"

---

## Recommended Resources

### Books
- Clean Code - Robert C. Martin
- Design Patterns - Gang of Four (reference, don't read cover to cover)
- Designing Data-Intensive Applications - Martin Kleppmann (system design bible)
- The Pragmatic Programmer - David Thomas, Andrew Hunt
- System Design Interview - Alex Xu

### Practice
- System design: practice whiteboard problems weekly
- LeetCode: focus on medium difficulty, understand patterns not memorization
- Build projects: a RAG chatbot, an MCP server, a microservice with proper CI/CD

### Stay Current
- Follow engineering blogs (Netflix, Uber, Stripe tech blogs)
- Listen to tech podcasts during commute
- Join communities (Discord servers, Reddit r/ExperiencedDevs)

---

## Progress Tracker

| Phase | Status | Started | Completed |
|-------|--------|---------|-----------|
| Phase 1: Fundamentals | Partial - deepening needed | | |
| Phase 2: Architecture & System Design | Partial - have practical experience, need formal knowledge | | |
| Phase 3: DevOps & Infrastructure | Partial - Docker/CI done, need K8s/cloud/monitoring | | |
| Phase 4: Testing & Quality | Partial - E2E done, need unit testing discipline & TDD | | |
| Phase 5: Security | Mostly new - have JWT/crypto basics | | |
| Phase 6: AI & LLM Ecosystem | Starting - high interest | | |
| Phase 7: Soft Skills | Active - mentoring, proposing changes | | |
| Phase 8: Full Stack Understanding | Strong base - embedded background | | |

---

> **Remember**: The goal is not to check every box. The goal is to understand deeply enough that you can make good decisions, evaluate AI output, design systems, and lead others. A senior developer is not someone who knows everything - it's someone who knows how to figure out anything and makes the people around them better.
