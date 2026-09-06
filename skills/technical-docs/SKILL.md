---
name: technical-docs
group: Documents
description: >-
  Write API references, user guides, setup manuals and architecture docs with consistent
  terminology. Use when writing developer documentation, API guides, or tutorials.
---

# Technical Docs

Technical documentation serves four distinct modes (the Divio framework: Tutorials, How-To Guides, Reference, and Explanation). Documentation fails when these modes blur — such as when setup tutorials detour into deep architecture, or when API reference pages lack reproducible request and response payloads.

## Process
1. Classify documentation intent (Tutorial, How-To, Reference, or Architectural Explanation).
2. Establish reader prerequisites, environment requirements, and required tokens/keys.
3. Structure procedures with sequential, imperative, single-action steps.
4. Provide complete, runnable code examples with expected output.
5. Standardize domain terminology in a structured glossary.

## Output Format
## Technical Documentation: [Topic]
### Overview
[One-paragraph plain English summary of what this component accomplishes and why it exists]
### Prerequisites
- Node.js >= 20.0.0 or Python >= 3.11
- Environment variable `API_KEY` configured in `.env`
### Quickstart / How-It-Works
1. **Step 1: Install Dependencies**:
   ```bash
   npm install @company/sdk
   ```
2. **Step 2: Initialize Client**:
   ```typescript
   import { Client } from "@company/sdk";
   const client = new Client({ apiKey: process.env.API_KEY });
   ```
3. **Step 3: Execute Operation**:
   ```typescript
   const res = await client.resources.get("id_123");
   console.log(res.data);
   ```
### API Reference / Schema
- **Endpoint**: `POST /api/v1/resources`
- **Headers**: `Authorization: Bearer <token>`, `Content-Type: application/json`
- **Request Body**:
  ```json
  { "name": "sample", "tier": "standard" }
  ```
- **Response `201 Created`**:
  ```json
  { "id": "res_987", "status": "active" }
  ```
### Glossary & Terminology
| Term | Definition | Context / Scope |
|---|---|---|
| Idempotency Key | Unique header to prevent duplicate charge execution | All mutation endpoints |
| Tenant ID | UUID representing the client organization partition | Multi-tenant auth token |
## Audience-First Writing
Before writing: Who is reading this and what do they already know?
- **Developer docs**: Technical terms OK, code examples, values precision
- **End-user guides**: Minimal technical knowledge assumed, task-oriented, screenshots
- **Executive summaries**: No technical detail, focus on business outcomes
## Documentation Types (Divio System)
- **Tutorials**: Learning-oriented, hold reader's hand to first success
- **How-to Guides**: Goal-oriented, step-by-step for known goals
- **Reference**: Information-oriented, complete and accurate, dense
- **Explanations**: Understanding-oriented, background and context
## Style Rules
Active voice, one action per step, consistent terminology, test your own instructions.

## Critical rules
1. Prefer concrete, actionable steps over vague advice — the user needs executable output.
2. Ask for missing context only when it blocks a correct answer; otherwise state assumptions.
3. Do not invent personal identities, third-party credits, or external source claims.

## Additional notes (merged)
- Write README files that make developers want to use a project within the first 30 seconds
- Create API reference docs that are complete, accurate, and include working code examples
- Build step-by-step tutorials that guide beginners from zero to working in under 15 minutes
- Write conceptual guides that explain *why*, not just *how*
- Set up documentation pipelines using Docusaurus, MkDocs, Sphinx, or VitePress
- Automate API reference generation from OpenAPI/Swagger specs, JSDoc, or docstrings
- Integrate docs builds into CI/CD so outdated docs fail the build
- Maintain versioned documentation alongside versioned software releases
- Audit existing docs for accuracy, gaps, and stale content
- Define documentation standards and templates for engineering teams
- Create contribution guides that make it easy for engineers to write good docs
- Measure documentation effectiveness with analytics, support ticket correlation, and user feedback
- **Code examples must run** — every snippet is tested before it ships
- **No assumption of context** — every doc stands alone or links to prerequisite context explicitly
- **Keep voice consistent** — second person ("you"), present tense, active voice throughout
- **Version everything** — docs must match the software version they describe
- **One concept per section** — do not combine installation, configuration, and usage into one wall of text
- Lead with the result the user asked for.
- Use clear headings and bullet lists where helpful.
- Call out assumptions and open questions at the end.
- Stay specific to the Technical Writer workflow; avoid generic filler.

## Verification & Quality Checklist

- [ ] Every factual claim and statistic traced to a citable source.
- [ ] Reading level and terminology matched to the stated audience.
- [ ] Length and formatting fit the destination channel's limits.
- [ ] One clear call to action, placed where the reader will still be reading.

## Anti-Patterns & Constraints

- NEVER invent statistics, quotes, or sources.
- NEVER present an unverified figure as sourced.
- NEVER bury the central point below preamble the reader will not reach.
