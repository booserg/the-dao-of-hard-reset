# The Dao of Hard Reset

> A pragmatic approach to iterative software development that embraces the power of "reset and retry" for better outcomes.

## What is Vibe Coding?

Vibe coding is a development methodology that combines structured iteration with the flexibility to reset and improve when needed. It acknowledges that the first attempt isn't always the best and provides a framework for continuous improvement through deliberate iteration cycles.

## Core Principles

- **Reset with Purpose**: When stuck or unsatisfied, reset to a clean state and try again with new insights
- **Iterate with Intention**: Each iteration should build on learnings from previous attempts
- **Ship with Confidence**: Only commit when the implementation meets your quality standards

## Quick Start

1. **Set up your project structure**:
   ```
   your-project/
   ├── development/           # Store drafts and final prompts here
   ├── playground/           # Isolated experimentation
   ├── roadmap.md            # Track planned features
   └── [your source code]
   ```

2. **Follow the new 4-phase workflow**:
   - **Roadmap**: Add feature to roadmap with short description
   - **Draft**: Create freeform feature description (user story style)
   - **Refine**: Work with Claude to clarify and improve the draft
   - **Prompt**: Convert refined draft to structured prompt using template
   - **Implement**: Use final prompt for implementation

## Repository Contents

### 📋 [approach.md](approach.md)
The complete methodology guide covering:
- Prerequisites and setup
- 7-phase workflow (Roadmap → Draft → Refine → Prompt → Implementation → Quality Gate → Decision)
- Playground development strategy
- Success metrics

### 🛠️ [resources/prompt-template.md](resources/prompt-template.md)
Comprehensive template for creating feature development prompts with sections for:
- Project context and requirements
- Technical specifications
- Quality criteria and acceptance tests
- Implementation guidance

### 📖 [resources/template-usage-guide.md](resources/template-usage-guide.md)
Practical guide for the new workflow:
- Draft creation tips
- Claude refinement process
- Template conversion guidance
- Common iteration patterns

## The Workflow

```mermaid
graph TD
    A[Update Roadmap] --> B[Create Draft]
    B --> C[Refine with Claude]
    C --> D{Draft Complete?}
    D -->|No| C
    D -->|Yes| E[Create Final Prompt]
    E --> F{Prompt Ready?}
    F -->|No| E
    F -->|Yes| G[Implement Feature]
    G --> H[Test & Evaluate]
    H --> I{Quality Gate}
    I -->|Satisfactory| J[Commit Changes]
    I -->|Needs Work| K[Hard Reset]
    K --> L{Issue Type}
    L -->|Requirements| C
    L -->|Prompt| E
    J --> M[Next Feature]
```

## When to Use This Approach

**✅ Great for:**
- Solo development projects
- Rapid prototyping
- Learning new technologies
- Complex features with unclear requirements
- AI-assisted development

**⚠️ Consider alternatives for:**
- Large team collaborations
- Critical production hotfixes
- Simple, well-defined tasks
- Strict regulatory environments

## Philosophy

The Dao of Hard Reset recognizes that software development is inherently iterative and that perfection often comes through refinement rather than getting it right the first time. By embracing controlled failure and systematic improvement, developers can achieve higher quality outcomes while maintaining development velocity.

## Getting Started

1. Read the [approach guide](approach.md) to understand the methodology
2. Review the [prompt template](resources/prompt-template.md) structure
3. Check the [usage guide](resources/template-usage-guide.md) for practical tips
4. Start with a simple feature to practice the workflow

## Contributing

This methodology is a living document. Feel free to:
- Adapt the templates for your specific needs
- Share improvements and variations
- Document lessons learned from your iterations

## License

This project is open source. Use, modify, and share freely.

---

*"Reset with purpose, iterate with intention, ship with confidence."*