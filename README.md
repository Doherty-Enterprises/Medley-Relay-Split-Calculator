Readme · MDCopyMedley Relay Split Calculator
A split calculator and performance analyzer for medley relay events in track and field. Covers the Distance Medley Relay (DMR), Sprint Medley Relay Short (100-100-200-400), and Sprint Medley Relay Long (200-200-400-800). Built as a single self-contained HTML file — no installation, no dependencies, no internet required after the page loads.

View Live → https://doherty-enterprises.github.io/Medley-Relay-Split-Calculator/

Events

EventLegsDMR — Distance Medley Relay1200m · 400m · 800m · 1600mSMR Short — Sprint Medley Relay100m · 100m · 200m · 400mSMR Long — Sprint Medley Relay200m · 200m · 400m · 800m

What It Does

Two modes for each event:
Calculate Splits — Enter a target finish time and get a realistic split for each leg, based on equal physiological effort across all four runners.
Analyze Performance — Enter your team's actual splits from a completed race and see how evenly the workload was distributed, who ran the hardest and easiest legs, and how the team performed relative to world record pace.

The Math

Most pace calculators use the Riegel fatigue formula, which models a single athlete's performance across varying distances. That doesn't apply to relays, where each leg is run by a different person.
This calculator uses a world record pace ratio model instead. Equal effort is defined as every runner performing at the same percentage of the world record for their specific event:
split = k × WR_for_that_event
k = target_time / sum_of_all_four_WRs
At k = 1.0, every runner is at world record pace. At k = 1.25, every runner is at 80% of their event's WR — equal physiological effort regardless of distance or event type.
World Records Used
DistanceMenWomenNote100m9.58s10.49sBolt (2009) / Griffith-Joyner (1988)200m19.19s21.34sBolt (2009) / Griffith-Joyner (1988)400m43.03s47.60svan Niekerk (2016) / Koch (1985)800m1:40.911:53.28Rudisha (2012) / Kratochvílová (1983)1200m2:43.03:01.0Derived via Riegel from 1500m WR*1600m3:41.84:06.2Scaled from mile WR*
*The 1200m and 1600m are not sanctioned World Athletics events. Reference times are mathematically derived from adjacent world records.

Features

Calculate Mode

Target time input with Men / Women / Mixed gender selection
Per-leg gender assignment in Mixed mode — each leg uses the correct gender's WR
Runner names — label each leg; names appear on result cards and in copied text
Runner weighting — adjust each leg ±20%; the other legs absorb the difference so the total always hits your target
Lock specific splits — pin one or more legs to a fixed time; the remaining legs redistribute automatically
PR reality check — enter each runner's personal record to see what percentage of their PR the assigned split requires
Split range bands — ±5% floor and ceiling shown on each leg card
Custom benchmarks — save named reference times and see how your target ranks against them
Calculation history — last 8 calculations saved locally; click any entry to reload it
Copy splits — one-click clipboard copy, formatted for sharing
Cumulative exchange clock — running total at each handoff
Speed and pace display in m/s, km/h, mph, per lap, per km, or per mile

Analyze Mode

Enter actual race splits to see each runner's effort as a percentage of WR pace
Identifies the hardest and easiest legs
Shows how each leg compares to what an equal-effort lineup would have run
Team balance rating and written summary
Equal-effort equivalent total time

Display

Light and dark mode with persistent preference
Per-event calculation history and benchmarks stored separately per event


Usage

Download index.html and open it in any modern browser. No server required.
Or visit the live version linked above.

About

Built by Kyle Doherty, a cross country and track & field runner at El Toro High School. The methodology was reviewed by national-qualifying athletes and coaches before release.
For bugs, suggestions, or questions: kyledoherty281@gmail.com

Built With

Vanilla HTML, CSS, and JavaScript — no frameworks, no build tools
Barlow Condensed and Share Tech Mono via Google Fonts
