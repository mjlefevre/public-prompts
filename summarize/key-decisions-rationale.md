# Key Decisions & Rationale

Decisions get made and then forgotten — along with why they were made. This prompt creates a decision log from any content, capturing not just what was decided but the reasoning and alternatives considered. Invaluable for architecture decision records (ADRs), post-mortems, or understanding why a codebase or system looks the way it does.

---

## The Prompt

Identify all decisions made, proposed, or implied in this content. For each decision, document:

### Decision Log Format

**Decision #[N]: [Short title]**
- **What was decided**: Clear statement of the choice made
- **Why**: The reasoning, constraints, or goals that drove this decision
- **Alternatives considered**: What other options were discussed or rejected?
- **Trade-offs accepted**: What downsides or risks were knowingly accepted?
- **Implications**: What does this decision affect going forward?
- **Reversibility**: Is this easy to change later, or are we locked in?
- **Status**: Decided / Proposed / Under discussion / Revisit later

Also note:
- Decisions that seem to contradict each other
- Decisions made without clear rationale
- Important decisions that should have been made but weren't
