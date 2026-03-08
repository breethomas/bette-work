# Patterns Library

Capture solved patterns so your AI assistant can reuse them across sessions.

---

## The Idea

Every time you solve a non-trivial problem with AI, you have two choices:
1. Solve it and move on (it dies with the session)
2. Capture the pattern so it's available next time

Option 2 compounds. Over time, your AI assistant gets better because it has access to patterns that already work in your codebase, your style, and your context.

## What to Capture

**Capture a pattern when:**
- You solved something that took multiple iterations to get right
- The solution required project-specific knowledge the AI wouldn't have by default
- You'll likely need to do something similar again
- The pattern deviates from what the AI would produce on its own

**Don't capture:**
- Standard, well-known approaches (the AI already knows these)
- One-off solutions you'll never need again
- Patterns that are obvious from reading the codebase

## Pattern Format

Keep it simple. Each pattern is a markdown file:

```markdown
# [Pattern Name]

## When to Use
[One sentence: the situation this pattern solves]

## The Pattern
[The actual approach — code, structure, or process]

## Why This Way
[Why this approach, not the obvious alternative]

## Example
[A concrete example from your project]
```

## How It Works With AI

Reference patterns in your project CLAUDE.md or context files:

```markdown
## Patterns
When working on [type of task], follow the patterns in patterns/:
- [pattern-name.md] for [situation]
```

The AI reads the pattern file and applies it consistently, without you re-explaining every session.

## Getting Started

Don't try to document everything at once. Start with the next pattern you solve that takes more than one attempt. Capture it, move on. The library grows organically.

---

*One pattern captured is worth ten sessions re-solving the same problem.*
