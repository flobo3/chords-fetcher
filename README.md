# chords-fetcher 🎸

A universal AI agent skill to fetch clean guitar chords and lyrics. 

Tired of ads, pop-ups, and messy guitar tabs when you just want to play a song? This script searches popular chord websites, extracts the pure text with chords, strips out unnecessary tabs, and formats it beautifully.

## Features
- **Multi-source search:** Automatically searches `mychords.net`, `ultimate-guitar.com`, and `amdm.ru` using DuckDuckGo.
- **Tab stripping:** Removes ASCII guitar tabs (`e|---`, `B|---`) to keep the output clean and readable on mobile devices.
- **Smart formatting:** Fixes spacing issues where chords are glued to lyrics (e.g., turns `AmWhite snow` into `Am White snow`).
- **Fallback mechanism:** If one site blocks the request or doesn't have the song, it seamlessly tries the next one.

## Requirements
- Python 3.10+
- `uv` (recommended for dependency management)

Dependencies:
- `requests`
- `beautifulsoup4`
- `ddgs` (DuckDuckGo Search)

## Usage

Run the script via `uv` to automatically handle dependencies:

```bash
uv run python chords.py <song_name_and_artist>
```

**Example:**
```bash
uv run python chords.py metallica unforgiven 2
```

## Integration with AI Agents (nanobot, OpenClaw, etc.)
Just drop this folder into your agent's skills directory. The included `SKILL.md` will tell your agent how to use it. When you ask your bot for chords, it will run the script and send you the clean text.