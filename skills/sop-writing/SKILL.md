---
name: sop-writing
group: Documents
description: >-
  Write procedures anyone can follow: numbered steps, owners, inputs, outputs, escalation and
  executable templates. Use when authoring Standard Operating Procedures, runbooks, or checklists.
---

# sop-writing

## Core Philosophy
A Standard Operating Procedure (SOP) is not a theoretical essay or an aspirational policy document. An SOP is an executable algorithmic runbook for human or agentic operators. A great SOP is designed so that a qualified operator under extreme stress at 3:00 AM can execute the process with zero ambiguity, zero guesswork, and zero catastrophic errors. Every step must have deterministic inputs, numbered physical actions, observable acceptance criteria, and explicit escalation paths.

---

## 4-Step Standard Operating Procedure (SOP) Architecture

### Step 1: Scope, Governance & Pre-Flight Prerequisites
1. **Metadata & Ownership Header**:
   - SOP ID, Version (SemVer), Effective Date, Review Cadence (Annual/Bi-annual), Accountable Process Owner.
2. **Strict Purpose & Scope Boundaries**:
   - Exactly what this procedure covers, and what it does *not* cover.
3. **Prerequisites & Access Permissions**:
   - List required credentials, VPN access, software packages, and environment variables *before* the first execution step.

### Step 2: The Deterministic Numbered Step Sequence
1. **Imperative, Unambiguous Action Verbs**:
   - Begin every step with an active verb: *Click, Run, Verify, Copy, Export, Check*.
   - Never write passive guidelines: "Ensure that logs are looked at."
   - Write: *"1. Open Datadog dashboard `Prod-Ingestion`. 2. Inspect graph `p99 Latency`. 3. Verify value is below 200ms."*
2. **Copy-Paste Command Hygiene**:
   - Provide exact CLI commands or code snippets in fenced blocks. Never make operators guess flag names or parameters.

### Step 3: Observable Verification & Acceptance Gates
1. **The "How Do I Know It Worked?" Check**:
   - Every major step must specify its expected output:
     - *"Expected Output: Terminal displays `Deployment Complete: 12/12 pods healthy`."*
2. **Decision Trees & Branching Logic**:
   - Format conditional logic clearly:
     - *If status == 200*: Proceed to Step 4.
     - *If status == 500*: Jump to Troubleshooting Section 5.1.

### Step 4: Failure Handling, Rollback & Escalation Paths
1. **The Rollback Runbook**:
   - If the procedure fails mid-stream, provide exact rollback commands to restore the system to a safe baseline state.
2. **Escalation SLA & Contact Matrix**:
   - Who to page, on what channel, with what severity, if the procedure cannot be completed within 15 minutes.

---

## Deliverable Format: Production Standard Operating Procedure (`SOP-TEMPLATE.md`)

```markdown
# Standard Operating Procedure: Production Hotfix Deployment
*SOP ID: SOP-ENG-042 | Version: v2.1.0 | Owner: Platform Engineering Lead*
*Effective Date: [YYYY-MM-DD] | Review Cadence: Quarterly*

## 1. Purpose & Scope
This procedure governs the deployment of emergency hotfixes to production clusters outside the standard weekly CI/CD release cycle.

## 2. Prerequisites & Access Requirements
- Production AWS IAM Role `arn:aws:iam::123456789012:role/EmergencyDeployer`
- GitHub CLI (`gh`) authenticated with repository write access
- AWS CLI v2 and `kubectl` configured locally

## 3. Step-by-Step Execution Sequence

### Step 1: Branch Isolation & Verification
1. Checkout hotfix branch from `main`:
   ```bash
   git checkout main && git pull origin main
   git checkout -b hotfix/SEC-[IssueNum]
   ```
2. Run full test suite locally:
   ```bash
   npm run test:ci
   ```
   - *Acceptance Check*: Exit code 0; all test suites pass.

### Step 2: Build & Tag Container Image
1. Trigger automated hotfix build pipeline:
   ```bash
   gh workflow run hotfix-build.yml -f branch=hotfix/SEC-[IssueNum]
   ```
   - *Expected Output*: GitHub Actions emits image digest `sha256:...`.

### Step 3: Production Rollout & Canary Verification
1. Apply rollout to Canary pod pool (10% traffic):
   ```bash
   kubectl set image deployment/api-gateway api=ecr.internal/api:[Digest] -n production
   ```
2. Monitor error rates for 5 minutes:
   - Check Grafana dashboard `https://grafana.internal/d/canary-health`.
   - *Acceptance Gate*: 5xx error rate must remain < 0.01%.

## 4. Rollback & Contingency Plan
If Canary error rate exceeds 0.05%:
1. Roll back deployment immediately:
   ```bash
   kubectl rollout undo deployment/api-gateway -n production
   ```
2. Notify Incident Commander on Slack `#incident-war-room`.

## 5. Escalation Contacts
- **Primary On-Call SRE**: PagerDuty schedule `sre-tier-1`
- **Engineering VP**: Phone: [Number] (Page if outage exceeds 15 minutes)
```

---

## Worked Example: Database Restoration SOP

- **Context**: Recovery runbook for encrypted PostgreSQL database snapshot restoration.
- **Impact**: Step-by-step SOP allowed a junior engineer on night rotation to restore an accidentally dropped customer table in 11 minutes with zero data corruption.

---

## Verification Checklist

- [ ] Every procedural step starts with an active imperative verb.
- [ ] Commands and code snippets are 100% copy-pasteable with exact syntax.
- [ ] Expected observable output is specified for every critical step.
- [ ] Explicit rollback procedures are documented for failed executions.
- [ ] Escalation contact matrix includes named roles and paging channels.

---

## Anti-Patterns

- **Ambiguous Instructions**: Writing "Configure the network properly" instead of providing the exact IP tables or YAML config.
- **Missing Rollback Runbook**: Explaining how to push a change without explaining how to revert it if it breaks.
- **Untested Runbooks**: Writing an emergency disaster recovery SOP that has never been dry-run in a staging environment.
