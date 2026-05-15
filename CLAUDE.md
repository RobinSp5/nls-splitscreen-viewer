# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Single-file web application (`index.html`) for watching up to 4 YouTube streams simultaneously in a split-screen layout. No build tools, no dependencies — pure HTML/CSS/JS.

## Development

Serve locally (YouTube embeds require HTTP, not `file://`):

```
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Architecture

Everything lives in `index.html`:
- **CSS**: Dark theme, 3 grid layouts (2x2, 1x4, 4x1), fullscreen mode hides all UI except videos
- **JS**: Video ID extraction (supports youtube.com/watch, youtu.be, /embed/, /live/, bare IDs), localStorage persistence of URLs and layout, Fullscreen API integration
- **Embed URLs**: `https://www.youtube.com/embed/{id}?autoplay=1&mute=1` — videos autoplay muted per browser policy

## Key Behaviors

- State (video URLs + selected layout) persists via `localStorage` key `splitscreen`
- Fullscreen mode uses `document.fullscreenElement` API and hides header + cell headers + placeholders while preserving the active grid layout
- Language: German UI (placeholder text, button labels)
