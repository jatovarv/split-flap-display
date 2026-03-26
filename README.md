# Split Flap Display

A browser-based **split-flap (solari board) display** simulator — the classic mechanical departure boards from airports and train stations, recreated digitally with realistic animations and sound.

Open it in your TV browser, cast it to a screen, or just enjoy the nostalgia.

## Live Demo

**[Launch Split Flap Display](https://jatovarv.github.io/split-flap-display/)**

## Features

- **Realistic flip animation** — each character flips through intermediate letters just like the real thing
- **Mechanical sound** — synthesized 3-layer audio (impact click + resonant thud + rattle tail)
- **Multiple custom messages** — add as many messages as you want; they persist in localStorage
- **RSS feed integration** — live News, Sports, Tech headlines via RSS, plus Weather from wttr.in and a curated Quotes collection
- **Auto-rotation mode** — cycles through your saved messages AND feeds automatically, with configurable interval (8s to 1 min)
- **Fullscreen TV mode** — hides all controls for a clean display on your television
- **Customizable** — columns (20-40), rows (3-8), flip speed, and 5 color themes (yellow, green, white, orange, cyan)
- **Zero dependencies** — single HTML file, no build tools, no frameworks
- **Works offline** — custom messages work without internet; feeds require connectivity

## Quick Start

### Option 1: Use the live demo
Visit the [live demo](https://jatovarv.github.io/split-flap-display/) — that's it!

### Option 2: Run locally
```bash
# Clone the repo
git clone https://github.com/jatovarv/split-flap-display.git

# Open directly in your browser
open index.html
```

### Option 3: Serve it
```bash
# Any static server works
npx serve .
# or
python3 -m http.server 8000
```

## Usage

### Display a custom message
1. Type your message in the text area (use Enter for new lines)
2. Click **SHOW** to display it immediately
3. Click **+ ADD** to save it to your message list for auto-rotation

### Auto-rotation mode
1. Add one or more messages with **+ ADD**
2. Click **AUTO** — it will cycle through your messages + all feeds
3. Adjust the interval with the dropdown (8s, 12s, 15s, 20s, 30s, 1min)

### TV mode
1. Click the fullscreen icon (top right) or press `F11`
2. All controls hide automatically
3. Press `Spacebar` to toggle auto-rotation while in fullscreen
4. Press `Escape` to exit fullscreen

### Keyboard shortcuts
| Key | Action |
|-----|--------|
| `Ctrl + Enter` | Show current message |
| `Spacebar` | Toggle auto-rotation |
| `Escape` | Exit fullscreen |

## Customization

| Setting | Options |
|---------|---------|
| Columns | 20, 25, 30, 35, 40 |
| Rows | 3, 4, 5, 6, 8 |
| Speed | Fast, Normal, Slow, Very slow |
| Color | Yellow, Green, White, Orange, Cyan |

## How It Works

The display simulates a real split-flap mechanism:

1. Each character cell has a **top half** and **bottom half**
2. When changing, the top flap **folds down** (revealing the new character underneath)
3. Then the bottom flap **folds up** into place
4. Characters flip sequentially through the alphabet, just like real hardware
5. Sound is synthesized in real-time using the Web Audio API — no audio files needed

## Contributing

Contributions are welcome! Some ideas:

- Additional RSS feed sources
- More color themes or custom color picker
- Transition effects between messages
- Clock/date display mode
- Custom font support
- Mobile-optimized controls

## License

[MIT](LICENSE) — use it however you want.
