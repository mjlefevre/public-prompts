# Brutality Prompts: When & How to Use

## When to Use This

- **Before joining a new project** — Know what you're getting into
- **During technical debt discussions** — Get concrete evidence, not feelings
- **Planning a refactor** — Identify where to focus effort
- **Code review escalation** — When you suspect something is wrong but can't articulate it
- **Honest self-assessment** — Point it at your own code when you're ready to hear the truth

## Tips for Best Results

1. **Run it on a complete codebase** — Partial context leads to partial answers
2. **Be ready to hear uncomfortable things** — That's the point
3. **Follow up on specifics** — "Explain why [X] is a problem" or "Show me more examples of [Y]"
4. **Cross-reference with git blame** — Sometimes the "why" is in the history
5. **Don't shoot the messenger** — The AI is just finding what's already there

## Variations

### The Quick Hit
```
Search this codebase and give me the 3 things most likely to cause a production incident. Be specific.
```

### The Maintainability Focus
```
If a new developer joined tomorrow, what 5 things would confuse them most about this codebase? Where would they make mistakes?
```

### The Performance Angle
```
Find the 5 most likely performance bottlenecks in this code. Show me the evidence.
```

### The Security Sweep
```
What are the 5 most obvious security vulnerabilities in this codebase? Include OWASP category and specific file/line references.
```

---

## Sample Output Structure

A good response should look something like:

> **#1: The UserService God Object** (src/services/UserService.ts)
>
> This 2,400-line file handles authentication, authorization, profile management, preferences, notifications, billing integration, and somehow also email templating. It has 47 public methods and imports 23 other modules.
>
> Evidence: Lines 1-50 show imports from every corner of the application...
>
> Impact: Every feature touches this file. Any change risks breaking unrelated functionality. The test file is 4,000 lines and still only achieves 60% coverage.

---

## Fair Warning

This prompt is designed to find problems. Every codebase has problems. Even good code looks bad under a harsh enough lens. Use the output as data for prioritization, not as a reason for despair.
