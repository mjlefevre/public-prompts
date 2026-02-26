# Brutality Prompt: Roast This Codebase

Use this prompt with agentic coding tools (Claude Code, Cursor, Windsurf, Cline, etc.) to get an unflinching, honest critique of a codebase. No sugarcoating.

---

## The Prompt

I want you to be brutally honest with me. Search through this project/repository and tell me the 20 worst things about this code. I don't want encouragement — I want the hard truth.

Look for:

**Architectural Sins**
- Where is the design fundamentally broken or fighting against itself?
- What patterns were clearly chosen without understanding the tradeoffs?
- Where did someone cargo-cult a "best practice" that doesn't fit this context?

**Maintenance Nightmares**
- What code is so tangled that any change risks breaking something unrelated?
- Where are there hidden dependencies or implicit coupling that will bite the next developer?
- What "temporary" hacks have clearly become permanent fixtures?

**Bug Factories**
- Where is the code begging for bugs? Race conditions, null dereferences, off-by-ones waiting to happen?
- What error handling is missing, broken, or actively misleading?
- Where are there obvious edge cases being ignored?

**Complexity Hotspots**
- What files/functions are so complicated that no one wants to touch them?
- Where has abstraction gone wrong — either too much (over-engineering) or too little (copy-paste everywhere)?
- What code requires "tribal knowledge" to understand or modify safely?

**Technical Debt Traps**
- Where are developers likely spending 80% of their time fighting the codebase?
- What would you have to rewrite to add any significant new feature?
- What decisions are going to hurt more the longer they're left in place?

**Testing & Reliability**
- What critical paths have no tests?
- What tests exist but test nothing meaningful (false confidence)?
- Where would a production incident be hardest to diagnose?

Be specific. Name files, functions, and line numbers. Quote the offending code. Don't tell me "consider improving X" — tell me "X is broken because Y and here's the evidence."

Prioritize by impact: what's actually causing pain vs. what's just ugly but harmless.

After the top 20, give me:
1. The single change that would have the biggest positive impact
2. The one thing that's actually done well (if anything)
3. Your honest assessment: is this codebase worth saving or should parts be rewritten?
