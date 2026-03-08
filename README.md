# PM AI Playbook

A practical system for product managers working with AI assistants — whether you're coding, writing strategy docs, or building products.

## The Problem

PMs using AI to build face a unique challenge: shipping quality work while respecting team standards and maintaining continuity across sessions. AI-assisted work can be incredibly productive, but without a system, it results in:

- Lost context between sessions (re-explaining the same things)
- Inconsistent quality (great output one session, sloppy the next)
- PRs that fail CI/CD (for coding work)
- Duplicated effort (solving the same problems repeatedly)

## The Solution

A layered playbook that scales from "I just started using AI" to "AI is my daily operating system."

## What's Inside

### Core (All AI-Assisted Work)

**[core-principles.md](core-principles.md)** — Universal principles and maturity model
- The maturity model: ad hoc → planned → systematic → optimized
- Documentation-first, checkpointing, planning in phases
- Session management (avoiding context rot)
- The 6-month test, lean thinking, discover before building

### Coding

**[coding/quality-gates.md](coding/quality-gates.md)** — Pre-commit checklist and PM-who-codes philosophy
- Pattern matching, CI/CD readiness, code review standards
- Role clarity: PM who codes vs. software engineer
- Team vs. solo codebase expectations

**[coding/test-first.md](coding/test-first.md)** — AI-generated safety nets
- Generate test suites from existing behavior before modifying code
- The highest-leverage use of AI in coding

**[coding/solo-projects.md](coding/solo-projects.md)** — Standards for solo projects
- Keep it simple, lean, and maintainable
- When to test, when to document, pre-ship checklist

**[coding/prompt-engineering.md](coding/prompt-engineering.md)** — Production prompt optimization
- The 6-step optimization framework
- Battle-tested production prompt template
- The 3 fatal mistakes and dependent operation patterns

### Patterns

**[patterns/](patterns/)** — Capture and reuse solved problems
- How to build a pattern library that compounds over time
- Pattern format and integration with AI context files

### Integration

**[skill.md](skill.md)** — Skill definition for AI operating systems
- Auto-trigger configuration for Claude Code / Bette OS
- What to load and when

## The Maturity Model

| Level | What It Looks Like | Focus |
|-------|-------------------|-------|
| **Ad Hoc** | Prompting AI, accepting output, hoping it works | Establish session management and context files |
| **Planned** | Guardrails exist, session notes capture state, quality gates define "done" | Build verification into workflow |
| **Systematic** | Test suites, captured patterns, phased plans with dependencies | AI proactively suggests improvements |
| **Optimized** | AI manages routine execution within guardrails, you focus on decisions | Living system that improves each session |

## Who This Is For

- **PMs learning to code** with AI assistance
- **PMs writing strategy** with AI as thought partner
- **Product builders** shipping with AI across coding and non-coding work
- **Founders** doing everything — CEO, product, engineering — with AI as force multiplier
- **Anyone working with AI** who wants a system, not just prompts

## How to Use

### Option 1: Integrate with Claude Code

Reference in your CLAUDE.md:

```markdown
## Working Standards

At the start of any session, load the PM AI Playbook:
- Read core-principles.md for universal working principles

For coding sessions, also load:
- Read coding/quality-gates.md for pre-commit standards
- Read coding/test-first.md for the test-first pattern
```

### Option 2: Use as Reference

- Before starting any sustained work: Read core-principles.md
- Before committing code: Check coding/quality-gates.md
- Before modifying existing code: Review coding/test-first.md
- After solving a hard problem: Capture it in patterns/

### Option 3: Customize for Your Setup

Fork this repo and adapt:
- Add your own patterns to patterns/
- Adjust quality gates for your team's tools
- Extend the maturity model for your context

## Philosophy

This isn't about being a perfect engineer or a perfect writer. It's about being a systematic one.

The goal: Ship quality work that compounds — where each session makes the next one better.

## Contributing

Found this helpful? Have improvements? PRs welcome.

## License

CC BY-NC-SA 4.0 — Free to use for personal and internal business use with attribution.

---

Built for PMs who want to work with AI systematically. Ship with quality and intention.
