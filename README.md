# Friction

**Song lyrics that sound said, not written.**

A Claude Code plugin for writing professional, radio-ready lyrics that sound authentically human - like overheard conversations or 2 a.m. confessions - rather than generic AI-generated text.

## The Problem

AI-generated lyrics sound like AI:
- Predictable metaphors (fire, wings, stars, hearts)
- Same structure every time (Verse-Chorus-Verse-Chorus-Bridge-Chorus)
- Time-of-day openings ("11 p.m. on a Tuesday...")
- Forced perfect rhymes
- No conversational texture

## The Solution

Friction enforces quality at every phase:
- 400+ genre-specific cliche detection
- Forced creativity rules (reject first ideas, delete obvious words)
- 7 structure templates (not always the default)
- 8 opening techniques (no time-of-day)
- "Said vs Written" test on every line

## Installation

### From Marketplace (recommended)

In Claude Code, run:

```
/plugin marketplace add forsonny/friction
/plugin install friction@forsonny-plugins
```

### From GitHub (manual)

```bash
# Clone and use directly
git clone https://github.com/forsonny/friction.git
claude --plugin-dir ./friction

# Or add to your project
git clone https://github.com/forsonny/friction.git .claude-plugin/friction
```

## Commands

| Command | Description |
|---------|-------------|
| `/friction:write-song <concept>` | Full pipeline from concept to finished lyrics |
| `/friction:check-lyrics` | Run anti-AI sweep on existing lyrics |
| `/friction:suggest-hooks <concept>` | Generate 5-7 hook options |
| `/friction:verify-song` | Full quality check on completed song |
| `/friction:rewrite-line <line>` | Make a single line more conversational |
| `/friction:cliche-check <phrase>` | Quick check against cliche database |

## Usage Examples

### Write a complete song

```
/friction:write-song country song about leaving your small town but feeling guilty
```

Output is ONLY formatted lyrics + Suno-compatible style guide. No phases, no working notes.

### Check existing lyrics

```
/friction:check-lyrics
[paste lyrics]
```

Returns issues found with specific suggestions.

### Generate hook options

```
/friction:suggest-hooks the guilt of success when friends are stuck
```

Returns 5-7 options with the first 3 marked as rejected (too obvious).

## Agent

The `song-writer` agent triggers automatically when you say:
- "Write me a song about..."
- "I need lyrics for..."
- "Help me write a song"

## Features

### Cliche Detection
400+ cliches organized by genre (country, pop, rock, hip-hop, R&B, folk, indie) plus universal AI tells. If detected, loops back with alternatives.

### The Rejection Rules
- Generate 5 hook ideas, reject first 3, use 4th or 5th
- Generate 35 words for word bank, delete 5 most obvious
- If cliches detected, return to Phase 1

### 7 Song Structures
| Structure | Pattern | Use Case |
|-----------|---------|----------|
| A: Classic Build | V-PC-C-V-C-B-C | Standard arc |
| B: Chorus First | C-V-C-V-B-C | Hook-driven |
| C: Slow Burn | V-V-PC-C-B-C | Storytelling |
| D: Bridge Early | V-C-B-V-C-O | Mid-song twist |
| E: No Bridge | V-PC-C-V-PC-C | Tight, focused |
| F: Extended Outro | V-C-V-C-O(8+) | Emotional landing |
| G: Minimal | V-C-V-C | Folk, intimate |

### 8 Opening Techniques
1. Dialogue Fragment
2. Sensory Snapshot
3. Action in Progress
4. Rhetorical Question
5. Confession/Admission
6. Contradiction
7. Place-Grounding
8. Object Focus

Never: Time of day ("It was 3 a.m...")

### Suno/Udio Ready
Output includes formatted style guide ready for copy-paste into AI music generators.

## File Structure

```
friction/
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── commands/
│   ├── write-song.md
│   ├── check-lyrics.md
│   ├── suggest-hooks.md
│   ├── verify-song.md
│   ├── rewrite-line.md
│   └── cliche-check.md
├── agents/
│   └── song-writer.md
├── skills/
│   └── songwriting/
│       ├── SKILL.md
│       └── references/
│           ├── cliche-database.md
│           ├── structures.md
│           ├── opening-techniques.md
│           └── anti-ai-rules.md
└── README.md
```

## License

MIT
