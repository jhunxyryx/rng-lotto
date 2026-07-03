# RNG Pro - Live Benchmark & Match Simulator

A lottery number generator with three integrated tools:

## Features

### 1. RNG Pro (Single Generator)
- **Lotto Presets**: Quick-select for 6/42, 6/45, 6/49, 6/55, 6/58 games
- **Configurable Parameters**: Max number (A1) and half-count (A2) for total numbers
- **Advanced Constraints**:
  - Force balanced odd/even (50/50)
  - Force balanced low/high (50/50)
  - Prevent consecutive numbers
  - Allow duplicate numbers
- **Entropy Collection**: Draw/swipe on canvas to gather finger entropy (SHA-256 seeded PRNG)
- **Three RNG Modes**:
  - Math.random()
  - Crypto.getRandomValues() (secure)
  - Finger entropy (SHA-256 → Mulberry32 PRNG)
- **Statistics Display**: Odd/even split, low/high split, retry count

### 2. Live Benchmark (Stress Test)
- **Configurable Iterations**: 500 to 10,000 runs
- **Real-time Progress**: Custom progress bar with live stats
- **Metrics Tracked**: Total time, avg/max retries, total candidate draws
- **Analytics Dashboard**:
  - Hot numbers (most drawn)
  - Cold numbers (least drawn)
  - Overdue numbers (longest gap since last draw)
- **Interactive Charts** (Chart.js):
  - Averages Distribution (line chart): All candidate averages vs accepted target region
  - Digit Frequency (bar chart): Per-number hit counts
- **Light/Dark Theme**: Charts auto-update on theme toggle

### 3. Lottery Match Simulator (Gamification)
- **Target Ticket**: Locks in numbers from RNG Pro panel
- **Ticket Wallet**: Store up to 5 tickets for multi-ticket simulation
- **Simulation Speeds**: Fast (500), Turbo (2,500), Hyper (10,000 draws/frame)
- **Match Tiers & Payouts**:
  - 3/6 = $5
  - 4/6 = $100
  - 5/6 = $2,000
  - 6/6 = $10,000,000 (JACKPOT - stops simulation + confetti + audio)
- **Live Stats**: Draws run, spent, won, time elapsed (years), net profit/ROI
- **Retro Terminal Log**: Color-coded match events with audio feedback
- **Theoretical Odds**: Calculated combinations (n choose k)

## Technical Stack
- **Vanilla HTML/CSS/JS** - Single file, no build step
- **Chart.js** (CDN) for distribution visualizations
- **Web Crypto API** for secure randomness and SHA-256 hashing
- **Web Audio API** for synthesized sound effects (no external audio files)
- **CSS Custom Properties** for light/dark theming
- **Mulberry32** seeded PRNG for reproducible entropy-based generation

## Usage
Open `index.html` in any modern browser. No server required.

## Project Structure
```
lotto rng v1/
├── index.html    # Complete application (HTML + CSS + JS)
└── README.md     # This file
```