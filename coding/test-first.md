# Test-First: AI-Generated Safety Nets

Before modifying existing code, have the AI generate a test suite from current behavior. Tests become your safety net before you change anything.

---

## The Principle

**Never modify code without a way to verify you didn't break it.**

When working with AI, it's tempting to jump straight to changes. The code is right there, the AI can read it, and you can see what needs to change. But without tests capturing current behavior, you're flying blind — you won't know if your change broke something unrelated until it's too late.

## The Pattern

### Step 1: Generate Tests From Current Behavior

Before changing anything, ask the AI to:

```
Read [file/module] and generate a test suite that captures its current behavior.
Cover:
- Happy path (what it does when everything works)
- Edge cases (empty inputs, missing data, boundary values)
- Error handling (what happens when things fail)
- Side effects (what it changes, calls, or triggers)
```

### Step 2: Run the Tests — They Must Pass

The generated tests should pass against the existing code. If they don't, fix the tests first. You need a green baseline before you change anything.

### Step 3: Make Your Changes

Now modify the code. Run the test suite after each change.

- **Tests still pass?** Your change is safe.
- **Tests fail?** You broke existing behavior. Decide: is that intentional (update the test) or a bug (fix your change)?

### Step 4: Add Tests for New Behavior

After your changes are stable, add tests for the new behavior you introduced.

## When to Use This

**Always use test-first when:**
- Modifying code you didn't write
- Changing code you wrote but don't fully remember
- Refactoring — behavior should be identical before and after
- Touching anything with complex business logic

**OK to skip when:**
- Writing brand new code (nothing to capture yet — write tests alongside)
- Trivial changes (fixing a typo, updating a string)
- Throwaway prototypes

## Why AI Makes This Practical

Before AI, generating a comprehensive test suite for unfamiliar code was a multi-day effort. Now you can have the AI read the code, understand its behavior, and produce tests in minutes. The barrier to doing this responsibly is gone.

This is one of the highest-leverage uses of AI in coding: **not writing new code, but making existing code safe to change.**

---

*Untested code isn't broken code you haven't found yet. It's a change you can't make safely.*
