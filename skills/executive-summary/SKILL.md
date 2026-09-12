---
name: executive-summary
last_reviewed: 2026-09-06
group: Documents
description: >-
  Compress complex input into one page: recommendation first, then the supporting case. Use when
  condensing complex reports, briefings, or proposals for leaders.
---

# executive-summary

## Core Philosophy
Senior executives, board members, and technical leaders do not read 40-page reports line by line. They read under extreme cognitive load, scanning for bottom-line implications, operational trade-offs, and critical decisions. An executive summary is not an introductory abstract; it is a high-density, 1-page synthesis structured around the **Minto Pyramid Principle**: lead with the bottom-line recommendation first, followed by the supporting business rationale, financial impact, and immediate next decisions.

---

## 4-Step Executive Synthesis Framework

### Step 1: The Minto Pyramid Architecture (Answer First)
1. **Inverted Hierarchy**:
   - *Level 1: The Governing Conclusion (Headline & Recommendation)*: State the proposed action in the first 2 sentences.
   - *Level 2: Core Supporting Pillars (3 Max)*: The primary strategic arguments justifying the decision.
   - *Level 3: Hard Data & Operational Evidence*: Metrics, financial ROI, risk mitigations.
2. **The "So What?" Filter**:
   - Every paragraph must pass the executive test: *"Why does the CFO or CEO care about this specific detail right now?"* If it doesn't impact revenue, risk, or strategic roadmap, cut it.

### Step 2: The 1-Page Layout Discipline (Under 500 Words)
1. **Visual Density & Typography**:
   - Maximum 1 page (400–500 words).
   - Use bold lead-in phrases for bullet points to enable 15-second scanning.
   - Eliminate academic throat-clearing ("This document serves to analyze...").

### Step 3: Financial & Operational Trade-Off Table
1. **Decision Matrix Comparison**:
   - Provide a concise comparison table contrasting: Proposed Option vs Status Quo vs Primary Alternative.
   - Include hard estimates for: Total Cost, Implementation Time, Net Value/Savings, Key Risks.

### Step 4: Clear Decision Gate & Immediate Next Steps
1. **Explicit Asks**:
   - End with the exact decision required:
     - *"Required Decision: Approve $140,000 capital expenditure allocation for AWS dedicated migration."*
     - *"Sign-off required from: CTO and CFO by Friday, 5:00 PM."*

---

## Deliverable Format: Executive Decision Memo (`EXECUTIVE-SUMMARY.md`)

```markdown
# Executive Decision Memorandum: [Initiative Name]
*Date: [YYYY-MM-DD] | Author: [Name, Title] | Target Reviewers: [Exec Team / Board]*

## 1. Recommendation (Answer First)
We recommend **migrating our core analytics cluster from Snowflake to a self-hosted ClickHouse instance on AWS EC2**. This will reduce annual infrastructure expenses by **$420,000 (68%)** while cutting query response times from 4.2 seconds to 340 milliseconds, with a 6-week engineering transition.

## 2. Key Business Drivers
- **Cost Reduction**: Eliminates unpredictable Snowflake compute credit spikes; saves $35,000/month in baseline queries.
- **Performance Unlock**: Sub-second analytics enables real-time user-facing dashboards, unlocking enterprise Tier-3 upsells.
- **Data Sovereignty**: Keeps all raw customer event telemetry inside our private VPC, resolving enterprise EU customer compliance blockers.

## 3. Options Comparison Matrix
| Option | Upfront Engineering | Annual Ongoing Cost | Query Latency (p95) | Risk Profile |
|---|---|---|---|---|
| **ClickHouse (Recommended)** | 6 Weeks ($45k dev time) | $180,000 / year | 340ms | Managed cluster maintenance |
| Status Quo (Snowflake) | 0 Weeks | $600,000 / year | 4,200ms | Rapidly escalating costs |
| Alternative (BigQuery) | 4 Weeks | $410,000 / year | 1,800ms | Egress fees; high concurrency costs |

## 4. Required Executive Decision
- **Sign-off Requested**: Approval to commit 2 staff backend engineers for Sprint 14–16.
- **Decision Deadline**: [Date, Time] to begin migration before Q4 volume surge.
```

---

## Worked Example: Infrastructure Migration Executive Memo

- **Context**: Engineering team needed $120,000 approval to replace a failing proprietary message queue.
- **Execution**: Rewrote a 25-page technical spec into a 1-page Minto Pyramid executive memo highlighting $300,000 in prevented downtime losses.
- **Outcome**: Unanimous executive approval granted in 15 minutes during Monday leadership sync.

---

## Verification Checklist

- [ ] Core recommendation and business impact are stated in the very first paragraph.
- [ ] Total word count is under 500 words and fits strictly on 1 printable page.
- [ ] Includes a financial/operational options comparison table.
- [ ] All claims are backed by hard numbers, percentages, or dollar figures.
- [ ] Concludes with an explicit decision ask and deadline.

---

## Anti-Patterns

- **Burying the Lede**: Writing 4 pages of background history before revealing the actual recommendation on page 5.
- **Technical Jargon Dumps**: Explaining low-level Linux kernel parameters to a CFO instead of financial ROI.
- **Vague Asks**: Ending with "Thoughts?" instead of requesting specific sign-off on a clear decision.
