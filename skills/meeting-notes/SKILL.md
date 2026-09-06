---
name: meeting-notes
group: Documents
description: >-
  Turn notes or a transcript into decisions, action items with owners and deadlines, and a parking
  lot. Use when summarizing meetings, tracking decisions, or extracting action items.
---

# meeting-notes

## Core Philosophy
Dumping an unedited, 10-page raw automated audio transcription into Slack or Notion after a meeting is not helpful; it is an abdication of editorial responsibility. Raw transcripts are filled with conversational tangents, stuttering, and half-formed thoughts. High-impact meeting notes represent executive synthesis: extracting binding decisions, assigning clear action items with single accountable owners and due dates, capturing critical debate context, and shelving off-topic discussions in a parking lot.

---

## 4-Step Executive Meeting Synthesis Protocol

### Step 1: Real-Time Listening & Signal Filtering
1. **Filter the 90% Noise**:
   - Ignore pleasantries, small talk, scheduling back-and-forths, and circular debates.
   - Listen aggressively for trigger verbs: *"We agreed that...", "I will own...", "The deadline is...", "We decided not to..."*

### Step 2: The Decision Ledger (What Was Decided)
1. **Binding Outcomes First**:
   - Document decisions made as unambiguous declarative statements:
     - *Decision*: We will deprecate the v1 REST API on October 31, 2026.
     - *Decision*: Approved $15,000 budget for Q3 security penetration test.

### Step 3: The DRI Action Item Register (Who Does What by When)
1. **Directly Responsible Individual (DRI) Model**:
   - Every action item must have **exactly ONE individual owner** (shared ownership means zero ownership).
   - Must include an explicit, deterministic due date (never "soon" or "next sprint"):
     - *Format*: `[ ] [Action Verb + Deliverable] — @OwnerName (Due: YYYY-MM-DD)`
     - *Example*: `[ ] Draft RFC for OAuth token exchange — @Sarah (Due: 2026-09-12)`

### Step 4: Critical Context & The Parking Lot
1. **Key Debate Rationale**:
   - Capture *why* a decision was reached (the trade-offs considered):
     - *"Considered AWS DynamoDB vs PostgreSQL; chose Postgres due to team familiarity and lower transactional cost."*
2. **The Parking Lot (Scope Defense)**:
   - Record valuable off-topic ideas parked for future discussion so participants feel heard without derailing the meeting.

---

## Deliverable Format: Executive Meeting Notes (`MEETING-NOTES.md`)

```markdown
# Executive Meeting Notes: [Meeting Title]
*Date: [YYYY-MM-DD HH:MM] | Facilitator: [Name] | Note Taker: [Name]*
*Attendees: [Name 1], [Name 2], [Name 3] | Absent: [Name 4]*

## 1. Decisions Made
1. **Database Selection**: Standardized on PostgreSQL 16 for the billing microservice.
2. **Sprint Timeline**: Delayed Sprint 15 launch by 3 days to accommodate external SOC 2 audit.
3. **Budget Approval**: Approved $8,000 annual spend for Datadog APM expansion.

## 2. Action Items (DRI Register)
| Action Item / Deliverable | Single Owner (DRI) | Due Date | Status |
|---|---|---|---|
| Provision staging RDS Postgres cluster | @Dave (DevOps) | 2026-09-09 | Pending |
| Update OpenAPI specification with new `/billing` schema | @Elena (Backend) | 2026-09-11 | Pending |
| Schedule follow-up compliance sync with Legal | @Marcus (PM) | 2026-09-08 | Completed |

## 3. Key Discussion Rationale & Trade-offs
- **Postgres vs MongoDB**: MongoDB was evaluated for schema flexibility, but discarded due to lack of ACID transactional guarantees across multi-tier billing subscriptions.
- **Audit Preparedness**: Security team confirmed all IAM roles must be pruned before Friday.

## 4. Parking Lot (Deferred Topics)
- *Topic*: Migration from REST to gRPC for internal worker communication.
  - *Next Action*: Deferred to Q4 architecture offsite.
```

---

## Worked Example: Executive Product Steering Committee Notes

- **Meeting Duration**: 60 minutes of high-stakes heated debate across 8 engineering leads.
- **Deliverable**: Condensed into a 1-page markdown memo distributed to `#leadership` within 15 minutes of call completion.
- **Outcome**: 3 major strategic decisions ratified; 4 action items completed on time; zero confusion regarding owners.

---

## Verification Checklist

- [ ] Notes published and distributed within 60 minutes of meeting completion.
- [ ] Decisions made are prominently listed at the top.
- [ ] Every action item has exactly one designated individual owner and an explicit date.
- [ ] Summary captures underlying rationale and trade-offs, not verbatim speech.
- [ ] Off-topic discussions are captured in a structured Parking Lot.

---

## Anti-Patterns

- **The Unedited Transcript**: Pasting 15 pages of Otter.ai raw speech text into a channel.
- **Multiple Owners**: Writing "Action: Team will review API docs" (guarantees nobody does it).
- **Vague Deadlines**: Assigning action items with deadlines like "ASAP" or "ongoing".
