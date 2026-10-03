# PADEKI – 16-pad sample groove station

🇬🇧 English · [🇭🇺 Magyar](README.hu.md)

**▶ Try it online:** [ekidio.github.io/padeki](https://ekidio.github.io/padeki/)

[![Watch the demo video (39 s, with sound)](screenshots/padeki-demo-poster.jpg)](https://ekidio.github.io/padeki/media/padeki-demo.mp4)

**[▶ Demo video](https://ekidio.github.io/padeki/media/padeki-demo.mp4)** · 39 s, with sound

**PADEKI** is a single-file, browser-based pad sampler and step sequencer in the spirit of classic MPC-style groove boxes. Load a loop onto the TAPE, chop it, put the slices on pads and program your beat. You can play it with the mouse, the computer keyboard or a USB MIDI pad controller.

It's written in vanilla JavaScript and the Web Audio API. There's nothing to install, no build step and no server. Everything runs in your browser, and your audio never leaves your computer.

PADEKI is an **EKIDIO SOUND** app. See also: [DAWEKI V3](https://github.com/Ekidio/daweki_v3).

## Features

### TAPE: the sample editor
- Drop an audio file onto the TAPE (or use **LOAD**): WAV, MP3, M4A, FLAC, OGG and **AIFF** (Logic / Pro Tools bounces). Zoom with the wheel and set the selection with the **IN / OUT** handles.
- **CHOP**: **AUTO** puts a marker on every transient, or split the loop into **4 / 8 / 16 / 32** equal slices.
- **+HIT / Alt-click** adds markers on the hits around the click. Click **IN** or **OUT** to zoom onto that marker and drag it sample-accurately; click again to see the whole sample. ← / → nudge 1 ms (Shift = 5 ms), and **SHIFT ALL** moves every marker at once.
- Parts of the sample that are on pads are **colored in the pad's color** on the TAPE. Hitting a pad shows its IN / OUT on the TAPE, ready to edit.
- **→ PAD**: click a slice, then click a pad. Or use **FILL EMPTY PADS** and **SELECTION → FREE PAD**.
- **LOOP → SLICE PAD** (ReCycle / REX style): puts the whole loop, with its slices, on **one pad**. The pad's row plays the slices at their original places. The loop follows any tempo and its pitch doesn't change.

### PADS
- **8 banks (A–H) × 16 pads**, each showing its own waveform. Use **LOAD KIT** for the built-in kits and **CLEAR** to empty a bank.
- **PAD EDITOR** (long-press or right-click a pad):
  - TUNE, DECAY, FILTER, LOW CUT, **EQ FREQ / EQ GAIN** (1-band bell EQ, ±15 dB), DRIVE, DIST, VOLUME, PAN, REVERB and DELAY
  - **DIST** creative distortion with three types: **FUZZ** (hard clip), **FOLD** (metallic wavefolder) and **CRUSH** (lo-fi bit reduction)
  - REVERSE and CHOKE groups
  - COPY / PASTE and rename
- **KEYS ♪**: play one sound chromatically.
  - Root-note detection with cent fine tune.
  - A centred 16-note range.
  - Piano layout on the computer keyboard: `A W S E D F T G Y/Z H U J K`, octave down / up with the key left of `X` / `X`.
- **Built-in kits**, all synthesized in code, all dry:
  - Electronic: EK-808, EK-909, DUSTY LO-FI, TRAP
  - Acoustic: FUNKY, ROCK, HEAVY, JAZZ

### Sequencer
- 8 patterns (**A–H**), each 1–4 bars of 16 steps. Chain patterns with **Shift-click**.
- **DRAW** lanes for per-note values: STEP, VEL, PITCH, **CHORD**, FILTER, DECAY, EQ FREQ, EQ GAIN, PAN, SLICE, REVERB and DELAY.
- **CHORD trigger**: in the CHORD lane, click a note and a piano opens over the pads. Click the keys to play one sample as any chord. The chord name (Cm7, F/C …) appears in the grid, with quick chord buttons, octave, inversion and copy / paste.
- **CHORD MEMORY**: one laptop key = one chord, defaulting to the C-major chords on A S D F G H J K. Store your own chords on keys, play them live and record them.
- **ROW LENGTH** (PAD EDITOR): a row can be 1–4 bars and repeats until the pattern ends, for example 1-bar drums under a 4-bar bass. Making a pattern shorter never deletes notes: they're kept hidden.
- **LOOP**: drag on the grid timeline to loop just that part (yellow frame). It snaps to beats; Shift snaps to single steps.
- **⤢ ZOOM** makes the selected row as tall as a pad. **↑ / ↓** step between rows.
- **M / S** (mute / solo) on every row. **🎲 RANDOM** writes a new rhythm for the bank, and **🎲 ROW** for a single row (on a slice pad it shuffles the slices).
- **DOUBLE** (with a **Shift-click / Shift-drag selection** it duplicates only the selected notes), **COPY →**, **CLEAR**, **UNDO**. **RENDER → PAD** renders what you hear (this pattern or its LOOP, with mute / solo and FX) onto an empty pad as a new sample. Delete / Backspace removes the selected notes.
- Swing, metronome, count-in and live recording from the pads, the keyboard or MIDI.

### Mix, export and projects
- **MASTER FX**: reverb and a tempo-synced **ping-pong delay** (echoes bounce left ↔ right, adjustable width), master volume and limiter.
- **EXPORT WAV** renders the pattern chain ×1 / ×2 / ×4 / ×8, in one of two modes:
  - **LOOP**: exact length, with the reverb or delay tail wrapped to the start so the file loops seamlessly.
  - **+ TAIL**: adds the ring-out at the end.
- **SAVE / OPEN** projects as `.padeki` files, with the samples embedded. Your last session is also kept: use **MENU → LAST SESSION**.
- **Web MIDI input** for 16-pad controllers (notes 36–51 → pads 1–16), plus MIDI start / stop.

### Four skins
**MENU → LOOK & CLICK**: CLASSIC, ICE, MODERN (default) and ANALOG.

| CLASSIC | ICE |
|---|---|
| ![CLASSIC](screenshots/padeki-classic.png) | ![ICE](screenshots/padeki-ice.png) |
| **MODERN** | **ANALOG** |
| ![MODERN](screenshots/padeki-modern.png) | ![ANALOG](screenshots/padeki-analog.png) |

## Quick start
1. Open [the web app](https://ekidio.github.io/padeki/), or download `index.html` and open it in your browser.
2. The **demo project** loads on start: press **▶** or **Space** and it plays right away.
3. Click the cells in the grid to change the beat. Use **LOAD KIT ▾** for another kit, or the blinking **LOAD** to put your own loop on the TAPE.
4. Drop a drum loop on the TAPE, press **AUTO**, then **LOOP → SLICE PAD**. Your loop now follows the project tempo.
5. Use **MENU → EXPORT WAV** or **SAVE** when you're done.

## Keyboard
| Key | Action |
|---|---|
| `Space` | Play / stop |
| `1 2 3 4` · `Q W E R` · `A S D F` · `Z/Y X C V` | Pads 13–16 · 9–12 · 5–8 · 1–4 |
| `↑ / ↓` | Previous / next row in the grid |
| `Cmd/Ctrl + ← / →` | Move the cell cursor along the row |
| `Cmd/Ctrl + ↑ / ↓` (Shift = fine) | Step the value of the note under the cursor in the selected DRAW lane (SLICE, PITCH, VEL …) |
| `← / →` (Shift = 5 ms) | Nudge the selected slice edge on the TAPE |
| `Esc` | Stop sending slices to pads |

The keys follow their physical positions, so QWERTZ (Hungarian, German) and QWERTY layouts both work.

## Browser support
Use a recent **Chrome** or **Edge** (recommended, required for Web MIDI), or Safari / Firefox. PADEKI is designed for desktop screens from 1280 to 1920 px wide.

## License
© Ekidio. All rights reserved unless stated otherwise.
