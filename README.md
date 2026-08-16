# LIGHTGRID

A Tron-inspired light-cycle overlay for [TikFinity](https://tikfinity.zerody.one/). Viewers beat **sectors** by sending TikTok gifts. Gifts throw identity discs that derez enemy cycles, fill sector energy, and smash open the next grid.

## Setup

1. Open **TikFinity Desktop** and connect it to your TikTok LIVE (`ws://localhost:21213/`).
2. Preview `index.html`. Press **D** for a demo gift, **C** for a combo.
3. OBS / TikTok LIVE Studio **Browser Source**:
   - Local file: `index.html`
   - Size `1920×1080`
   - Use the default black void as its own scene, or `index.html?overlay=1` for a transparent background
4. Flags: `?clean=1` hides settings, `?min=10&need=500` sets the gift threshold and Sector 1 energy.

## Gifts

Streakable gifts only fire a disc when `repeatEnd` is true. During the streak the cycle goes **TURBO** and the combo counter ticks. Fill a sector’s energy bar to clear it; each sector needs more diamonds than the last.
