# Core Principles for AI-Assisted Work

Universal principles for working with AI on sustained tasks — coding, strategy docs, pitches, analysis, or any work that spans multiple sessions.

---

## The Maturity Model

Where you are today determines what to focus on next.

### Level 1: Ad Hoc

**What it looks like:** Prompting the AI, accepting output, hoping it works. No consistent process. Quality varies wildly between sessions. Context gets lost between sessions — every restart feels like starting over.

**How to level up:**
- Establish a session management practice (see below)
- Create a project CLAUDE.md or context file with patterns to follow
- Start committing/saving work in small checkpoints instead of big batches

### Level 2: Planned

**What it looks like:** Guardrails exist. Session notes capture state. Quality gates define "done." You have a repeatable process for starting and ending sessions.

**How to level up:**
- Build verification into your workflow (test suites, review checklists, CI checks)
- Create reusable patterns from solved problems (see [patterns/](patterns/))
- Break work into phases with clear dependencies

### Level 3: Systematic

**What it looks like:** Test suites validate changes before they ship. Solved patterns are captured and reused. Work is broken into phased plans with dependencies mapped. The AI follows established conventions consistently because context files are well-structured.

**How to level up:**
- Have the AI proactively suggest improvements (tests, refactors, pattern violations)
- Automate session handoffs — AI generates its own continuation notes
- Build evaluation criteria for AI output quality

### Level 4: Optimized

**What it looks like:** AI proactively catches pattern violations, suggests test coverage, and manages session continuity. You focus on decisions and direction. The AI handles routine execution within established guardrails. Your context files and patterns are a living system that improves with each session.

**The goal isn't to reach Level 4 on day one.** It's to know where you are and what the next step looks like.

---

## Principles

### 1. Documentation First

Before doing the work, document the plan:
- **What** you're trying to accomplish
- **Why** this approach (not an alternative)
- **Patterns to follow** — link to similar past work
- **How you'll know it's done**

Markdown files > trying to explain everything in chat. Written plans survive session restarts. Chat history doesn't.

### 2. Plan Big Work in Phases

For multi-session or multi-step work, create a punch list.

Structure by dependencies:
1. **Blockers first** — fix what prevents accurate progress
2. **Core work second** — the actual deliverable
3. **Polish third** — refinement, formatting, edge cases
4. **Verification last** — confirm everything holds together

Update the document as you work:
- Mark items complete with dates
- Add findings and decisions inline
- Create follow-up items for deferred work

A punch list keeps you focused and gives visibility into progress.

### 3. Checkpoint Frequently

Save after every meaningful unit of progress, not just when "done."

- Get one thing working -> save/commit
- Complete one section -> save/commit
- Fix one issue -> save/commit
- Do NOT wait until the entire deliverable is complete

**Why:** You always have a last known good state to return to. If something goes wrong, you revert one small change instead of losing hours of work.

### 4. Quality > Speed

Shipping fast is good. Shipping sloppy work is not.

Before publishing, sending, or merging, ask:
- **Is this creating more work than it saves?**
- **Will this be easy to maintain or build on?**
- **Did I follow established patterns or force my own?**

If the answer to any is "no" — refactor before shipping.

### 5. Know When to Ask

You're not expected to know everything. Pause before:
- Creating new patterns when established ones exist
- Deviating from conventions
- Making decisions that affect others
- Shipping something you're not confident about

**It's better to ask than to create work for others cleaning up after you.**

### 6. The 6-Month Test

Ask: "If I had to modify this in 6 months with no memory of creating it, would I be annoyed?"

If yes — simplify, document intent, or restructure before shipping.

This applies to code, docs, processes, and project organization equally.

### 7. Clean Up Before Milestones

Before major deliverables (releases, submissions, publications), do a housekeeping pass.

**Remove:**
- Stale documentation that no longer reflects reality
- Artifacts from past debugging or exploration
- Abandoned experiments and dead drafts

**Keep:**
- The source of truth (current configs, active docs)
- Session notes and decision logs
- Active work in progress

The best time to clean up is before shipping, not after.

### 8. Keep It Lean

- Use straightforward approaches over clever ones
- Don't over-engineer for hypothetical future needs
- Remove what's unused — if removing it breaks nothing, it shouldn't be there
- Ask: "Do I really need this, or can I do it simply?"

### 9. Discover Before Building

Before adding something new, search for existing patterns.

This applies to code, docs, processes, and templates:

1. **Ask "how is this currently done?"**
2. **Search for existing patterns** — past work, templates, conventions
3. **Look at similar past work** — what's been done before?
4. **Check before creating** — don't duplicate what exists

**Red flags that you're about to duplicate:**
- Building a new template for something that already has one
- "I'll create a helper to..."
- Adding a new process when an existing one covers the case

---

## Session Management

Context rot is real. AI assistants lose coherence over long sessions. Managing sessions is as important as managing the work itself.

### When to Restart

**After 2-3 major tasks, or when you notice:**
- AI suggesting approaches different from what you established
- Having to re-explain things covered earlier
- Output quality declining
- More errors or back-and-forth

### Before Restarting: Capture State

Create a session notes file with:

1. **Accomplished** — what got done
2. **Current state** — what's working, what's in progress
3. **What's next** — immediate steps, known issues
4. **Context for next session** — patterns established, decisions made, key info AI needs

### Where to Save

**Team projects:**
```
.claude/sessions/YYYY-MM-DD-feature-name.md
# or
docs/sessions/YYYY-MM-DD-your-name.md
```

**Solo projects:**
```
.claude/sessions/YYYY-MM-DD.md
# or
dev-log.md  # Append to running log
```

### Starting Fresh

1. **Load context** — point AI to session notes and project context files
2. **Verify understanding** — confirm AI knows where you left off
3. **Break down next task** — smaller tasks = better output

### Session Notes Template

```markdown
# [Date] - [What You Worked On]

## Done
- [Task 1]
- [Task 2]

## Current State
- [What's working]
- [What's in progress]

## Next
1. [Immediate task]
2. [Following task]

## Patterns / Decisions
- [Key decision and why]
- [Pattern established for future reference]

## Resume Prompt
[What to tell the AI to load context for the next session]
```

---

## Working with AI

### Your Role

The AI is your collaborator, but you're responsible for:
- **Directing the approach** — "Follow the pattern in X"
- **Verifying quality** — check output against standards
- **Making judgment calls** — "Is this good enough or should I refine?"

The AI helps you execute. You ensure the output is responsible.

### Task Breakdown

**The smaller the task, the better the output.**

Break work into focused chunks:
- **Bad:** "Write the quarterly strategy update"
- **Good:** "Draft the Top 3 section for the exec update, following last week's format"

Each task should be completable in one focused session.

### Context Files Over Chat

Structure what the AI needs to know in files, not conversation:
- **Project context** — what the AI needs to know about this work
- **Patterns to follow** — link to similar past work
- **Decisions made** — why you're taking this approach

Files persist across sessions. Chat history doesn't.

---

*These principles apply to any sustained AI-assisted work. For coding-specific standards, see [coding/](coding/).*
