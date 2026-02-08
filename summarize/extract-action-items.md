# Extract Action Items

Meetings, documents, and discussions generate commitments that get lost in the noise. This prompt ruthlessly extracts every task, to-do, and follow-up buried in content. Critical for turning long meeting transcripts into accountable work, or ensuring nothing falls through the cracks after reading a detailed spec or plan.

---

## The Prompt

Read this content and extract every actionable item, task, commitment, or follow-up.

For each action item, capture:
- [ ] **Task**: What needs to be done (specific and concrete)
- **Owner**: Who is responsible (if mentioned or implied; otherwise mark as "Unassigned")
- **Deadline**: When it's due (if mentioned; otherwise mark as "No deadline specified")
- **Context**: One sentence on why this matters or where it came from
- **Dependencies**: What needs to happen first, if anything

Output format:
```
### Action Items

- [ ] [Task description]
  - Owner: [Name/Unassigned]
  - Deadline: [Date/No deadline specified]
  - Context: [Brief context]
  - Dependencies: [None/List]
```

Also flag:
- Any commitments that seem unrealistic or conflicting
- Tasks mentioned but with no clear owner
- Deadlines that have already passed
