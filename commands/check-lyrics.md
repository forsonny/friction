---
name: check-lyrics
description: Run anti-AI sweep on existing lyrics to find cliches and issues
allowed-tools:
  - Read
argument-hint: "<paste lyrics or describe where to find them>"
---

# Check Lyrics Command

Analyze existing lyrics against Friction quality standards.

## Input

Accept:
- Pasted lyrics directly in the command
- Reference to a file containing lyrics
- Request to analyze lyrics from conversation context

## Analysis Process

Run full anti-AI sweep from `references/anti-ai-rules.md`:

1. **Banned Phrase Scan**
   - Check against cliche database
   - Flag exact matches and near-matches

2. **"Said vs Written" Test**
   - Flag any line that sounds written rather than spoken
   - Mark lines that fail the "would someone actually say this?" test

3. **Rhyme Quality Check**
   - Flag forced perfect rhymes
   - Identify rhyme scheme issues

4. **Structural Issues**
   - Time-of-day openings
   - Generic opening patterns
   - Overused ending patterns

5. **Specificity Check**
   - Generic nouns that should be specific
   - Abstract language that should be concrete

## Output Format

```
## Lyrics Analysis

### Issues Found: [count]

**Line 3:** "In the depths of my heart"
- Issue: Banned phrase (abstract emotional language)
- Suggestion: "Somewhere in my chest" or describe the feeling physically

**Line 7:** "We danced all night"
- Issue: Time reference + generic activity
- Suggestion: What specific moment? Where exactly?

**Line 12:** "love / above" rhyme
- Issue: Overused perfect rhyme
- Suggestion: Try near-rhyme: "love / enough" or "love / shove"

### Summary
- Cliches found: X
- "Written" lines: Y
- Rhyme issues: Z
- Structural issues: W

### Overall Rating: [A/B/C/D/F]
```

## Notes

- Be specific about WHY each line fails
- Always provide a concrete alternative suggestion
- Don't just list problems - offer solutions
- Rate harshly but helpfully
