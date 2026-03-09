# Wave Edit for Move Everything

A full-featured audio waveform editor for your Ableton Move. Trim, gain adjust, normalize, copy/paste, and mute sections of WAV files directly on the device.

## Features

- Waveform display with zoom and minimap overview
- Start/end marker selection with jog and knobs
- Real-time gain adjustment and normalization
- Cut, copy, paste, and mute operations
- Hold-to-audition playback with loop mode
- Undo support for all destructive edits
- Export selection to new file
- **Slice mode**: Even, Auto (transient detection), and Lazy (real-time SP-2400 style chop)
- **Slice export**: Save slices as individual WAVs, Drum Presets, or REX Loops
- **Loop view**: Seam editor for creating seamless loops
- **Recording**: Record from Resample, Line In, or any installed sound generator

## Prerequisites

- [Move Everything](https://github.com/charlesvestal/move-anything) installed on your Ableton Move
- SSH access enabled: http://move.local/development/ssh

## Install

### Via Module Store (Recommended)

1. Launch Move Everything on your Move
2. Select **Module Store** from the main menu
3. Navigate to **Tools** > **Wave Edit**
4. Select **Install**

### Build from Source

```bash
git clone https://github.com/charlesvestal/move-anything-waveform-editor
cd move-anything-waveform-editor
./scripts/build.sh
./scripts/install.sh
```

## Controls

### Edit Mode

| Control | Function |
|---------|----------|
| Jog wheel | Move selected marker |
| Jog click | Toggle start/end marker |
| Knob 1 | Move start marker |
| Knob 2 | Move end marker |
| Knob 3 | Zoom |
| Knob 4 | Vertical scale (1x–32x) |
| Knob 5 | Gain (Shift: normalize) |
| Any pad | Hold to audition selection |
| Shift+Pad | Preview near end marker |
| Mute | Zero out selection |
| Copy | Copy selection |
| Shift+Copy | Paste at cursor |
| Delete | Cut selection |
| Loop | Enter loop seam editor |
| Capture | Enter slice mode |
| Sample | Save (overwrite confirm) |
| Shift+Capture | Export selection to new file |
| Undo | Undo last edit |
| Back | Exit (warns on unsaved) |

### Slice Mode

| Control | Function |
|---------|----------|
| Jog | Navigate footer (Mode, Count, Select) |
| Jog click | Toggle edit/navigate |
| Knob 1 | Adjust slice start |
| Knob 2 | Adjust slice end |
| Knob 3 | Zoom |
| Knob 5 | Threshold (Auto mode) |
| Pads | Select + audition slice |
| Left/Right | Prev/next slice |
| Down | Split slice at midpoint |
| Up | Merge with previous slice |
| Sample | Save as: Slices, Drum Preset, or REX Loop |
| Capture | Exit slice mode |

Slice modes: **Even** (fixed count), **Auto** (transient detection), **Lazy** (real-time chop, SP-2400 style)

### Recording

Select **New Recording** in the file browser to record audio.

Choose a source: **Resample** (Move output), **Line In**, or any installed sound generator. Source plugins that have their own UI will open it for configuration — when playback starts, Wave Edit auto-returns and arms for recording.

| Control | Function |
|---------|----------|
| REC | Start/stop recording |
| Menu | Change recording source |
| Back | Cancel recording |

## Header Indicators

- `*` — unsaved changes
- `L` — loop mode enabled

## Credits

- **Move Everything framework**: [Charles Vestal](https://github.com/charlesvestal/move-anything)

## License

MIT License — See [LICENSE](LICENSE)

## AI Assistance Disclaimer

This module is part of Move Everything and was developed with AI assistance, including Claude, Codex, and other AI assistants.

All architecture, implementation, and release decisions are reviewed by human maintainers.
AI-assisted content may still contain errors, so please validate functionality, security, and license compatibility before production use.
