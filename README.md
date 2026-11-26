# sfx-library

A Claude Code skill with 1,199 sound effects for video editing, sorted by what they do, plus the rules for using them: which sound goes on which visual event, what to layer it with, how many frames early it starts and how loud it sits under a voice.

## Install

```sh
git clone https://github.com/GFXER/sfx-library
cp -r sfx-library/skills/sfx-library ~/.claude/skills/
```

The clone is about 850 MB. Then in Claude Code: `/sfx-library`, or ask for "sound design for this edit" or "which sound for a card landing".

## What's inside

| Folder | Sounds | For |
|---|---:|---|
| `clicks/` | 114 | caption words, UI taps, settles |
| `ticks_typing/` | 17 | focus ticks, type-on trains |
| `pops/` | 9 | pills, badges, boxes drawing on |
| `impacts/` | 273 | stamps, card landings, punch-ins, hits |
| `sub_drops/` | 59 | drops, reveals, sub under a flash |
| `risers/` | 39 | builds that end on the cut |
| `whooshes_swells/` | 156 | transitions, swells |
| `reverses_rewinds/` | 13 | reverse impacts, tape stops |
| `shutters_flash/` | 26 | camera shutters, flash bursts, polaroid |
| `paper_foley/` | 79 | paper, pages, cards, glass |
| `glitch/` | 211 | RGB, datamosh, static, scans |
| `tape_film/` | 13 | projector, film wind, tape, vinyl |
| `ambience/` | 143 | room tone, crowds, rain, city |
| `stingers/` | 14 | logo and end cards |
| `sparkle_playful/` | 33 | chimes and sparkles, for playful content only |

- `SKILL.md`: when a sound is needed, a pick table for 20 events, layering, mixing.
- `references/CATALOG.md`: every file with its duration and peak, and a count of how many real mixes used it.
- `references/MOST_USED.md`: the 80 most-used sounds. Start there.

WAV sources are stored as lossless FLAC (24-bit where the source was 24-bit or float). A few files are MP3 because their source was MP3.

## Where the sounds come from

- Mixkit (free sound effects licence).
- Licensed Envato packs.
- The Lumoir SFX Essentials pack.
- Kenney and OpenGameArt (CC0).
- myinstants uploads.
- Sounds made for this library (`synth__` files).

File names keep their source prefix (`mixkit__`, `lumoir_`, `cc0_`, `mi_`). Each sound keeps its source's licence; check it before you resell or repackage anything.

Made by cheats1337.
