---
name: sfx-library
description: >-
  A licensed library of 1,199 sound effects sorted by role (clicks, ticks, pops, impacts, sub drops, risers, whooshes, reverses, shutters, paper and foley, glitch, tape and film, ambience, stingers), plus how to use them: when a visual event needs a sound and when it doesn't, which sounds to layer together, lead frames, levels in dB and an offline mix recipe. Use when a video, reel, motion graphic or edit needs sound design: "add SFX", "sound design", "which sound for…", "click/pop/shutter/hit/riser/whoosh for…", "SFX cue sheet", "/sfx-library", or when a mix script needs file paths. Do NOT use for: choosing music, voice cleanup or voice effects, or loudness-only fixes.
---

# SFX library

The sounds are in `sounds/<role>/` next to this file. All paths below are relative to this skill folder.
- `references/CATALOG.md` lists every file with its duration, peak and a **uses** count: how many past mixes used it, so a high number means the sound has been proven in real work.
- `references/MOST_USED.md` lists the top 80. Start there.
- Every sound is licensed for use in videos, including commercial and client work.

## When a sound is needed
- **Yes:** every visual event the viewer should feel: text or a card arriving, a zoom punch, a flash, a cut to a new section, a reveal, a counter, a photo, a page.
- **No:**
  - every cut in a music edit. There the drums are the cue, so add sound only where the picture has its own event.
  - under a spoken word you want understood.
  - two big sounds within ~6 frames of each other.
  - a sound that tells nothing new (one on the card landing is enough, not on its shadow and its badge as well).
- **Density:**
  - Talking-head and UI-heavy reels: about 2 cues per second (a soft click per caption word).
  - Cinematic edits: a few strong moments with silence before them.
  - Education: quiet and sparse.
- A sound that is loud or sweet (sparkles, chimes) cheapens premium work. Keep `sparkle_playful/` for kids, games or comedy.

## Pick by event
Levels are peak-normalised targets under a voice at about −15 LUFS. Lead = how many frames the sound starts before the visual (at 24–30 fps; scale for 50/60).

| Event | Layer it as | First picks | Level dB | Lead |
|---|---|---|---|---|
| Caption word appears | click (rotate 3 variants) | `clicks/modern-click__Modern_Click_{1,2,3}.flac`, `clicks/mixkit__single-classic-click-1116.flac` | −33 | 2 f |
| Text lands / resolves | click + focus tick | + `clicks/synth__glass_tick_{2800,3500,4200}hz.flac` | −33 / −34 | 2 f / 0 |
| Key word stamp | click + soft thump (+ hit for a slam) | `impacts/synth__soft_landing_thump.flac`, `impacts/hit__Hit.flac` (cut at 0.6 s) | −29 / −27 | 1 f |
| Card, widget, photo lands | thump at land, paper on paper cards | `impacts/synth__soft_landing_thump.flac`, `paper_foley/mixkit__paper-slide-1530.flac` | −29…−31 | 1 f |
| Pill, badge, box draws on | bloop | `pops/synth__bloop_up_1.flac`, `pops/synth__bloop_up_2.flac` | −30 | 1 f |
| Move settles | soft tone click | `clicks/mixkit__cool-interface-click-tone-2568.flac` | −31 | 0 |
| Punch-in zoom | low drum + settle click 7 f later | `impacts/mixkit__deep-cinematic-subtle-drum-impact-549.flac`, `impacts/mixkit__drum-deep-impact-563.flac` | −25…−30 | 1 f |
| Flash / invert / white frame | burst + shutter | `shutters_flash/synth__flash_burst_0.3s.flac` + `shutters_flash/mixkit__camera-shutter-click-1133.flac` | −28 / −30 | on the first bright frame |
| Photo, polaroid, grid tile | shutter (vary: nikon, hard, old) | `shutters_flash/mixkit__nikon-camera-shutter-1434.flac`, `…camera-shutter-hard-click-1430.flac`, `…old-camera-shutter-click-1137.flac` | −24…−30 | 0 |
| Type-on / scramble | tick train, end on the resolve | `ticks_typing/synth__tok_train_{12,15,24,30}ps_0.5s.flac` (chain for longer), `clicks/mixkit__hard-typewriter-click-1119.flac` | −32 | 3–5 f before the first glyph; stop within 2 f of the resolve |
| Paper, newspaper, receipt, page | page/slice + a soft thump on land | `paper_foley/mixkit__page-turn-single-1104.flac`, `…paper-quick-slice-2384.flac`, `…paper-quick-movement-2380.flac` | −28 | 1 f |
| Big reveal / drop | silence pocket → sub drop + hit | `impacts/bass-drop__bass-drop-01.flac`, `sub_drops/` (10–14 dB under the music) | −22 | 0; dip the music −30 dB for ~5 f before |
| Build into a new section | riser that ends on the cut | `risers/synth__charge_riser_2s_ends_on_cut.flac`, `risers/mixkit__cinematic-synth-riser-645.flac` | −26 | ends exactly on the new section's first frame |
| Rewind, reverse, suck-in | reverse impact (last ~1.5 s) | `reverses_rewinds/mixkit__reverse-cinematic-impact-trailer-784.flac`, tape stops in the same folder | −26 | peak on the cut |
| Transition between shots | low-passed whoosh, few | `whooshes_swells/swipe__Swipe_2.flac`, `…mixkit__quick-air-woosh-2605.flac` | −35 | peak on the midpoint |
| Clock, time, countdown | tick-tock or pulse | `risers/mixkit__tick-tock-clock-close-up-1059.flac`, `clicks/click-time-pulse__Click_Time_Pulse.flac` | −27 | 2 f |
| Glitch, RGB split, datamosh | ≤ 0.3 s glitch, never twice the same | `glitch/` | −30 | 0 |
| Logo / end card | stinger or a hit + air tail | `stingers/`, `impacts/` | −24 | 0 |
| Retro, film, VHS look | projector run, wind, tape mech under the scene | `tape_film/` | −32 bed | starts with the look |
| Scene bed | room tone, crowd, rain, mono | `ambience/` | −30 or lower | under the whole scene |

Rotate variants (the 3 clicks, 2 bloops, 3 glass ticks, the shutters) so the same file never plays twice in a row. Pitch ±1–2 semitones also helps.

## Combining layers
- A designed hit is 3–5 short layers that each own a band: sub (`sub_drops/`) + body (`impacts/`) + transient (`clicks/` or `shutters_flash/`) + air tail (`whooshes_swells/`, low-passed). Offset them by 0–2 f, not stacked on one sample.
- High-pass the body layer around 120 Hz when a sub is under it. Low-pass whooshes at ~1.5 kHz so they sit behind the voice.
- Before a big moment, make a silence pocket: pull the music and the SFX down 4–8 f before the hit.
- Glints and light sweeps: nothing, a muted air texture, or a soft sub. Not a sparkle.

## Mixing
- Mix offline to one WAV: per cue `atrim` (`max_dur`), `adelay`, `volume`, a 2–3 ms `afade` in and out, then `amix` and `loudnorm`. Don't leave the final mix as SFX layers in an editor timeline.
- Many files peak near 0 dBFS (see the `peak` column). Set gain from the table, never at the file's own level.
- Targets:
  - Music-led edits: −14 LUFS, true peak −1.
  - Speech: voice ≈ −15 LUFS, music ≥ 11 dB under the voice, or a muffled bed (low-pass ~500 Hz) 6–8 dB under.
- Keep SFX mono and centred. Only a wide ambience bed is stereo.
- Check on phone speakers: no cue louder than the word it sits on.

## Find a sound
```sh
grep -i "shutter" references/CATALOG.md | head
python3 -c "import json;[print(r['uses'],r['dur'],r['path']) for r in json.load(open('references/catalog.json')) if r['role']=='impacts' and r['dur']<1]" | sort -rn | head
```
How to choose:
- Prefer files with uses > 0.
- Role folders came from pack categories and titles, not from listening, so audition the sound with the picture before committing.

## Adding sounds
Put a new file in the role folder it fits, then add a row for it to `references/catalog.json` (path, role, title, dur, peak_db, uses 0). Keep the file short and trimmed, and note its licence in the README.
