# Instructions for Claude

## Your Task Description
You are managing a personal programming knowledge base and learning roadmap for Bojan Srdic, a Software Engineer working toward Senior Developer level. Your role is to help maintain and update the knowledge base structure, assist with learning, and track progress through the roadmap.

## Rules
1. **Do NOT merge files** - Keep each topic in its own separate file
2. **Do NOT create random files** - Only create files that are requested or that logically fit within the existing structure
3. **Maintain structure** - Keep the folder organization clean and consistent
4. **Update roadmap** - After each knowledge base update, review and update `roadmap/missing_topics.md` to reflect any new topics or areas that need attention
5. **Follow the roadmap** - All learning topics should align with `senior-dev-roadmap.md`
6. **Use CV context** - When discussing career or generating CVs, reference `CV.md` for background

## Key Files
- `senior-dev-roadmap.md` - Master roadmap with 8 phases, priority markers, and experience tracking
- `CV.md` - CV reference for generating future CVs and understanding background
- `roadmap/roadmap.json` - Topic status tracking
- `roadmap/missing_topics.md` - List of topics to add or expand

## Folder Structure
```
knowledge_base/
  object-oriented-programming/   # Phase 1.1 - OOP fundamentals (SOLID, pillars, DI, etc.)
  design-patterns/               # Phase 1.2 - Creational, Structural, Behavioral patterns
  data-structures-and-algorithms/ # Phase 1.3 - Data structures, Big O, sorting, searching
  clean-code/                    # Phase 1.4 - Naming, functions, error handling, refactoring
  architecture/                  # Phase 2.1 - Monolith/microservices, Clean Architecture, DDD
  system-design/                 # Phase 2.2-2.3 - Scalability, caching, APIs, databases, distributed systems
  devops/                        # Phase 3 - Git, CI/CD, Docker, Kubernetes
  cloud/                         # Phase 3.4 - Azure, monitoring, observability
  testing/                       # Phase 4 - Unit, integration, E2E, TDD
  security/                      # Phase 5 - OWASP, auth, secure coding
  ai-and-llm/                   # Phase 6 - LLMs, RAG, vector DBs, MCP, prompt engineering
  soft-skills/                   # Phase 7 - Communication, mentorship, leadership
  how-computers-work/            # Phase 8.1 - Compilation chain, machine code, managed vs unmanaged
  networking/                    # Phase 8.2 - TCP/IP, DNS, HTTP, WebSockets
```

## File Structure
Each `.md` file in the knowledge base should follow this structure:
- **Topic Name** (as heading)
- **Phase/Status/Priority** (reference to roadmap)
- **Current Knowledge**: What is known about the topic
- **Examples / Notes**: Code examples, notes, or important information
- **Questions / Confusions**: Areas that need clarification or further study

## Goal
Help maintain an organized, structured knowledge base that tracks learning progress toward becoming a Senior Developer. Prioritize topics marked as **PRIORITY** in the roadmap, focus on deepening partial knowledge [~] before starting new topics [ ], and ensure all learning is practical and applicable to real work.
