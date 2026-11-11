# Micro Buster 2.0

MicroburstHunter landing page frontend — *Fifty milliseconds of chaos, caught in twenty.*

A single-page concept landing site for MicroburstHunter, a Computer Networks course project on real-time detection and mitigation of microbursts in data-centre networks.

## What's in here

- `index.html` — the complete landing page (self-contained, no build step). Open it in a browser, or serve it with any static server, e.g. `python3 -m http.server`.

## The story it tells

Calm → a 50 ms burst at 150 Mbps → detection in 20 ms → attribution: 85% to `10.0.0.99` → capped at ~35 Mbps → calm again (kernel: 92.2 → 33.9 Mbps).

## Numbers (verified, from the project)

- Burst: 150 Mbps for 50 ms, offender `10.0.0.99` at 85% share
- Detection: 20 ms (window 2, EWMA α=0.1, threshold 80 Mbps)
- Mitigation: Linux `tc` / HTB cap ~35 Mbps; live kernel 92.2 → 33.9 Mbps
- Detector benchmark: 100/100 detected, 0 false positives in 1,000 windows

## Note

This repo is the **landing page frontend only**. The full console (Overview, Traffic, Topology, Sources, Mitigation, Experiments, Events, Settings) and the Python/Scapy + Linux `tc` backend live in the original project repo, `arshad-88/MICROBUSRTHUNTER` (forked as `Prateek2007-cmd/MICROBUSRTHUNTER`).
