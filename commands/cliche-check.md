---
name: cliche-check
description: Quick check of a phrase or concept against the cliche database
allowed-tools:
  - Read
argument-hint: "<phrase or concept to check>"
---

# Cliche Check Command

Fast lookup against the Friction cliche database.

## Input

Accept:
- Single phrase: "fire in my heart"
- Concept: "song about a pickup truck on a dirt road"
- List of words/phrases to check

## Process

1. Check input against all cliche categories:
   - Universal AI cliches
   - Genre-specific cliches
   - Structural cliches
   - Overused rhymes

2. Flag any matches or near-matches

3. Provide alternatives for each hit

## Output Format

### If cliches found:

```
## Cliche Check Results

### Input: "[the input]"

### Matches Found: [count]

**"[phrase]"**
- Category: [Universal AI / Country / Pop / etc.]
- Why it's cliche: [brief explanation]
- Alternatives:
  - "[option 1]"
  - "[option 2]"
  - "[option 3]"

**"[phrase 2]"**
- Category: [category]
- Why: [reason]
- Alternatives:
  - "[option 1]"
  - "[option 2]"

### Verdict: NEEDS REVISION
Revise using the alternatives above before proceeding.
```

### If clean:

```
## Cliche Check Results

### Input: "[the input]"

### Matches Found: 0

### Verdict: CLEAR
No cliches detected. Safe to proceed.

### Caution Notes:
- [Any near-misses to watch for]
- [Adjacent cliches that might emerge during writing]
```

## Quick Reference

Flag immediately if input contains:
- pickup truck, dirt road, tailgate (country)
- fire, flames, burning, desire (universal)
- depths, void, echoes, tapestry (AI abstractions)
- forever and always, meant to be (greeting card)
- started from the bottom, real recognize real (hip-hop)
- autumn leaves, wandering soul (folk)
