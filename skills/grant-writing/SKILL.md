---
name: grant-writing
last_reviewed: 2026-09-06
group: Documents
description: >-
  Write grant applications for nonprofits, research institutions and social enterprises, including
  prospect research. Use when authoring grant applications, proposal narratives, or budgets.
---

# grant-writing

## Core Philosophy
Grant writing for research institutions, open-source foundations, and non-profits is not an emotional plea for charity. Institutional grantmakers (NSF, DARPA, Sloan Foundation, Mozilla, philanthropic trusts) evaluate applications through rigorous scoring rubrics. Winning grants requires strict alignment with the funder’s strategic mandate, a falsifiable problem statement backed by primary empirical data, a structured Logic Model, and a line-item budget justification where every dollar maps to a measurable technical milestone.

---

## 4-Step Institutional Grant Proposal Architecture

### Step 1: Alignment & The Logic Model Framework
1. **Funder Mandate Deconstruction**:
   - Analyze the Request for Proposals (RFP) or Program Solicitation. Identify key scoring priorities: Innovation, Broader Impacts, Reproducibility, Sustainability.
2. **The 5-Stage Logic Model**:
   - *Inputs*: Personnel, hardware, compute infrastructure, partner institutions.
   - *Activities*: Core engineering, algorithmic research, community workshops, open-source releases.
   - *Outputs*: Lines of code, datasets published, peer-reviewed papers, conference presentations.
   - *Outcomes (1–2 Years)*: Measurable adoption (e.g. 5,000 active researchers using the library).
   - *Impact (3–5 Years)*: Systemic transformation (e.g. 50% reduction in public cloud compute energy waste).

### Step 2: Problem Statement & Significance (The Case for Need)
1. **Empirical Grounding**:
   - Never write broad assertions like "AI infrastructure is inefficient".
   - Ground in verified data: *"Over 74% of academic NLP labs lack access to clusters with > 8 GPUs, resulting in a 4x delay in replicating frontier open-weight models."*

### Step 3: Project Work Plan & SMART Milestones
1. **Specific, Measurable, Achievable, Relevant, Time-Bound (SMART) Objectives**:
   - Organize work into Work Packages (WPs) across quarters:
     - *WP1 (Q1-Q2)*: Core Algorithmic Optimization and Rust Prototype.
     - *WP2 (Q3)*: Cross-Validation across 5 University Benchmark Clusters.
     - *WP3 (Q4)*: Public Open-Source Release, Documentation & Educational Workshops.
2. **Key Performance Indicators (KPIs)**:
   - Commit to binary, auditable deliverables (e.g., "Publish v1.0 on GitHub under Apache 2.0 with 90% unit test coverage").

### Step 4: Budget Justification & Long-Term Sustainability
1. **Direct vs Indirect Costs**:
   - *Direct Labor*: Personnel salaries (Principal Investigator, Postdoc, Staff Engineer) calculated as % of FTE effort.
   - *Direct Equipment & Travel*: Specific cloud compute allocations (AWS credits) and conference presentation travel.
   - *Indirect / Overhead (F&A)*: Institutional negotiated indirect rate.
2. **The Sustainability Plan**:
   - Funders refuse to fund permanent dependencies. Explain how the project continues after grant capital is exhausted (e.g., foundation governance, enterprise sponsorship, institutional adoption).

---

## Deliverable Format: Grant Application Narrative (`GRANT-PROPOSAL.md`)

```markdown
# Institutional Grant Proposal: [Project Title]
*Funding Opportunity: [Grant Program Name / Solicitation #] | Target Amount: [$XXX,XXX]*

## 1. Executive Abstract & Broader Impacts
[250-word summary: Problem, proposed technical innovation, and measurable societal impact.]

## 2. Statement of Need & Significance
- **The Core Barrier**: [Specific technical/scientific bottleneck]
- **Empirical Evidence**: [Primary citation or survey data proving severity]
- **Why Existing Solutions Fail**: [Limitations of current proprietary/open alternatives]

## 3. Project Work Plan & Milestones (12-Month Schedule)
| Quarter | Work Package | Specific Deliverable | Measurable KPI |
|---|---|---|---|
| Q1 | WP1: Architecture | Formal mathematical specification | Peer-reviewed preprint on arXiv |
| Q2 | WP1: Engine Build | Core Rust compiler implementation | Passes 100% of benchmark test suite |
| Q3 | WP2: Deployment | Integration with PyTorch / HuggingFace | 500 beta downloads; 5 academic labs |
| Q4 | WP3: Dissemination | Open-source release (Apache 2.0) | 2,000 GitHub stars; documentation live |

## 4. Itemized Budget Justification
| Budget Category | Description | Justification | Total ($ USD) |
|---|---|---|---|
| Lead Research Dev | 0.50 FTE (12 mos) | Core compiler engine implementation | $75,000 |
| Cloud Compute | AWS GPU cluster (H100) | Running 50 benchmark evaluations | $22,000 |
| Dissemination Travel | NeurIPS Conference | Presenting research paper | $3,500 |
| **Total Requested** | | | **$100,500** |
```

---

## Worked Example: Open-Source Scientific Tool Grant

- **Proposal**: $125,000 grant application to the Sloan Foundation for reproducible scientific Python packaging.
- **Strategy**: Framed the application around the reproducibility crisis in computational biology. Committed to a specific logic model with 3 university pilot partners.
- **Outcome**: Awarded full grant funding; deliverables cited in 12 academic publications.

---

## Verification Checklist

- [ ] Proposal strictly aligns with the specific funding priorities of the target RFP.
- [ ] Logic Model maps inputs, activities, outputs, outcomes, and systemic impact.
- [ ] All milestones are SMART with auditable, binary deliverables.
- [ ] Budget items are itemized and mathematically justified per FTE and vendor quote.
- [ ] Sustainability plan explains longevity beyond the funding window.

---

## Anti-Patterns

- **Ignoring the Review Criteria**: Submitting a standard pitch deck instead of answering the funder's exact scoring rubric.
- **Vague Budgets**: Asking for $100,000 for "general development and miscellaneous expenses".
- **Academic Jargon Without Outcomes**: Writing 20 pages of dense theoretical equations without explaining the real-world application.
