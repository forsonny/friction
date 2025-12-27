---
name: Friction Songwriting
description: This skill helps users write professional, radio-ready song lyrics that sound authentically human. Use when user asks to "write a song", "create lyrics", "help with songwriting", "I need a song about", or mentions wanting lyrics that don't sound like AI. Provides a 7-phase pipeline from concept to polished output with built-in cliche detection, forced creativity rules, and Suno-compatible formatting.
version: 1.1.0
---

# Friction Songwriting System

Write song lyrics that sound **said, not written**. This system produces authentic, conversational lyrics by enforcing anti-AI rules at every phase.

## Core Philosophy

Lyrics should sound like:
- Overheard conversations
- 2 a.m. confessions
- Things people actually say

NOT like:
- Greeting cards
- Poetry class assignments
- AI-generated text

---

## The 7-Phase Pipeline

Execute phases internally. User sees ONLY final output (formatted lyrics + style guide).

### Phase 1: Concept Intake

Gather from user:
- **Genre**: Country, pop, rock, hip-hop, R&B, folk, indie, etc.
- **Concept**: What the song is about (1-2 sentences)
- **Emotional Core**: The underlying feeling (not just "sad" - be specific: "the guilt of moving on too fast")
- **Keywords**: 3-5 words/phrases that must appear or be referenced

If user provides only a concept, infer reasonable defaults for genre and emotional core.

**Before proceeding:** Read 2-3 analyses from `song-samples/{genre}/` to calibrate.

### Phase 2: Cliche Detection

Check all inputs against the cliche database (see `references/cliche-database.md`).

**If cliches detected:**
1. Flag the specific cliches found
2. Loop back to Phase 1 with suggested alternatives
3. Do NOT proceed until concept is cliche-free

**Cliche categories to check:**
- Genre-specific tropes (pickup trucks for country, fire metaphors for pop)
- Universal AI cliches (echoes, voids, tender moments)
- Structural cliches (time-of-day openings, question endings)

### Phase 3: Word Bank Generation

Build a palette of 20-30 words related to the concept.

**Rules:**
1. Generate 35 words initially
2. **Delete the 5 most obvious words** - these are what AI would pick first
3. Include unexpected sensory words (textures, sounds, smells)
4. Include conversational filler appropriate to genre
5. Include at least 3 specific nouns (brand names, place names, objects)

**Good word bank example (breakup song):**
> voicemail, 3 a.m., radiator, coat pocket, Tuesday, half-empty, windshield, static, borrowed, kitchen light, probably, honestly, whatever, still

**Bad word bank example (same concept):**
> heart, tears, pain, memories, forever, broken, love, soul, dreams, hope

**Specificity examples from analyzed songs:**

| Generic | Specific (from real songs) |
|---------|---------------------------|
| car | "fast car," "brother's Tacoma," "Cadillac" |
| drink | "whiskey," "cheap wine," "half-empty Modelo" |
| place | "convenience store," "smoky room," "midnight train" |
| book | "poems from 13th century Italian" |
| money | "managed to save just a little bit" |

**Advanced technique - Invented Vocabulary:**
Consider creating new phrases for unnamed emotions:
- "Skinny love" - malnourished, fragile relationship
- "Whiskey lullaby" - euphemism for drinking to death
- "Tangled up in blue" - stuck in sadness/memory

See `references/techniques-library.md` for more.

### Phase 4: Hook Forging

Generate the central hook/chorus concept.

**Rules:**
1. Generate 5 hook ideas
2. **Reject the first 3** - they're too obvious
3. Use idea 4 or 5
4. Hook must be 2-8 syllables (shorter can be stronger)
5. Hook must pass the "would someone actually say this?" test
6. Hook should work as both song title and conversational phrase

**Hook quality test:**
- Could you imagine someone saying this to a friend? Yes = good
- Does it sound like a bumper sticker? No = good
- Is it trying too hard to be clever? No = good

**5 Hook Techniques (from analyzed songs):**

| Technique | Example | Why It Works |
|-----------|---------|--------------|
| Micro-Hook (2-3 syllables) | "Fast car," "Skinny love" | Memorable, lets verses explain |
| Contradiction Hook | "Whiskey lullaby" | Gentle word + brutal meaning |
| Universal Phrase | "We could have had it all" | Exact words people say |
| Rejection Hook | "We'll never be royals" | Denies instead of affirms |
| Delayed Hook | Don't Stop Believin' chorus at 3:20 | Context changes meaning |

**Hook Testing:**
- Say it out loud 5 times. Still feel it? Good.
- Would a stranger understand the emotion without context? Good.
- Can you hum it? Good.

### Phase 5: Structure Selection

Choose from 7+ structures based on emotional needs. See `references/structures.md`.

**DO NOT default to Structure A.** Select intentionally based on:
- Story complexity (more story = Slow Burn)
- Hook strength (strong hook = Chorus First)
- Emotional arc (needs twist = Bridge Early)
- Genre conventions (folk = Minimal)

| Structure | When to Use | Example Song |
|-----------|-------------|--------------|
| A: Classic Build | Standard emotional arc | Rolling in the Deep |
| B: Chorus First | Hook is undeniable | Most pop hits |
| C: Slow Burn | Story-driven, delayed payoff | Fast Car, Whiskey Lullaby |
| D: Bridge Early | Need a twist mid-song | Royals |
| E: No Bridge | Tight, no escape needed | Smells Like Teen Spirit |
| F: Extended Outro | Emotional landing | November Rain |
| G: Minimal | Stripped down, intimate | Most folk |

**Advanced structures from analyzed songs:**
- **Parallel Structure:** His story, then her story, same format (Whiskey Lullaby)
- **Delayed Chorus:** Hold chorus until 3+ minutes in (Don't Stop Believin')
- **Epic/No Chorus:** Seven verses, hook ends each verse differently (Tangled Up in Blue)

### Phase 6: Anti-AI Sweep

Line-by-line quality check before output. See `references/anti-ai-rules.md`.

**Check each line for:**

1. **Banned phrases**: Reference the banned list
2. **"Said vs Written" test**: Would someone actually say this?
3. **Rhyme quality**: Near-rhymes and slant rhymes > perfect rhymes
4. **Line variety**: Mix long and short lines
5. **Conversational texture**: Include at least 2-3 low-stakes "throwaway" lines
6. **Opening check**: Does NOT start with time of day (see `references/opening-techniques.md`)

**"Said Not Written" markers (from analyzed songs):**

| Marker Type | Written (Bad) | Said (Good) |
|-------------|---------------|-------------|
| Informal grammar | "I have seen" | "I seen" |
| Contractions | "going anywhere" | "goin' anywhere" |
| Hesitation | "I knew" | "I had a feeling" |
| Qualifiers | [none] | "probably," "honestly," "I mean" |
| Trailing off | "forever" | "on and on and on" |

**Advanced techniques to check:**
- Does it include fragmented syntax? ("Pour a little salt, we were never here")
- Does it have deliberate incoherence if genre-appropriate? (Rock/grunge)
- Does it use euphemism for brutal concepts? ("Put him to sleep")
- Is there communal witness where appropriate? ("We watched him...")

**If issues found:**
- Rewrite offending lines
- Re-run sweep until clean

### Phase 7: Output Formatting

Produce final output with two parts only:

**Part 1: Formatted Lyrics**
```
[Verse 1]
Line one here
Line two here
...

[Pre-Chorus]
...

[Chorus]
...
```

**Part 2: Style Guide (Suno/Udio Compatible)**
```
[Genre and subgenre with specific descriptors]
[Tempo and energy]
[Key instruments]
[Vocal style]
[Production notes]
```

**Example style guide:**
```
Modern country with acoustic drive and pedal steel accents. Mid-tempo,
reflective energy building to anthemic chorus. Male vocal with slight
rasp, conversational verses, soaring on chorus. Light percussion verse,
full band chorus. Mix references: Chris Stapleton meets Zach Bryan.
```

---

## Genre-Specific Guidance

### Country
- Specificity over generality ("convenience store" not "struggling")
- Let dialogue create character ("You still ain't got a job")
- Time jumps without announcement
- Community as moral witness ("We watched...")
- Structure C (Slow Burn) works well

### Pop
- Rejection of genre excess can work within genre (Royals)
- "We" makes personal feel communal
- Commit to consistent imagery throughout (fire, drowning, etc.)
- Regret over pleading in breakup songs
- Strong hook = Structure B (Chorus First)

### Rock
- Apathy as rage ("oh well, whatever, nevermind")
- Self-loathing over pure rebellion
- "Whatever" expresses more than manifestos
- Command/imperative openings work
- Structure E (No Bridge) for relentless energy

### Folk
- Biblical/literary anchoring adds weight
- Damaged things are beautiful ("cold and broken hallelujah")
- Tentative theology works ("maybe there's a God above")
- Pronoun instability as memory technique
- Structure G (Minimal) or epic verse-only

### Indie
- Invented vocabulary for new emotions
- Paradox in first line creates engagement
- Let production carry what lyrics don't say
- Title as atmosphere, not subject
- Fragmented syntax mirrors fragmented emotions

---

## Output Rules

1. **Show ONLY the final lyrics and style guide**
2. **No phase headers** in output
3. **No working notes** visible to user
4. **No word banks** in output
5. **No "here's what I did"** explanations
6. Section headers in `[brackets]`
7. Style guide formatted for copy-paste into Suno/Udio

---

## Quick Reference

### The Rejection Rules
- Reject first 3 hook ideas, use 4th or 5th
- Delete 5 most obvious words from word bank
- Loop back if cliches detected

### The Quality Tests
- "Would someone actually say this?"
- "Does this sound written or said?"
- "Is this what AI would generate first?"

### The Forced Variety Rules
- No time-of-day openings
- Use 8 opening techniques (see references)
- Choose structure intentionally, not by default
- Near-rhymes over perfect rhymes

### Advanced Techniques Checklist
- [ ] Invented vocabulary considered?
- [ ] Contradiction in hook or opening?
- [ ] Informal grammar present?
- [ ] Hesitation markers included?
- [ ] Specificity over abstraction?
- [ ] Genre-appropriate techniques applied?

---

## Reference Files

- `references/cliche-database.md` - 400+ genre-specific cliches to avoid
- `references/structures.md` - 7 song structure templates
- `references/opening-techniques.md` - 8 ways to start a song
- `references/anti-ai-rules.md` - Banned phrases and quality rules
- `references/techniques-library.md` - Advanced craft techniques from 100+ analyzed songs

---

## Song Samples Library

Reference real songs in `song-samples/` before writing. Each analysis includes:
- Structure breakdown with section purposes
- Opening technique used and why it works
- Hook analysis with syllable count and conversational test
- Notable lyrical techniques with examples
- "Said Not Written" lines with explanations
- Cliche avoidance strategies

**Before writing in a genre, read 2-3 analyses from that genre folder:**
- `song-samples/country/` - Storytelling, specificity, avoiding truck/beer cliches
- `song-samples/pop/` - Hooks, accessibility, avoiding generic empowerment
- `song-samples/rock/` - Energy, authenticity, avoiding darkness cliches
- `song-samples/folk/` - Intimacy, storytelling, avoiding nature cliches
- `song-samples/indie/` - Uniqueness, mood, avoiding introspection cliches
