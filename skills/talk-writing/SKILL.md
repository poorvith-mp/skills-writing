---
name: talk-writing
group: Long form
description: >-
  Write a conference talk or keynote: through-line, one idea per slide, opening hook and honest
  timing. Use when scripting keynote talks, conference presentations, or lightning talks.
---

# talk-writing

## Core Philosophy
A conference keynote or technical presentation is not an academic lecture, nor is it a live reading of 40 text-heavy PowerPoint slides. A talk is live performance theater designed to plant a single unforgettable thesis into the audience's minds. Delivering a great talk requires a relentless Through-Line, respecting strict word-count timing constraints (130 words per minute), scripting the visual interplay between speaker and screen, and practicing an opening hook that grabs attention within 30 seconds.

---

## 4-Step Conference Presentation & Keynote Pipeline

### Step 1: The Through-Line (The Single Idea)
1. **The One-Sentence Rule**:
   - Every talk must have exactly **one** through-line:
     - Example: *"Compilers are not mysterious black boxes; they are simple state machines that every engineer can inspect and optimize."*
   - If a slide or story does not directly advance the through-line, delete it without mercy.
2. **The 3 Core Audience Questions**:
   - *Why this?* (Why does this topic matter right now?)
   - *Why you?* (What unique failure or data gives you authority to speak?)
   - *Why me?* (How does the attendee's daily work change tomorrow because of this talk?)

### Step 2: Timing & Word Count Budgeting
1. **The 130 Words-Per-Minute Constant**:
   - Conversational speaking pace on stage is strictly **120–140 words per minute**.
   - Standard Presentation Time Budgets:
     - *10-Minute Lightning Talk*: 1,200 words max.
     - *20-Minute Standard Tech Talk*: 2,500 words max.
     - *45-Minute Keynote*: 5,500 words max.
   - Going over your scheduled time is the ultimate cardinal sin of public speaking; it disrespects the organizers, the attendees, and the speakers following you.

### Step 3: Slide Deck Choreography (One Idea Per Slide)
1. **The Screen is Your Backdrop, Not Your Teleprompter**:
   - Slides should contain minimal text (target: $\le 6$ words per slide).
   - Use slides for visual punchlines, architecture diagrams, large readable code snippets (24pt font minimum), and high-contrast terminal captures.
2. **The Speaker vs Screen Dance**:
   - Never turn around and read your slides with your back to the audience.

### Step 4: The Scripting & Opening Hook Architecture
1. **The First 30 Seconds**:
   - Never begin with throat-clearing: "Hi everyone, thank you for coming, can you hear me okay, my name is Dave and today I'm going to talk about..."
   - Start directly inside the action or the controversy:
     - *"At 2:14 AM on Christmas Eve, our production database dropped 40 million customer accounts. And I was the one who ran the script."*
2. **The Call to Action (The Final Resonance)**:
   - End on a high, inspiring, actionable note that gives the audience a homework assignment for Monday morning.

---

## Deliverable Format: Keynote Script & Slide Plan (`KEYNOTE-SCRIPT.md`)

```markdown
# Conference Talk Script & Slide Plan: [Talk Title]
*Event: [Conference Name] | Duration: 20 Minutes (Target: 2,500 words)*
*The Through-Line: [Single sentence thesis]*

## 1. Slide & Script Choreography

### [Slide 1: Plain Black Screen with Blood-Red Text: "02:14 AM"]
**Spoken Voiceover (Time: 0:00 - 0:45 | 100 words)**:
At 2:14 AM on Christmas Eve, my phone buzzed. Then it buzzed again. By 2:16, sixteen engineers were on a frantic Zoom bridge staring at an empty AWS RDS console. 40 million records gone. 
Most post-mortems blame human error. Today, I'm going to prove to you that human error is a myth—and that our database tooling was actively engineered to deceive us.

---

### [Slide 2: Architecture Diagram — The Illusion of High Availability]
**Spoken Voiceover (Time: 0:45 - 2:30 | 220 words)**:
Let's look at what we thought we built. On paper, it was textbook elegance: multi-region active-passive replication with automated failover... [Continue technical breakdown]

---

### [Slide 3: Big Code Snippet: 3 Lines of Rust]
**Spoken Voiceover (Time: 2:30 - 4:00 | 195 words)**:
Here is the bug. Notice line 42. It looks innocent, doesn't it? But under heavy concurrent load...

## 2. Rehearsal Timing Verification
- [ ] Total word count: 2,420 words (Target: 2,500 words).
- [ ] Practice run 1: 18 minutes, 40 seconds.
- [ ] Code snippet slides tested for readability from 50 feet away (32pt font).
```

---

## Worked Example: 20-Minute Technical Keynote

- **Topic**: "Debugging Production Distributed Traces".
- **Execution**: Scripted to exactly 2,450 words across 28 visual slides. Opened with a 15-second personal outage story.
- **Outcome**: Delivered in 19 minutes, 15 seconds; ranked #1 speaker out of 42 presenters at the annual developer conference.

---

## Verification Checklist

- [ ] Talk possesses a single, clearly articulated through-line.
- [ ] Script adheres strictly to the 130 words-per-minute budget.
- [ ] Opening grabs attention within the first 30 seconds without biographical filler.
- [ ] Slide text is minimal (large diagrams/code; no bullet-point paragraphs).
- [ ] Total rehearsal time leaves at least 2 minutes of buffer under the session limit.

---

## Anti-Patterns

- **Wall-of-Text Slides**: Putting 8 bullet points of 14pt text on a slide and reading them verbatim.
- **Overrunning Time**: Speaking for 28 minutes in a 20-minute slot until the organizers cut your microphone.
- **The Apologetic Intro**: Spending the first 2 minutes apologizing for being nervous or complaining about slide formatting.
