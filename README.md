# Pumpetuals ($PUMPETUALS)

Single-file site: `index.html` (no build step, no folders). Deploy as-is on Vercel or GitHub Pages.

## Set your links
Near the top of the script in `index.html`:

```js
var CONFIG={xUrl:'',xHandle:'',ca:'',buyUrl:''};
var PUMP_MARKETS=['BTC','ETH'];
```

- `xUrl`: your X profile link
- `ca`: contract address (blank until launch; page says "CA posted on X at launch")
- `buyUrl`: buy link once live
- `PUMP_MARKETS`: perps tagged "PUMP.FUN". Add markets here as pump.fun lists them.

## Data
- Live prices, 24h volume, open interest, funding, max leverage and 1h candles come from Hyperliquid's public info API (`https://api.hyperliquid.xyz/info`), polled every 10s. No API key needed.
- If the API can't be reached, the page shows a labelled sample snapshot.

## Calls
- Users' calls are tracked against the live Hyperliquid mark price and saved in their browser (localStorage) in this preview.
- Community calls, the leaderboard callers and the weekly pool are samples until launch. A shared backend is needed for a real public board.
