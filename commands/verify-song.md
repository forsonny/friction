---
name: verify-song
description: Full quality verification of completed song against all Friction rules
allowed-tools:
  - Read
argument-hint: "<paste lyrics or reference file>"
---

# Verify Song Command

Comprehensive quality check against all Friction standards.

## Input

Accept completed lyrics (with section headers).

## Verification Checklist

### 1. Cliche Database Scan
- [ ] No genre-specific cliches
- [ ] No universal AI cliches
- [ ] No banned phrases
- [ ] No overused metaphors

### 2. Opening Technique
- [ ] Does NOT start with time of day
- [ ] Uses one of 8 approved techniques
- [ ] First line hooks attention

### 3. Structure Integrity
- [ ] Follows one of 7 approved structures
- [ ] Structure choice makes sense for content
- [ ] Not defaulting to Structure A without reason

### 4. Hook Quality
- [ ] 4-8 syllables
- [ ] Passes "would someone say this?" test
- [ ] Not a bumper sticker
- [ ] Works as title and phrase

### 5. Line-by-Line Quality
- [ ] All lines pass "said vs written" test
- [ ] No forced perfect rhymes
- [ ] Line lengths vary
- [ ] Includes 2-3 throwaway lines
- [ ] Specific nouns, not generic

### 6. Conversational Texture
- [ ] Has natural speech patterns
- [ ] Includes hesitation/filler where appropriate
- [ ] Fragments used effectively
- [ ] Contractions used naturally

### 7. Rhyme Quality
- [ ] Near-rhymes preferred over perfect
- [ ] No cliche rhyme pairs (love/above, heart/apart)
- [ ] Rhyme scheme varies

## Output Format

```
## Song Verification Report

### Overall: [PASS / NEEDS WORK / FAIL]

### Detailed Results

#### Cliche Scan: [PASS/X issues]
- [List any found]

#### Opening: [PASS/FAIL]
- Technique used: [which one]
- Notes: [any issues]

#### Structure: [PASS/NEEDS WORK]
- Structure detected: [A-G]
- Appropriate for content: [yes/no]

#### Hook: [PASS/X issues]
- Hook: "[the hook]"
- Syllables: X
- Issues: [any]

#### Line Quality: [X/Y lines pass]
- Failing lines:
  - Line X: [issue]
  - Line Y: [issue]

#### Conversational Texture: [PASS/NEEDS WORK]
- Throwaway lines found: [count]
- Natural speech patterns: [yes/no]

#### Rhyme Quality: [PASS/X issues]
- Forced rhymes: [list]
- Cliche rhymes: [list]

### Recommended Fixes
1. [Most important fix]
2. [Second fix]
3. [Third fix]
```

## Pass Criteria

- **PASS**: No critical issues, minor suggestions only
- **NEEDS WORK**: 1-3 issues that should be fixed
- **FAIL**: 4+ issues or any cliche detection hits
