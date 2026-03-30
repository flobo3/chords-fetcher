# chords-fetcher

Fetch clean guitar chords and lyrics for Russian and international songs without ads, tabs, or garbage.

## Usage
When the user asks for chords to a song (e.g., "аккорды Кино Звезда по имени Солнце", "chords behind blue eyes"), use the `exec` tool to run the fetcher script.

```bash
uv run python chords.py <song_name_and_artist>
```

## Features
- Searches across multiple sources: amdm.ru, mychords.net, ultimate-guitar.com.
- Automatically strips out guitar tabs (e|---, B|---, etc.) to keep the output clean.
- Fixes spacing issues where chords are glued to lyrics.
- Returns pure text ready to be sent to the user.

## Notes
- Run the script from the skill's directory: `C:\Users\BSC_User\.nanobot\workspace\skills\chords-fetcher`
- If the script returns an error or cannot find the song, inform the user.