# TikTok Roulette

A single-file gift roulette overlay for [TikFinity](https://tikfinity.zerody.one/). It connects to the local Event API, spins on completed gifts, and is ready for OBS / TikTok LIVE Studio as a browser source.

## Setup

1. Install and open **TikFinity Desktop**, then connect it to your TikTok LIVE.
2. Leave the Event API on the default endpoint: `ws://localhost:21213/`.
3. Open `index.html` in a browser to preview. Hover the bottom-right corner for settings. Press **D** for a demo gift or **C** for a demo combo.
4. In **OBS** (or TikTok LIVE Studio), add a **Browser Source**:
   - Local file: `index.html` in this folder
   - Width `1920`, height `1080`
   - Enable **Transparent** / shutdown source when not visible as you prefer
5. Optional OBS URL params:
   - `index.html?clean=1` hides the settings panel
   - `index.html?preview=1` uses a dark background for testing
   - `index.html?min=10&goal=20000` sets the spin threshold and diamond goal

## Gift combos

Streakable gifts (`giftType: 1`) only trigger a full wheel spin when `repeatEnd` is `true`. While a combo is still going, the overlay shows a live combo chip with `repeatCount` and does not spin yet.

Gifts below the **Min diamonds to spin** value still add to the goal bar, but they skip the wheel.
