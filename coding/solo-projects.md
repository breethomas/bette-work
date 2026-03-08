# Solo Project Standards

Standards for coding projects where you're the only engineer. The [core principles](../core-principles.md) (session management, checkpointing, planning) apply here too.

---

## The Standard

Solo code should be:
- **Maintainable** — you or someone else can modify it 6 months later
- **Lean** — simple, focused, no bloat
- **Quality** — not slop code, even when moving fast

## Testing: Enough to Be Confident

You don't need 100% coverage. You need enough confidence to ship.

**Minimum viable testing:**
- Happy path works — core functionality does what it's supposed to
- Common edge cases handled — empty states, errors, boundary conditions
- Manual testing done — you've actually used it in a realistic scenario

**Write automated tests when:**
- Logic is complex or has edge cases
- You'll forget how it works
- It's critical functionality
- It will change frequently

**Skip automated tests when:**
- It's purely presentational
- It's a throwaway prototype
- Manual testing is sufficient

Also see [test-first.md](test-first.md) — before modifying existing code, generate a test suite from current behavior first.

## Document Intent, Not Implementation

**Document:**
- WHY you made a decision — not what the code does
- Non-obvious trade-offs — "Using X instead of Y because Z"
- Future considerations — "TODO: Will need to handle Z when feature X ships"

**Don't document:**
- What the code obviously does
- Implementation details that are self-evident

## Red Flags

**Stop and refactor if:**
- You're copy-pasting the same code in multiple places
- You can't explain what a function does in one sentence
- Utility files are growing out of control
- You're adding dependencies for trivial functionality
- You're shipping AI-generated code you don't understand

## Pre-Ship Checklist

- [ ] **Code is maintainable** — future you will understand it
- [ ] **No obvious bloat** — removed unused code, unnecessary dependencies
- [ ] **Core functionality tested** — confident it works
- [ ] **Basic documentation exists** — README explains what/why/how to run
- [ ] **You'd want to use this** — would you show this to someone?

---

*The goal: Build things you're proud of, not just things that work.*
