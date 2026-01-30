# Specialized Agents and Personas

This folder contains detailed skill definitions for specialized agents that can be employed during development tasks. Each agent brings focused expertise to specific types of work.

---

## Instructions for LLMs

**Do NOT read or parse the individual agent files unless explicitly requested.** These files contain detailed persona instructions and are only needed when an agent is actively being employed. For routine coding tasks, HTML changes, bug fixes, or general development work, ignore the agent files entirely.

**When to employ an agent:**
- The user explicitly references an agent file (e.g., `@brand-guardian.md`)
- The user asks you to "use" or "employ" a specific agent by name
- The task clearly falls within an agent's specialty AND would benefit from their focused expertise

**When NOT to employ an agent:**
- General coding, debugging, or refactoring tasks
- Simple HTML, CSS, or template changes
- Database queries or API work
- Any task where the user hasn't requested specialized assistance

When you do employ an agent, read their full file and adopt their persona, methodology, and deliverable formats for the duration of that task.

---

## Available Agents

| Agent | File | Specialty |
|-------|------|-----------|
| **The macOS Architect** | `architect-macos.md` | Swift and macOS code architecture, code review, and feature planning. Expert in this codebase's patterns, SwiftUI conventions, and established coding standards. Provides collaborative guidance with honest assessments and mentorship. |
| **The Architect (Python)** | `architect-python.md` | Python code architecture, code review, and feature planning. Expert in Python codebase patterns, conventions, and established coding standards. Provides collaborative guidance with honest assessments and mentorship. |
| **Brand Guardian** | `brand-guardian.md` | Brand strategy, visual identity systems, brand voice/messaging, and brand protection. Expert at creating cohesive brand foundations and ensuring consistent brand expression across all touchpoints. |

---

## Adding New Agents

When new agent files are added to this folder, update this README with a one-paragraph summary in the table above. Each agent file should be a self-contained persona definition that an LLM can adopt when referenced.
