---
name: translation
group: Repurposing and translation
description: >-
  Translate while preserving register, idiom and domain terms, flagging what doesn't carry across.
  Use when translating text across languages preserving nuance, tone, and idioms.
---

# translation

## Core Philosophy
Translation is not word-for-word lexical substitution across languages. Machine translation tools often produce grammatically valid sentences that sound unnatural, comical, or culturally offensive because they fail to capture register, tone, technical idiomatic conventions, and pragmatic context. Professional translation balances **Dynamic Equivalence** (conveying the exact emotional and conceptual meaning in natural target language) with **Formal Equivalence** (preserving precise legal and technical accuracy).

---

## 4-Step Technical Translation & Localization Framework

### Step 1: Source Deconstruction & Domain Glossary Formulation
1. **Terminology Standardization**:
   - Before translating, compile a **Do Not Translate (DNT)** and **Approved Technical Glossary**:
     - *DNT List*: Brand names, registered trademarks, API endpoints (`/api/v1/auth`), CLI commands (`git push`), programming keywords (`async/await`).
     - *Standardized Terminology*: Ensure domain terms (e.g. "thread pool", "concurrency", "distributed ledger") map to their established, accepted equivalents in the target language.

### Step 2: Register, Tone & Pragmatic Calibration
1. **Matching the Cultural Register**:
   - Calibrate social distance and formality:
     - German: *Du* (colloquial developer) vs *Sie* (enterprise legal/banking).
     - Japanese: *Keigo* (formal polite business) vs *Desu/Masu* (neutral technical documentation).
     - Spanish: *Tú* vs *Usted*.
2. **Preserving Rhetorical Stance**:
   - If the source text is dry, direct, and technical, the translation must not become flowery or emotional.

### Step 3: Idiomatic Localization & Cultural Adaptation
1. **Handling Untranslatable Idioms**:
   - Translate the underlying metaphor, not the literal words:
     - *"Bite the bullet"* $ o$ Do not translate into chewing ammunition; translate into accepting an inevitable hardship.
     - Currency, dates, and measurement units: Localize formatting (e.g. `YYYY-MM-DD` vs `DD/MM/YYYY`, metric vs imperial).

### Step 4: The Back-Translation & QA Verification Pass
1. **The Back-Translation Quality Gate**:
   - For high-stakes legal agreements, medical documentation, or core brand messaging:
     - Translate from Source $ o$ Target Language.
     - Have an independent linguist translate Target $ o$ Back to Source Language without seeing the original.
     - Compare original and back-translated text: discrepancies immediately expose semantic drift or ambiguity.

---

## Deliverable Format: Localization & Translation Dossier (`TRANSLATION-SPEC.md`)

```markdown
# Translation & Localization Dossier: [Project Name]
*Source Language: [e.g. English (US)] | Target Language: [e.g. German (DE)]*
*Domain: B2B Developer Documentation / Cloud Infrastructure*

## 1. Tone & Register Specifications
- **Target Audience**: German Software Engineers & DevOps Leads
- **Register / Formality**: Professional Informative ("Du" form for dev docs; "Sie" for legal Terms)
- **Voice**: Direct, technically precise, anti-marketing

## 2. Technical Glossary & Do Not Translate (DNT) Register
| Source Term (EN) | Approved Target Term (DE) | Context / Rules |
|---|---|---|
| Deployment | Deployment / Bereitstellung | Keep "Deployment" in dev contexts |
| Connection pool | Verbindungspool | Standard accepted translation |
| `kubectl apply` | `kubectl apply` | **DO NOT TRANSLATE** (CLI Command) |
| Latency | Latenz | Technical metric |

## 3. Side-by-Side Translated Excerpt
- **Source (EN)**:
  > *"When a node fails health checks, the orchestrator drains traffic immediately and spins up a healthy replica within 200 milliseconds."*
- **Target (DE)**:
  > *"Schlägt die Zustandskontrolle eines Knotens fehl, leitet der Orchestrator den Datenverkehr unverzüglich um und startet innerhalb von 200 Millisekunden ein funktionstüchtiges Replikat."*
- **Translator Note**: Translated "health check" to "Zustandskontrolle" and "drains traffic" to "leitet den Datenverkehr um" for natural technical German flow.
```

---

## Worked Example: Japanese API Documentation Localization

- **Challenge**: Literal machine translation of English error messages resulted in awkward, overly blunt phrases that offended Japanese enterprise customers.
- **Solution**: Re-translated using standard Japanese polite software conventions (*Kenjōgo* style for system constraints) while keeping API method names in original English ASCII.
- **Outcome**: Japanese enterprise developer satisfaction scores increased from 42% to 94%.

---

## Verification Checklist

- [ ] Technical terms match an approved domain-specific glossary.
- [ ] Brand names, API routes, and code syntax remain strictly untranslated.
- [ ] Tone and formality register (formal vs informal) consistently maintained.
- [ ] Idioms and cultural metaphors adapted dynamically rather than translated literally.
- [ ] Number, date, currency, and punctuation formats match target locale standards.

---

## Anti-Patterns

- **Translating Code and CLI Commands**: Translating `git commit` into foreign verbs, rendering terminal instructions unusable.
- **Ignoring Regional Variations**: Using European Spanish terms for a Mexican or South American user base.
- **Machine Translation Dumping**: Releasing raw Google Translate output without human review for technical accuracy.
