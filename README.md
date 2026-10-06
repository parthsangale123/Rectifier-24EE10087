# Rectifier Bench

Developed by Parth Sangale (24EE10087).

Interactive schematics and steady-state waveforms for single- and three-phase rectifiers.

## Circuits
| | 1-phase | 3-phase |
|---|---|---|
| Half-wave | Single diode | 3-pulse midpoint |
| Full-wave | Centre-tapped, 2 diodes | 6-pulse midpoint (hexaphase) |
| Diode bridge | 4 diodes | 6-pulse bridge |
| Thyristor bridge | 4 SCRs, firing angle α | 6 SCRs, firing angle α |

Half-wave and full-wave can also be switched to thyristors.

## Features
- Animated schematic: conducting devices, current path, gate pulses
- Waveforms over 2 cycles: supply, vo, io and ia, device voltage (with PIV)
- Controls: Vm, 50/60 Hz, R, L (0–500 mH), α, freewheeling diode
- Metrics: Vdc, Vrms, Idc, Irms, FF, RF, ripple frequency, PIV, conduction angle, mode, ideal Vdc

## Model
Time-stepped simulation (0.25° steps) run to steady state. RL load uses the exact exponential update per step. Devices are ideal; source inductance is ignored.

## Run locally
Open `index.html` in a browser, or:
```
python -m http.server 8000
```
then visit http://localhost:8000

## Deploy
- **GitHub Pages:** push this folder to a repo → Settings → Pages → Deploy from branch (`main`, root). `.nojekyll` is included.
- **Netlify:** drag the folder onto https://app.netlify.com/drop
- **Vercel:** run `vercel` inside the folder.

No build step or dependencies. Google Fonts (Barlow) load from the web; system fonts are used offline.
