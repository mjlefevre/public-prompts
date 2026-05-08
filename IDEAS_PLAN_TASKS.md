# The IDEAS → PLAN → TASKS Flow

### A simple three-file system for thinking clearly, building intentionally, and shipping consistently — especially when working with AI

---

## Why this flow exists

Most software work fails in one of two predictable ways. Either you skip thinking and start coding too early — building the wrong thing fast — or you think forever and never ship, drowning in possibilities that never become reality.

The `IDEAS → PLAN → TASKS` flow is a lightweight discipline that forces you to separate three distinct modes of thinking that usually get tangled together:

1. **Divergent thinking** — exploring what's possible
2. **Convergent thinking** — deciding what you'll actually do
3. **Executive thinking** — breaking work into atomic, completable units

Each mode lives in its own markdown file. Each file has its own job. Once you have all three, you have a durable, readable, AI-friendly artifact set that captures the entire arc from "what if?" to "shipped."

This article walks through how to use the flow, what belongs in each file, and how to get the most out of it — whether you're working solo, with a team, or with an AI coding assistant.

---

## The three files at a glance

| File | Purpose | Mindset | Output |
|------|---------|---------|--------|
| `*_IDEAS.md` | Explore the problem space | Divergent, generative, judgment-free | A messy menu of options |
| `*_PLAN.md` | Commit to an approach | Convergent, decisive, trade-off aware | A clear, defensible direction |
| `*_TASKS.md` | Break work into doable steps | Executive, concrete, sequential | A checklist you can execute |

The `*` is a feature name, project name, or initiative — for example `CHECKOUT_IDEAS.md`, `CHECKOUT_PLAN.md`, `CHECKOUT_TASKS.md`. Keeping them as a triplet under a shared prefix makes them easy to find, sort, and reference together.

---

## Stage 1 — `*_IDEAS.md`: think wide, write fast

The IDEAS file is where you go before you've decided anything. It exists to capture every approach, reference, concern, and half-formed thought before they're pruned.

The cardinal rule: **no judgment yet.** If you start evaluating ideas while you're generating them, you'll generate fewer and worse ideas. Capture first, evaluate later.

### What belongs in IDEAS.md

- **The problem statement** — what are we actually trying to solve, and for whom?
- **Goals and non-goals** — what's in scope, and explicitly what isn't
- **Open questions** — things you don't know yet but need to
- **Possible approaches** — three or more, even if some seem obviously worse
- **References and prior art** — links to similar systems, blog posts, internal docs
- **Constraints** — known technical, business, time, or team constraints
- **Risks and unknowns** — things that could derail the work
- **Wild ideas** — the option you'd pick if you had unlimited time or budget

### A minimal template

```markdown
# CHECKOUT_IDEAS

## Problem
Our checkout has a 38% abandonment rate at the payment step.

## Goals
- Reduce abandonment by at least 10 percentage points
- Don't increase fraud rate
- Ship something measurable within one quarter

## Non-goals
- Redesigning the cart page
- Adding new payment methods this quarter

## Open questions
- Is the abandonment driven by UX, trust, or actual payment failures?
- Do mobile and desktop abandon at different rates?
- What does the funnel look like for returning vs. new customers?

## Possible approaches
1. One-page checkout (collapse the 3-step flow)
2. Express checkout via wallet APIs (Apple Pay, Google Pay, Shop Pay)
3. Save card on file by default for returning users
4. Add trust signals (reviews, security badges, money-back guarantee)
5. Pre-fill address from email autocomplete services

## References
- Baymard Institute checkout research
- Stripe's "Optimized Checkout Suite" blog post
- Internal: 2024 funnel analysis from analytics team

## Constraints
- PCI compliance requirements limit some changes
- One frontend engineer available
- Must work in our existing React + Rails stack

## Risks
- Wallet APIs require new vendor relationships
- Saving cards by default may have legal implications in EU
```

### How to know you're done

You're done with IDEAS.md when you genuinely cannot think of more options worth writing down — *not* when you've found the one you like. The temptation to stop early is the biggest enemy of this stage.

### Pro tip

Use an AI assistant to expand your thinking here. A great prompt: *"Here's my IDEAS.md so far. What approaches am I missing? What questions should I be asking that I'm not? What would a skeptical senior engineer push back on?"* You'll be surprised how often it surfaces something real.

---

## Stage 2 — `*_PLAN.md`: decide, with reasons

The PLAN file is where exploration becomes commitment. You take the menu of options from IDEAS.md and choose one — or a sequenced combination — and document *why*.

This is the hardest of the three stages because it requires saying no. A good plan kills more ideas than it keeps. The discipline of writing down the trade-offs forces you to actually weigh them, not just follow the most exciting option.

### What belongs in PLAN.md

- **Context** — a one-paragraph summary of the problem, written so a new teammate could understand it
- **Decision** — the approach you've chosen, stated clearly
- **Why this, not the others** — explicit trade-offs against the alternatives in IDEAS.md
- **Architecture or approach** — diagrams, data flow, key components, system boundaries
- **Phases or milestones** — how the work breaks into shippable chunks
- **Success criteria** — how you'll know it worked
- **Rollout and rollback** — how it ships and how you back it out if needed
- **Open risks** — what's still uncertain, and how you'll learn

### A minimal template

```markdown
# CHECKOUT_PLAN

## Context
Checkout abandonment is 38% at the payment step. We've identified five candidate
approaches in CHECKOUT_IDEAS.md. After data review, the largest abandonment cohort
is mobile users who don't have their card handy — express wallet checkout addresses
this directly.

## Decision
Implement Apple Pay and Google Pay express checkout on the cart page, alongside
the existing flow. Defer one-page checkout and saved-card-by-default to a later
phase.

## Why this approach
- Highest expected impact on the identified cohort (mobile, no-card-handy)
- Lowest implementation cost — wallet SDKs handle most complexity
- Reversible — can be removed without affecting the existing flow
- Doesn't touch PCI scope (wallets are tokenized)

## Why not the others
- One-page checkout: bigger refactor, would slow the quarter, less targeted
- Save card by default: legal review needed in EU, slower to ship
- Trust signals: low-cost but data shows abandonment is logistical, not trust-based
- Email autocomplete: nice-to-have, doesn't address the core cohort

## Architecture
[diagram or description of where the wallet button lives, what events fire,
how the order is created server-side, how failures are handled]

## Phases
1. Apple Pay on iOS Safari (week 1-2)
2. Google Pay on Chrome (week 3)
3. Both wallets on desktop (week 4)
4. Measurement and iteration (week 5-6)

## Success criteria
- Mobile checkout abandonment drops by at least 10 percentage points
- Wallet checkout fraud rate stays within 0.5% of baseline
- Zero increase in p95 checkout latency

## Rollout
- Feature-flag by user bucket, ramp 1% → 10% → 50% → 100%
- Monitor abandonment and fraud daily during ramp

## Rollback
- Single feature flag toggle disables wallet buttons
- Existing flow remains untouched, so rollback is a no-op for users mid-checkout

## Open risks
- Apple Pay requires merchant verification — vendor timeline TBD
- Need legal sign-off on wallet terms (in progress)
```

### How to know you're done

You're done with PLAN.md when someone unfamiliar with the work could read it and accurately predict what you're going to build, why, and how you'll know it worked. If a smart skeptic could read it and ask "but why not X?" and X isn't addressed, you're not done.

### Pro tip

Treat PLAN.md as a contract with your future self. A month from now, when something doesn't go as expected, you'll re-read the plan to ask "did I anticipate this?" The clearer your reasoning, the faster you can adapt.

---

## Stage 3 — `*_TASKS.md`: ship in small, completable steps

The TASKS file is where the plan becomes work. It's the most boring file and the most important one — it's where momentum lives.

The principle: **every task should be small enough to complete in a single sitting and concrete enough that you don't have to think to start it.** If a task makes you hesitate, it's not ready — break it down further.

### What belongs in TASKS.md

- **A flat or grouped checklist** — `- [ ]` items that are atomic
- **Phase headers** — matching the phases from PLAN.md
- **Acceptance criteria for each task** — what "done" looks like
- **Dependencies** — what must happen before what
- **Status markers** — checked off as you go, with notes if needed

### A minimal template

```markdown
# CHECKOUT_TASKS

## Phase 1 — Apple Pay on iOS Safari

### Setup
- [ ] Register merchant ID with Apple
- [ ] Add Apple Pay capability to iOS configuration
- [ ] Verify domain with Apple
- [ ] Add ApplePayJS SDK to frontend bundle

### Frontend
- [ ] Add `<ApplePayButton />` component to cart page
- [ ] Hide button when Apple Pay is unavailable on the device
- [ ] Wire button click to `onApplePayButtonClicked` handler
- [ ] Build PaymentRequest object from cart contents
- [ ] Handle `onpaymentauthorized` callback
- [ ] Handle `oncancel` and error cases with user-visible messaging

### Backend
- [ ] Add `/api/apple-pay/validate-merchant` endpoint
- [ ] Add `/api/apple-pay/process` endpoint
- [ ] Tokenize wallet payload via Stripe
- [ ] Create order on successful tokenization
- [ ] Handle and log all error paths

### Testing
- [ ] Unit tests for token validation
- [ ] Integration test for full happy path
- [ ] Manual test on real iOS device (sandbox)
- [ ] Manual test of cancellation flow
- [ ] Manual test of declined-card flow

### Rollout
- [ ] Feature flag created and defaulted off
- [ ] Analytics events instrumented
- [ ] Dashboard built for abandonment + fraud
- [ ] Enable for internal users only
- [ ] Ramp to 1% of mobile traffic
```

### Anti-patterns to avoid

- **Tasks that hide work.** "Implement checkout" is not a task. It's the whole project.
- **Tasks without acceptance criteria.** "Add a button" — what does done look like?
- **Tasks that depend on undocumented decisions.** If the task requires choosing between two approaches, that decision belongs in PLAN.md, not TASKS.md.
- **Stale lists.** If you finish a task, check it off the same day. Stale lists rot.

### Pro tip

Keep tasks small enough that completing one feels good. Momentum is the real product of a task list. Big undifferentiated tasks kill momentum; small completable ones build it.

---

## Using this flow with AI

The flow is good on its own, but it gets remarkable when you pair it with an AI coding assistant. The reason is simple: AI tools work better when they have context, and these three files *are* the context — written, durable, and structured.

A few patterns that work well:

**Use IDEAS.md as a research partner.** Drop your initial draft into the chat and ask the AI to challenge assumptions, suggest missing approaches, or identify constraints you haven't named. Expand the file with what comes back.

**Use PLAN.md as the AI's source of truth.** When you ask the AI to help build something, point it at the plan first. "Read CHECKOUT_PLAN.md and tell me how you'd structure the frontend component." The plan grounds its suggestions in your actual decisions.

**Use TASKS.md as the AI's worklist.** Many AI coding tools can pick up tasks from a checklist, complete them, and check them off. Keeping tasks small and well-specified means the AI can actually finish them — and you can review them in small reviewable units.

**Update the files as you go.** When you learn something mid-build, write it back into the relevant file. The flow only stays useful if it stays current.

---

## Common questions

**Do I really need all three files for small work?**
No. For a one-hour task, a handful of bullet points is plenty. The flow earns its weight when work spans days or weeks, multiple people, or AI assistance.

**Can these files live in the repo?**
Yes — and they should, when the work is technical. Keep them in a `/docs`, `/plans`, or `/specs` directory next to the code. They become part of the project's history and reasoning.

**What if my plan changes?**
Update PLAN.md and note what changed and why. The point of the flow isn't to be rigid — it's to be intentional. A changed plan with documented reasoning is fine; an unchanged plan that no longer matches reality is not.

**How is this different from a PRD or RFC?**
A PRD is roughly the PLAN file from a product lens. An RFC is roughly the PLAN file from a technical lens. The IDEAS and TASKS files are the bookends that most PRD and RFC processes leave implicit. Making them explicit is the contribution of this flow.

**What about meeting notes, retros, postmortems?**
Different artifacts for different purposes. This flow covers the path from problem to shipped work. It doesn't replace operational or learning artifacts — it complements them.

---

## A summary you can pin to your wall

> **IDEAS** is where you think.
> **PLAN** is where you decide.
> **TASKS** is where you do.
>
> Don't decide while you're thinking.
> Don't think while you're doing.
> Don't do without deciding.

Three files. Three modes. One clear path from problem to shipped.
