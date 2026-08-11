---
name: screenplay-writer
description: >-
  Writes screenplays and scripts following industry-standard formatting (Final Draft/Fountain) with scene headings, action lines, dialogue, and parentheticals. Use when writing short films, web series, video scripts, or adapting stories to screenplay format.
---

# Screenplay Writer

Standard screenplay format exists because it maps directly to screen time — one properly formatted page is roughly one minute of screen time, and industry readers (and software like Final Draft) expect the format exactly. Get the format right even in a quick draft; sloppy format signals amateur work regardless of how good the story is.

## Format reference (apply exactly)

```
INT. COFFEE SHOP - DAY

Action lines describe only what's seen or heard — present
tense, no camera directions unless truly necessary, no
internal thoughts or feelings that can't be shown on screen.

                    MAYA
          Dialogue is centered in its own
          block, character name in caps
          above it.

                    MAYA (CONT'D)
          Used when the same character keeps
          speaking after an action line
          interrupts them.

                    JORDAN
                    (quietly)
          Parentheticals go directly under
          the character name, used sparingly —
          only for delivery that isn't obvious
          from the dialogue itself.
```

- **Scene headings (sluglines):** `INT.`/`EXT.` + LOCATION + `- DAY`/`- NIGHT` (or other time marker). Always all-caps.
- **Action lines:** present tense, third person, only what a camera could capture — no "she feels betrayed," instead show the behavior that reads as betrayal.
- **Character cues:** all-caps, centered above dialogue.
- **Parentheticals:** used sparingly — only when the delivery genuinely isn't clear from the dialogue and staging alone. Overusing them is a common amateur tell.
- **Transitions** (CUT TO:, SMASH CUT TO:) — used sparingly in modern spec scripts; most scene changes don't need an explicit transition at all.

## Workflow

1. **Clarify scope** — a single scene, a full script, a beat sheet/outline, or a treatment (prose summary) are different deliverables with different formats. Ask if it's ambiguous.
2. **For a beat sheet or outline**, work at the level of story beats, not scene-by-scene prose — this is a planning document, not formatted script pages.
3. **For actual script pages**, apply the format above exactly. Don't write dialogue and action in prose paragraphs and call it a script.
4. **Write action lines lean.** Screenplays reward economy — cut adjectives and internal narration that a camera can't capture. If the user's draft is prose-heavy, actively trim it down when converting to script format, don't just reformat the same wordiness into script layout.
5. **Give characters distinct voices.** If writing dialogue for multiple characters, vary sentence length, vocabulary, and rhythm between them — flat, interchangeable dialogue is one of the most common weaknesses in amateur scripts.

## Structure frameworks (use when asked for outlining help)

- **Three-act structure**: Act 1 (setup, ~25% of runtime) → inciting incident → Act 2 (rising complication, ~50%) → midpoint turn → Act 3 (climax and resolution, ~25%).
- **Save the Cat beats** (15-beat structure): useful for feature-length outlining when the user wants a more granular beat-by-beat scaffold — see `references/save-the-cat-beats.md`.

## What NOT to do

- Don't write in prose-narrative style and call it a script — format matters here, not just content.
- Don't pad scripts with excessive camera direction (CLOSE ON, PAN TO) unless the user is specifically writing a shooting script rather than a spec script — spec scripts stay largely direction-agnostic and leave those calls to the director.

## Output format

For script pages, use the exact block format shown above (monospace-friendly, since real script format assumes a fixed-width font — mention this if the user will be pasting into a plain text editor rather than dedicated screenwriting software).

See `references/save-the-cat-beats.md` for the full 15-beat outline structure when the user wants outlining help before diving into pages.

## Verification & Quality Checklist
- [ ] Code compiles cleanly and passes all automated tests and typechecks without warnings.
- [ ] Edge cases, boundary conditions, and error states handled explicitly.
- [ ] No hardcoded secrets, test credentials, or insecure defaults introduced.
- [ ] Performance and resource utilization verified against baseline constraints.
