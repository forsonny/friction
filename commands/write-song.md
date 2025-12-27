---
name: write-song
description: Write a complete song from concept to polished lyrics with Suno-compatible style guide
allowed-tools:
  - Read
argument-hint: "<genre> <concept>"
---

# Write Song Command

Execute the full Friction songwriting pipeline. Takes a concept, outputs only formatted lyrics and style guide.

## Input Handling

Accept these formats:
- `genre + concept`: "country song about leaving home but feeling guilty"
- `concept only`: "song about leaving home but feeling guilty" (infer genre)
- `detailed brief`: genre, concept, emotional core, and keywords

If user provides minimal input, infer reasonable defaults rather than asking questions.

## Execution

1. Load the Friction Songwriting skill
2. Execute all 7 phases internally:
   - Phase 1: Concept Intake
   - Phase 2: Cliche Detection (loop back if needed)
   - Phase 3: Word Bank Generation
   - Phase 4: Hook Forging
   - Phase 5: Structure Selection
   - Phase 6: Anti-AI Sweep
   - Phase 7: Output Formatting

3. Apply all rejection rules:
   - Reject first 3 hook ideas
   - Delete 5 most obvious words from word bank
   - Loop back on cliche detection

4. Apply all quality checks:
   - No time-of-day openings
   - Near-rhymes over perfect rhymes
   - "Said vs written" test on every line

## Output

Show ONLY:

```
[Verse 1]
...

[Pre-Chorus]
...

[Chorus]
...

[Verse 2]
...

[Bridge]
...

[Final Chorus]
...

---

**Style Guide:**
[Genre description, tempo, instrumentation, vocal style, production notes, mix references]
```

## Rules

- NO phase headers or working notes in output
- NO word banks shown to user
- NO "here's what I did" explanations
- NO asking for confirmation between phases
- Section headers in `[brackets]`
- Style guide ready for Suno/Udio copy-paste
