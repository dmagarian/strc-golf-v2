# STRC Open: Saylor's Minute Drive ⛳

A single-file 3D golf "launch monitor" that turns **STRC** (Strategy's Variable Rate Series A "Stretch" Preferred) into a golf shot every minute. Michael Saylor tees off, and the market decides how it goes.

**Play it:** https://dmagarian.github.io/strc-golf-v2/

## The swing formula

**Accuracy = STRC price vs its $100 par**

| STRC price | Shot |
|---|---|
| ≥ $99.50 | Pure, dead straight |
| $99.00+ | Fairway with a little shape |
| $97.50+ | Rough |
| $95.00+ | Fairway bunker |
| $90.00+ | Sand or water |
| $82.00+ | Water or trees |
| $75.00+ | Trees, water or a shank |
| < $75 | Whiff, top, trees or water |

**Power = last-minute volume ÷ 10-day average minute volume (RVOL)**: carry ≈ 270 + 20·log₂(RVOL) yards.

**Hole-in-one** = price ≥ $99.50 **and** RVOL ≥ 3× (volume pumping). At ≥ 2× he drives the green.

## Data

Live quotes and 1-minute bars come from CNBC's public quote endpoints, called straight from the browser. When the market is closed, drives replay the last session minute by minute. If the feed is unreachable, a scripted demo tour plays instead. You can also switch to **Demo** or **Manual** mode, or fire one-off what-if shots.

## Run locally

It's one HTML file (Three.js loads from a CDN). Open `index.html` directly, or serve the folder:

```
python3 -m http.server 8000
```

URL options: `?mode=demo|manual|live`, `?interval=15|30|60|0`.

Fan-made proof of concept. Not affiliated with Strategy or CNBC. Not financial advice.
