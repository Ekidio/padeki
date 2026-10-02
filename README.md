# PADEKI – 16-pad sample groove station

🇬🇧 English · [🇭🇺 Magyar](README.hu.md)

**▶ Try it online:** [ekidio.github.io/padeki](https://ekidio.github.io/padeki/)

![PADEKI – CLASSIC skin](screenshots/padeki-classic.png)

**PADEKI** is a single-file, browser-based pad sampler and step sequencer in the spirit of classic MPC-style groove boxes. Load a loop onto the TAPE, chop it, put the slices on pads and program your beat. You can play it with the mouse, the computer keyboard or a USB MIDI pad controller.

It's written in vanilla JavaScript and the Web Audio API. There's nothing to install, no build step and no server. Everything runs in your browser, and your audio never leaves your computer.

PADEKI is part of the DAWEKI family ([DAWEKI V3](https://github.com/Ekidio/daweki_v3)).

## Features

### TAPE: the sample editor
- Drop an audio file onto the TAPE (or use **LOAD**). Zoom with the wheel and set the selection with the **IN / OUT** handles.
- **CHOP**: **AUTO** puts a marker on every transient, or split the loop into **4 / 8 / 16** equal slices.
- **+HIT / Alt-click** adds markers on the hits around the click. Use **SHIFT ALL** and the **IN / OUT ±1 / 5 ms** buttons for sample-accurate trimming.
- **→ PAD**: click a slice, then click a pad. Or use **FILL EMPTY PADS** and **SELECTION → FREE PAD**.
- **LOOP → SLICE PAD** (ReCycle / REX style): puts the whole loop, with its slices, on **one pad**. The pad's row plays the slices at their original places. The loop follows any tempo and its pitch doesn't change.

### PADS
- **8 banks (A–H) × 16 pads**, each showing its own waveform. Use **LOAD KIT** for the built-in kits and **CLEAR** to empty a bank.
- **PAD EDITOR** (long-press or right-click a pad):
  - TUNE, DECAY, FILTER, LOW CUT, DRIVE, VOLUME, PAN, REVERB and DELAY
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
- **DRAW** lanes for per-note values: STEP, VEL, PITCH, FILTER, DECAY, PAN, SLICE, REVERB and DELAY.
- **⤢ ZOOM** makes the selected row as tall as a pad. **↑ / ↓** step between rows.
- **M / S** (mute / solo) on every row. **🎲 RANDOM** writes a new rhythm for the bank, and **🎲 ROW** for a single row (on a slice pad it shuffles the slices).
- **DOUBLE**, **COPY →**, **CLEAR** and **UNDO**.
- Swing, metronome, count-in and live recording from the pads, the keyboard or MIDI.

### Mix, export and projects
- **MASTER FX**: reverb and tempo-synced delay sends, master volume and limiter.
- **EXPORT WAV** renders the pattern chain ×1 / ×2 / ×4 / ×8, in one of two modes:
  - **LOOP**: exact length, with the reverb or delay tail wrapped to the start so the file loops seamlessly.
  - **+ TAIL**: adds the ring-out at the end.
- **SAVE / OPEN** projects as `.padeki` files, with the samples embedded. Your last session is also kept: use **MENU → LAST SESSION**.
- **Web MIDI input** for 16-pad controllers (notes 36–51 → pads 1–16), plus MIDI start / stop.

### Four skins
**MENU → LOOK & CLICK**: CLASSIC, ICE, MODERN, ANALOG.

| CLASSIC | ICE |
|---|---|
| ![CLASSIC](screenshots/padeki-classic.png) | ![ICE](screenshots/padeki-ice.png) |
| **MODERN** | **ANALOG** |
| ![MODERN](screenshots/padeki-modern.png) | ![ANALOG](screenshots/padeki-analog.png) |

## Quick start
1. Open [the web app](https://ekidio.github.io/padeki/), or download `index.html` and open it in your browser.
2. Click the blinking **LOAD KIT ▾** and pick a kit. Or drop your own loop onto the TAPE.
3. Click the cells in the grid to write a beat, then press **▶** or **Space**.
4. Drop a drum loop on the TAPE, press **AUTO**, then **LOOP → SLICE PAD**. Your loop now follows the project tempo.
5. Use **MENU → EXPORT WAV** or **SAVE** when you're done.

## Keyboard
| Key | Action |
|---|---|
| `Space` | Play / stop |
| `1 2 3 4` · `Q W E R` · `A S D F` · `Z/Y X C V` | Pads 13–16 · 9–12 · 5–8 · 1–4 |
| `↑ / ↓` | Previous / next row in the grid |
| `← / →` (Shift = 5 ms) | Nudge the selected slice edge on the TAPE |
| `Esc` | Stop sending slices to pads |

The keys follow their physical positions, so QWERTZ (Hungarian, German) and QWERTY layouts both work.

## Browser support
Use a recent **Chrome** or **Edge** (recommended, required for Web MIDI), or Safari / Firefox. PADEKI is designed for desktop screens from 1280 to 1920 px wide.

## License
© Ekidio. All rights reserved unless stated otherwise.
