---
name: rewrite-line
description: Take a single line and make it sound more conversational
allowed-tools:
  - Read
argument-hint: "<the line to rewrite>"
---

# Rewrite Line Command

Transform a "written" line into a "said" line.

## Input

Accept a single line of lyrics that sounds too polished, poetic, or AI-generated.

## Process

1. **Diagnose the problem**
   - Why does it sound "written"?
   - Is it too abstract?
   - Too many syllables?
   - Too formal?
   - Trying too hard?

2. **Apply fixes from anti-AI rules**
   - Remove adjectives
   - Make it shorter
   - Add hesitation if appropriate
   - Use contractions
   - Fragment the sentence
   - Replace abstract with concrete

3. **Generate 3 alternatives**
   - Each taking a different approach
   - All must pass "would someone say this?" test

## Output Format

```
## Original Line
"[the line]"

## Diagnosis
- Problem: [what makes it sound written]
- Specific issues: [list]

## Rewrites

**Option 1 (Recommended):** "[rewritten line]"
- Approach: [what I did]
- Why it works: [brief reason]

**Option 2:** "[rewritten line]"
- Approach: [what I did]

**Option 3:** "[rewritten line]"
- Approach: [what I did]

## Before/After Test
- Original: Does it sound said? NO
- Rewrites: Do they sound said? YES
```

## Common Fixes

| Problem | Fix |
|---------|-----|
| Too abstract | Find the physical/specific version |
| Too long | Cut words until it feels casual |
| Too formal | Add contractions, remove formality |
| Too clever | Simplify, understate instead |
| Too poetic | Remove metaphor, say it plainly |
| Generic | Add specific nouns, names, places |
