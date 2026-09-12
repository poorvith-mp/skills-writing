---
name: feedback-writing
last_reviewed: 2026-09-06
group: Workplace
description: >-
  Write constructive feedback using Situation-Behavior-Impact for performance, peer and 360
  reviews. Use when drafting constructive performance reviews, peer praise, or coaching.
---

# feedback-writing

## Core Philosophy
Constructive feedback fails when it is delivered as subjective character criticism or wrapped in cowardly "feedback sandwiches" (praise-criticism-praise) that confuse the recipient. High-impact professional feedback is grounded in objective behavioral observation, clear business impact, and psychological safety. Utilizing the Center for Creative Leadership’s **Situation-Behavior-Impact (SBI)** model, feedback separates observable actions from assumed motives and establishes clear forward-looking behavioral commitments.

---

## 4-Step Constructive Feedback Framework (The SBI Model)

### Step 1: Situation (Anchor in Exact Time & Place)
1. **Specific Temporal Anchoring**:
   - Establish the precise context so the recipient's memory is grounded:
     - *Bad*: "You're often aggressive in team meetings."
     - *Good (SBI Situation)*: "Yesterday during the 2:00 PM architecture review for the billing migration..."

### Step 2: Behavior (Observable, Video-Camera Facts)
1. **The "Video-Camera" Test**:
   - Describe only what a video camera could record. Eliminate adjectives, personality traits, and mind-reading assumptions:
     - *Bad*: "You were rude and dismissive to the junior engineer."
     - *Good (SBI Behavior)*: "When Sarah was presenting her database schema proposal, you interrupted her three times and said 'this approach is completely stupid' before she finished explaining."

### Step 3: Impact (The Measurable Outcome on Team & Business)
1. **Explaining the Repercussions**:
   - Articulate the emotional, team, or operational consequences:
     - *SBI Impact*: "Sarah stopped sharing her ideas for the rest of the meeting, the junior team members became visibly hesitant to ask technical questions, and we missed exploring an edge case that delayed our sprint sign-off."

### Step 4: Alternative Behavior & Collaborative Commitment (SBI-A)
1. **Forward-Looking Alignment**:
   - Agree on concrete future behavior rather than litigating the past:
     - *"In future architecture reviews, I need you to let the presenter finish their slide deck before critiquing, and phrase disagreements around technical trade-offs rather than labels. How does that sound to you?"*

---

## Deliverable Format: Performance Feedback Record (`FEEDBACK-MEMO.md`)

```markdown
# Constructive Feedback Memo: [Recipient Name]
*Date: [YYYY-MM-DD] | Manager / Reviewer: [Name, Title]*

## 1. Feedback Type & Context
- **Type**: [Developmental / Performance Coaching / Peer 360 Review]
- **Setting**: 1-on-1 private sync

## 2. SBI Feedback Framework
- **Situation**:
  During yesterday's sprint planning session at 10:00 AM...
- **Behavior (Observable Facts)**:
  You committed to delivering the authentication refactor by Wednesday, but did not update the Jira ticket or notify the team until Friday afternoon when CI builds failed.
- **Impact (Business & Team Consequence)**:
  Frontend engineers were blocked from integrating the new login flow for two days, and we had to reschedule the client demo from Thursday to next week.

## 3. Required Future Behavior (The Commitment)
- Update ticket status within 2 hours if an unexpected blocker delays a committed deadline.
- Post an async update in `#eng-blockers` as soon as an issue is identified so teammates can swarm.

## 4. Recipient Response & Agreed Next Action
- [Notes on recipient's perspective and confirmed commitment].
- Check-in review date scheduled for: [Date, 2 weeks out].
```

---

## Worked Example: Senior Engineer Code Review Feedback

- **Situation**: During pull request reviews on Tuesday.
- **Behavior**: Left 18 one-line comments saying "rewrite this" without explanations or suggestions.
- **Impact**: Junior developer felt demoralized and spent 6 hours guessing what was wrong rather than learning the team standard.
- **Resolution**: Aligned on using conventional review prefixes (`nit:`, `blocking:`) with concrete code examples. Review turnaround improved 40%.

---

## Verification Checklist

- [ ] Situation specifies exact time, meeting, or event.
- [ ] Behavior describes observable actions that pass the "video-camera test".
- [ ] Impact clearly explains business, team, or project consequences.
- [ ] Zero subjective character assassinations ("unprofessional", "lazy", "arrogant").
- [ ] Concludes with a concrete forward-looking behavioral agreement.

---

## Anti-Patterns

- **The Feedback Sandwich**: Hiding critical performance issues between fake compliments, leaving the recipient thinking everything is great.
- **Mind Reading**: Claiming to know someone's intent ("You obviously don't care about this company").
- **Public Shaming**: Delivering developmental criticism in a public Slack channel or team meeting instead of 1-on-1.
