---
name: suggest-hooks
description: Generate 5-7 hook options for a song concept
allowed-tools:
  - Read
argument-hint: "<concept or emotional core>"
---

# Suggest Hooks Command

Generate hook options following Friction methodology.

## Input

Accept:
- Concept: "song about leaving your hometown"
- Emotional core: "the guilt of success when friends are stuck"
- Genre + concept: "country song about complicated family loyalty"

## Process

1. **Generate 7 initial hooks**
   - Don't filter yet, just generate

2. **Apply rejection rule**
   - Mark first 3 as "REJECTED - too obvious"
   - These are what AI would generate first

3. **Evaluate remaining 4**
   - Apply hook quality tests:
     - 4-8 syllables
     - "Would someone say this?"
     - Not a bumper sticker
     - Not trying too hard

4. **Rank final options**
   - Best to least best
   - Note the syllable count and why it works

## Output Format

```
## Hook Options for: [concept]

### Rejected (First Instincts - Too Obvious)
1. ~~"[hook]"~~ - [why it's obvious]
2. ~~"[hook]"~~ - [why it's obvious]
3. ~~"[hook]"~~ - [why it's obvious]

### Recommended Options

**#1 (Best):** "[hook]"
- Syllables: X
- Why it works: [specific reason]
- Sounds like: [what a person might actually say]

**#2:** "[hook]"
- Syllables: X
- Why it works: [reason]

**#3:** "[hook]"
- Syllables: X
- Why it works: [reason]

**#4:** "[hook]"
- Syllables: X
- Why it works: [reason]

### Notes
- [Any observations about the concept or direction]
```

## Hook Quality Tests

Run each hook through:
- [ ] 4-8 syllables
- [ ] Could be said to a friend
- [ ] Not a bumper sticker
- [ ] Not greeting-card sentiment
- [ ] Works as song title AND phrase
- [ ] Doesn't try too hard to be clever
