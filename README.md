# DMR-Calculator

A standalone split calculator and performance analyzer for the Distance Medley Relay (DMR) in track and field. Built as a single HTML file — no installation, no dependencies, no internet connection required after the page loads.

**[View Live →]([https://yourusername.github.io/your-repo-name](https://doherty-enterprises.github.io/Medley-Relay-Split-Calculator/))**
https://doherty-enterprises.github.io/Medley-Relay-Split-Calculator/

---

## What It Does

The DMR consists of four legs run in a fixed order: **1200m → 400m → 800m → 1600m**. Coaching a relay means answering two questions:

1. *Given a target finish time, what does each runner need to split?*
2. *After a race, how evenly did the team actually work?*

This tool answers both.

---

## The Math

Most pace calculators use the Riegel fatigue formula, which breaks down badly across the DMR's range — the 400m is a near-anaerobic sprint while the 1600m is an aerobic endurance event. Treating them the same way produces splits that are wildly off.

This calculator uses a **world record pace ratio model** instead. Equal effort is defined as every runner performing at the same percentage of the world record for their specific event. The formula is simple:

```
split = k × WR_for_that_event
k = target_time / sum_of_all_four_WRs
```

At k = 1.0, you're running every leg at world record pace. At k = 1.25, every runner is working at 80% of their event's world record — equal physiological effort regardless of distance.

Reference world records used (in seconds):

| Event | Men | Women |
|-------|-----|-------|
| 400m  | 43.03 | 47.60 |
| 800m  | 100.91 | 113.28 |
| 1200m | 163.0 | 181.0 |
| 1600m | 221.8 | 246.2 |

*Note: No official IAAF world record exists for 1600m. The reference values are mathematically derived by scaling the mile world record down to 1600m.*

This model was reviewed and validated by coaches, who confirmed the splits are accurate.

---

## Features

### Calculate Mode
- **Target time input** with Men / Women / Mixed gender selection
- **Runner names** — label each leg; names appear on cards and in copied text
- **Runner weighting** — adjust each leg ±20% and let the others absorb the difference, so the total always hits your target
- **Lock specific splits** — pin one or more legs to a fixed time; remaining legs redistribute automatically
- **PR reality check** — enter each runner's personal record to see how aggressive their assignment is
- **Split range bands** — ±5% floor and ceiling shown on each leg card
- **Custom benchmarks** — save named reference times (school record, conference record, etc.) and see where your target ranks
- **Calculation history** — last 8 calculations saved locally; click any entry to reload it
- **Copy splits** — one-click clipboard copy formatted for sharing with coaches or in a team chat
- **Cumulative exchange clock** — running total at each handoff point

### Analyze Mode
- Enter the actual splits from a completed race to see:
  - Each runner's effort as a percentage of their event's world record
  - Who had the hardest and easiest assignments
  - How each leg compares to what an equal-effort lineup would have run
  - An overall team balance rating and written summary

### Display
- Speed in m/s, km/h, or mph
- Pace per lap, per km, or per mile
- Light and dark mode with persistent preference

---

## Usage

Download `index.html` and open it in any modern browser. No server required.

Or visit the live version linked above.

---

## Built With

- Vanilla HTML, CSS, and JavaScript — no frameworks or build tools
- [Barlow Condensed](https://fonts.google.com/specimen/Barlow+Condensed) and [Share Tech Mono](https://fonts.google.com/specimen/Share+Tech+Mono) via Google Fonts
