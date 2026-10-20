# Round HK Island Swim Tracker

Live in-flight-style display for the school swimming gala. A teacher swims continuous lengths at Sun Yat Sen Memorial Park Pool, and every length is mapped 1:1 onto a virtual swim around Hong Kong Island, finishing at VSA (Wong Chuk Hang).

Open `index.html` in a browser (needs internet for the map and fonts).

## Controls

| Key / button | Action |
|---|---|
| Space / Enter, **+1 LAP** | Teacher touched the wall (one pool length) |
| Backspace, **−1 lap** | Undo a mistaken tap |
| S | Start / pause the swim clock (starts automatically on the first lap) |
| U | Switch speed between m/s and km/h |
| ← / → | Step through the info carousel |
| H | Hide / show the control bar (for a clean projector view) |

Dropdowns pick the route (eastbound via Shek O & Stanley ≈ 34.7 km, or westbound via Pok Fu Lam ≈ 10.7 km), pool length (25/50 m) and map camera. Progress is saved in the browser, so a refresh keeps the count — press **Reset** before the gala.

## How it works

- **Speed** = distance of the last 5 lengths ÷ time between those "+1 LAP" presses. It drives the pool-lane swimmer, the map marker, and all time estimates.
- **Route** is a hand-traced line about 100–300 m offshore (edit `ROUTES` in `index.html` to refine). Map tiles © Esri.
- Built with [Leaflet](https://leafletjs.com/).
