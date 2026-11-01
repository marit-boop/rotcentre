# ROT Centre

Offline calculator for the **rotation centre by crane hook**, for several cranes at once.
It runs in the browser, installs on a phone like a normal app (PWA) and works without internet after the first open.

**Open:** https://marit-boop.github.io/rotcentre/  
**Android APK:** https://github.com/marit-boop/rotcentre/releases/latest

## Install on a phone

| Phone | How |
|---|---|
| **Android** | Install the APK from Releases (allow unknown sources), or open the link in Chrome → ⋮ → **Install app** |
| **iPhone (Safari)** | Open the link in **Safari** → Share □↑ → **Add to Home Screen** |

After the first open, the app works offline (on board, without Wi-Fi).

## How to use

1. **+ Crane** → name and crane position relative to midship: **Offset X** (+FWD / −AFT) and **Offset Y** (+SB / −PS).
2. Enter **Radius**, **Slew angle**, **Height of wire point**, **Heel**, **Trim**.
3. The result shows the rotation centre **Ahead/Astern** and **SB/PS**, plus a plan view.
4. **All** shows a summary of every crane.
5. **⋯ → Backup** lets you copy your cranes as text and paste them on another phone (*Import from text*). Useful for sharing a vessel's crane set with colleagues.

Each phone keeps its data locally (nothing is sent anywhere).

## Formula (same as the Excel sheet)

```
Ahead/Astern (+FWD/−AFT) = OffX + R·cos(Slew) + H·sin(Trim)
SB/PS        (+SB/−PS)   = OffY + R·sin(Slew) + H·sin(Heel)
```
R = radius, H = height of wire point. Slew 0° = bow, 90° = SB, 180° = stern, 270° = PS.
Heel +SB / −PS, Trim +FWD / −AFT.

> Decision-support tool only. Always verify against the vessel's approved lifting/stability documentation.
