# Same Tune, New Chords

**Live site:** https://dphan123.github.io/same-tune-new-chords/

A music-theory app for the music module: one famous melody plays on a loop while you switch its style. The melody never changes; only the chords (the harmony) and the groove underneath it do. This is called **reharmonization**, a core arranging skill.

## What you can do

- Pick a tune: "Twinkle, Twinkle, Little Star", "Ode to Joy" or "Happy Birthday to You".
- Switch between six versions while it plays, without stopping: **Original, Jazz, Gospel, Film score, Bossa nova, Blues** (keys 1–6 work too).
- Watch the **chord strip** light up as each chord plays. New chords (a different root) are filled in, chords with the same root but added color (7ths, 9ths, a different bass note) are outlined, and every chord shows its **Roman numeral**.
- Read **how each style reharmonizes** and **the specific moves** in each tune: secondary dominants, tritone substitutions, passing diminished chords, IV/V, the minor-plagal "amen", borrowed ♭VI–♭VII–I, planing, blues turnarounds and more.
- See the **sheet music**: the melody with that style's chord symbols above and Roman numerals below.
- Change the melody instrument, or turn the melody off to hear only the chords.

Every version has a link, for example `#ode-gospel` or `#birthday-film`.

## How it was made

- The 18 reharmonizations (3 tunes × 6 styles) and the analysis were written with Claude, and every chord was checked against the melody note it sits under.
- Melodies are public domain, so they are written note for note.
- Instruments are real recorded samples from the FluidR3 General MIDI soundfont, loaded note by note as needed. Drums are synthesized with the Web Audio API.
- Each loop is rendered in the browser with an OfflineAudioContext. Switching styles crossfades to the new version at the same point in the tune.
- Sheet music is generated as ABC notation and drawn with abcjs.

No server, no API keys, no build step: it is one `index.html` file.

## Run locally

```
python3 -m http.server
```

Then open http://localhost:8000.
