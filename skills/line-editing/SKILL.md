---
name: line-editing
group: Voice and quality
description: >-
  Tighten a draft: cut filler, vary rhythm, sharpen verbs, and make every sentence earn its place.
  Use when polishing prose line by line for rhythm, concision, and clarity.
---

# line-editing

## Core Philosophy
Line editing is not mechanical copyediting (fixing typos and commas), nor is it developmental editing (restructuring plot and chapters). Line editing is the surgical craft of sentence-level music, economy, and power. It operates on the level of the clause: cutting flab, varying rhythmic cadence, activating inert verbs, untangling clumsy syntax, and ensuring every single word earns its existence on the page.

---

## 4-Step Surgical Line Editing Discipline

### Step 1: The Flab & Deadwood Sweep (Ruthless Pruning)
1. **Eliminate Inflated Phrasing**:
   - Replace wordy boilerplate with active equivalents:
     - *"In order to"* $ o$ *"To"*
     - *"Due to the fact that"* $ o$ *"Because"*
     - *"At the present moment in time"* $ o$ *"Now"*
     - *"There are many developers who believe"* $ o$ *"Many developers believe"*
2. **Purge Throats-Clearing Qualifiers**:
   - Cut weak hedges that betray insecurity: *"I believe that"*, *"It is interesting to note that"*, *"Clearly"*, *"Obviously"*, *"Essentially"*, *"Virtually"*.

### Step 2: Verb Activation & Nominalization Destruction
1. **Kill the "To Be" + Nominalization Disease**:
   - A nominalization is a strong verb murdered and turned into a weak noun. Resurrect the verb:
     - *Flabby*: "The committee reached a decision to conduct an investigation into the failure."
     - *Sharpened*: "The committee decided to investigate the failure."
     - *Flabby*: "Our service provides an improvement to query performance."
     - *Sharpened*: "Our service accelerates queries."

### Step 3: Cadence, Music & Sentence Length Variance
1. **The Gary Provost Sentence Music Rule**:
   - Never write 4 consecutive sentences of identical length (12–15 words). The ear tunes out.
   - Juxtapose short, explosive sentences with long, rhythmic, clause-rich sentences:
     - *"This sentence has five words. Here are five more words. Five-word sentences are okay. No, they are boring."*
     - *"Now listen. The music changes. Write sentences that build like waves, crashing with thunder, carrying the reader through clauses that twist and turn, before stopping cold. Like that."*

### Step 4: The Out-Loud Ear Test
1. **Acoustic Reading**:
   - Read the draft aloud at full conversational volume.
   - Any point where you stumble, lose breath, or have to re-read a clause is an architectural flaw in your sentence structure. Mark and rewrite it immediately.

---

## Deliverable Format: Line-by-Line Editorial Markup (`LINE-EDIT-LOG.md`)

```markdown
# Surgical Line Edit: [Article / Chapter Title]

## 1. Editorial Metrics & Pruning Score
- **Original Word Count**: 1,240 words
- **Edited Word Count**: 880 words (**29.0% reduction in deadwood**)
- **Passive-to-Active Transformation Count**: 18 instances

## 2. Sentence-by-Sentence Transformations

### Excerpt 1: Architecture Overview
- **Original**:
  > *"It is important to remember that when dealing with distributed microservices, there is a very real possibility that network latency will result in an increase in system failures."* (27 words)
- **Line Edited**:
  > *"In distributed microservices, network latency breeds cascading failures."* (8 words)
- **Rationale**: Cut 19 filler words; replaced passive nominalization with strong verb ("breeds").

### Excerpt 2: The Recommendation
- **Original**:
  > *"Our team made the determination that taking into consideration the cost factors, it would be advantageous to utilize an open-source solution."* (21 words)
- **Line Edited**:
  > *"We chose open source to slash cloud costs."* (8 words)
- **Rationale**: Replaced corporate flab ("made the determination", "taking into consideration") with active voice.

## 3. Recurring Patterns & Advice for the Writer
- Watch out for the "To Be + Noun" habit (e.g. "is an indication of" -> "indicates").
- Inject short 3-word punchline sentences after dense technical explanations.
```

---

## Worked Example: Technical Blog Post Transformation

- **Original Draft**: 1,850 words of rambling, passive architectural prose.
- **Line Edit**: Pruned to 1,210 words. Activated 34 weak verbs; dismantled 22 corporate passive constructions.
- **Impact**: Read-through completion rate increased from 18% to 64%; post hit #1 on Hacker News front page.

---

## Verification Checklist

- [ ] All instances of "in order to", "due to the fact that", and "there is/are" pruned.
- [ ] Nominalizations converted back into strong, active transitive verbs.
- [ ] Sentence length varies dynamically across short ($\le 6$), medium, and long structures.
- [ ] Weak qualifiers ("very", "really", "basically", "clearly") eliminated.
- [ ] Text read aloud to confirm flawless acoustic flow and breath pacing.

---

## Anti-Patterns

- **Editing for Vocabulary Vanity**: Replacing simple clear words with Latinate dictionary words ("utilize" instead of "use").
- **Fixing Only Grammar**: Correcting punctuation while leaving bloated, boring 40-word run-on sentences intact.
- **Robotic Symmetrical Cadence**: Keeping every sentence at exactly 14 words, creating synthetic drone.
