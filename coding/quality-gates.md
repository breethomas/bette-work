# Quality Gates - Pre-Commit Checklist

These checks are non-negotiable. Don't commit code until ALL pass.

Also review [core principles](../core-principles.md) — checkpointing, session management, and documentation-first apply to all work.

---

## Your Role as PM Who Codes

**You're a product manager who codes, not a software engineer.**

- **Goal:** Ship features quickly while respecting engineering quality
- **Strength:** Product thinking, prototyping, getting things done
- **Limitation:** Not a professional software engineer
- **Responsibility:** Don't create more work for the team than the feature is worth

## Universal Pre-Commit Checklist

### 1. Pattern Matching
- [ ] **Found similar code** — located existing components/patterns that match what you're building
- [ ] **Studied the patterns** — understand how they work and why
- [ ] **Matched exactly** — your code follows the same spacing, naming, structure

**Consistency > personal preference.** When working in existing codebases:
- Match patterns exactly — spacing, naming, structure, everything
- Don't innovate on architecture — use what's already there
- Ask before deviating from established conventions

### 2. Code Quality
- [ ] **Formatters run** — code is properly formatted
- [ ] **Linters pass** — no linting errors
- [ ] **Type checking passes** — no TypeScript/type errors (if applicable)

### 3. Testing
- [ ] **Manual testing done** — tested in actual environment
- [ ] **Feature works as expected** — verified acceptance criteria
- [ ] **Edge cases tested** — tried to break it, couldn't
- [ ] **Tests written** — automated tests per project conventions
- [ ] **Tests pass** — all test suites pass locally

### 4. CI/CD Readiness
- [ ] **All local checks pass** — everything CI will run has been run locally first
- [ ] **No failing tests** — test suite is 100% passing
- [ ] **No linting errors** — clean output
- [ ] **No type errors** — clean type checking (if applicable)

### 5. Code Review
- [ ] **Only relevant files staged** — no accidental changes
- [ ] **Working directory clean** — no uncommitted experimental code
- [ ] **Changes are focused** — commit does one thing, does it well
- [ ] **Would you want to review this?** — be honest

## The CI/CD Blocker

**STOP if any of these are true:**
- "I haven't run the checks yet"
- "I'm not sure if tests pass"
- "I'll fix the linting errors after pushing"
- "CI will tell me if something's wrong"

**Instead:**
1. Run all checks locally
2. Fix all issues
3. Verify everything passes
4. THEN commit and push

## Prompt Engineering Checklist

**When modifying AI prompts (system prompts, agent prompts, etc.):**

Review [prompt-engineering.md](prompt-engineering.md) FIRST. This is different from regular coding — prompts affect user-facing AI behavior, failure modes are subtle, and side effects cascade.

### Before Making Changes
- [ ] **Review the 6-step framework** in prompt-engineering.md
- [ ] **Identify the failure mode clearly** — what specific behavior are you fixing?
- [ ] **Search for related edge cases** — what OTHER operations could have the same problem?
- [ ] **Check for dependent operations** — do any mutations/actions require outputs from other actions?

### When Making Changes
- [ ] **Use hard constraints (NEVER) over soft guidance** — more reliable than "be careful about X"
- [ ] **Provide specific BAD/GOOD examples** — concrete examples beat abstract rules
- [ ] **Add constraints in multiple locations** — put critical rules in both hard_constraints AND relevant sections

### After Making Changes
- [ ] **Define success criteria** — how will you know if this fix worked?
- [ ] **Test the failure mode** — reproduce the original issue and verify it's fixed
- [ ] **Test related scenarios** — check that fixing one thing didn't break another

## Working in Team vs. Solo Codebases

### Team Projects
- Follow their workflow religiously
- Use their tools and conventions
- Run their quality checks
- Respect their architectural decisions
- Don't create cleanup work for senior engineers

### Solo Projects
- See [solo-projects.md](solo-projects.md) for standards
- Quality still matters — future you is your teammate

## Success Metrics

You're doing this right when:
- PRs pass CI on first push
- Code reviews focus on product decisions, not code quality issues
- Senior engineers aren't cleaning up after you
- Your code is maintainable 6 months later

---

*This is not about being a perfect engineer. It's about being a responsible one.*
