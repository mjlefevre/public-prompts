# Timeline / Chronology Extraction

Dates, deadlines, and milestones get scattered throughout documents. This prompt pulls them all into a single chronological view, making it easy to see the sequence of events or build a project timeline. Essential for project planning, historical analysis, or understanding how events unfolded.

---

## The Prompt

Extract all dates, deadlines, milestones, and time-referenced events from this content. Present them as a chronological timeline.

### Output Format

**Timeline Overview**
- Earliest date mentioned: [date]
- Latest date mentioned: [date]
- Time span: [duration]

**Chronological Timeline**

| Date | Event/Milestone | Type | Notes |
|------|-----------------|------|-------|
| [Date] | [What happened/happens] | Past/Deadline/Milestone/Target | [Context] |

**Upcoming Deadlines** (sorted by urgency)
1. [Date]: [What's due] — [X days from now]
2. ...

**Potential Conflicts**
- Deadlines that seem too close together
- Dependencies that might not allow enough time
- Dates that have already passed but are referenced as future

**Missing Dates**
- Events or milestones mentioned without specific dates
- Vague timing ("soon", "Q3", "next sprint") that should be clarified

Also note if dates are:
- Firm commitments vs. estimates
- External deadlines vs. internal targets
- Dependencies on other events
