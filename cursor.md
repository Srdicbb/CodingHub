# CURSOR.md – Project Instructions for AI Assistants

## Critical Rules (MUST FOLLOW)

### DO NOT CHANGE PROJECT STRUCTURE
- NEVER rename folders
- NEVER merge files
- NEVER move files between folders
- NEVER create files outside predefined folders unless explicitly instructed

### Markdown-Only Rule
- Work ONLY with `.md` files
- Do NOT introduce other file formats
- Do NOT embed code unless explicitly asked

### Non-Destructive Updates
- NEVER delete my existing notes
- ONLY append, clarify, or reorganize inside allowed sections
- If something is wrong or unclear, add a note instead of overwriting

## Project Overview

**Personal Programming Knowledge Base & Learning Roadmap**

This project is a long-term, structured learning system for programming and software engineering topics.

The goal is to:
- Capture what I already know
- Identify knowledge gaps
- Maintain a clear learning roadmap
- Continuously evolve without losing history

**This is not a codebase.**
**This is a thinking + learning system.**

### High-Level Goals
- Maintain a clean, structured knowledge base
- Detect missing fundamentals and advanced topics
- Suggest what to learn next in the correct order
- Keep everything human-readable and version-controlled (Git)

## Directory Structure

```
knowledge_base/
├── object-oriented-programming/
├── system-design/
├── angular/
├── dotnet/
└── AI/

roadmap/
├── roadmap.json
└── missing_topics.md
```

## Knowledge Base Rules

### Folder Meaning
- Each folder = one major domain
- Example: `system-design`, `dotnet`, `AI`

### File Meaning
- Each `.md` file = one atomic concept
- Example:
  - `inheritance.md`
  - `dependency-injection.md`
  - `http-caching.md`

### Mandatory File Structure

Every `.md` file MUST follow this structure:

```markdown
# Topic Name

## Current Knowledge
- What I understand today

## Examples / Notes
- Examples, mental models, summaries

## Questions / Confusions
- What is unclear or incomplete
```

🚫 Never invent new sections
🚫 Never remove sections
✅ You may add bullet points inside sections

## Roadmap Rules

### `roadmap/roadmap.json`
- Represents progress state
- Allowed statuses:
  - `not_started`
  - `learning`
  - `understood`
  - `needs_review`
- Example:
```json
{
  "topics": [
    {
      "name": "Object-Oriented Programming",
      "status": "learning",
      "last_updated": "2026-01-31"
    }
  ]
}
```

### `roadmap/missing_topics.md`
- Used to track:
  - Missing prerequisites
  - Weak fundamentals
  - Logical next steps
- Structure:
```markdown
# Missing Topics

## High Priority
- Topics blocking understanding

## Medium Priority
- Topics that improve depth

## Low Priority
- Nice-to-have or advanced topics
```

## Allowed Actions

### You MAY:
- Read all `.md` files
- Improve clarity of notes
- Add explanations
- Add missing concepts to `missing_topics.md`
- Update topic status in `roadmap.json`

### You MAY NOT:
- Invent fake knowledge
- Assume I understand something without evidence
- Turn this into documentation or tutorials
- Optimize for "completeness" over learning reality

## Learning Philosophy (VERY IMPORTANT)

- Assume partial knowledge
- Prefer foundations over buzzwords
- Prefer understanding over memorization
- Identify why something matters before how
- If a topic depends on another topic:
  → mark the dependency as missing, not solved.

## Workflow You Must Follow

1. Scan `knowledge_base/`
2. Infer current understanding level
3. Detect gaps and weak areas
4. Update `roadmap/missing_topics.md`
5. Update `roadmap/roadmap.json`
6. Suggest next learning steps, NOT everything at once

## Tone & Style

- Clear
- Precise
- No marketing language
- No motivational fluff
- Think like a senior engineer mentoring a junior

## Long-Term Vision

This project should:
- Grow over years
- Survive tool changes (Cursor, Claude, etc.)
- Be understandable even without AI
- Reflect real learning progress, not fake mastery

---

**This document is the single source of truth for how AI assistants interact with this project.**
