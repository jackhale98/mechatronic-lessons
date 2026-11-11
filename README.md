# Mechatronic Lessons

An interactive refresher course on electromechanical systems, written for mechanical engineers who want to get back up to speed on the electrical, sensing and control side of mechatronics.

The whole course is a single static page (`docs/index.html`) with no build step and no dependencies beyond Google Fonts. It works on desktop and mobile.

**Live site:** https://jackhale98.github.io/mechatronic-lessons/ (after GitHub Pages is enabled, see below)

## What's inside

18 modules in 9 parts. Every module has a theory section, a "Key relations" table, at least one interactive lab, and a short quiz.

| Part | Modules |
| --- | --- |
| I · Mechanics refresher | 01 Rotational dynamics & power |
| II · Electronics | 02 Circuit fundamentals · 03 Capacitors, inductors & filters · 04 Diodes, transistors & H-bridges · 05 PWM & power electronics |
| III · Embedded & signals | 06 Microcontrollers, ADCs & sampling |
| IV · Sensors | 07 Encoders, strain bridges & more |
| V · Actuators | 08 The DC motor model · 09 Brushless, steppers & servos |
| VI · Power transmission | 10 Gears, belts & screws (ratios and inertia) |
| VII · Modeling & control | 11 System models & step response · 12 Feedback & PID · 13 Frequency response & cascaded loops |
| VIII · Integration | 14 Power, wiring & safety · 15 Motion profiles & motor sizing |
| IX · Machine elements | 16 Shafts, keys & couplings · 17 Bearings & linear guides · 18 Screws, belts & gear strength |

Also included:

- **Formula sheet**: every module's key equations on one page.
- **Bench projects**: seven hands-on exercises using a gearmotor with an encoder, an H-bridge driver and a dev board.

Labs include a flywheel spin-up, a loaded voltage divider, an RC filter scope, coil flyback, an interactive H-bridge, PWM current ripple, sampling and aliasing, an animated quadrature encoder, a DC motor torque–speed explorer, BLDC commutation, gear-ratio optimization, second-order step response with poles, a PID position loop, Bode/phase-margin loop shaping, wire-drop and regeneration calculators, index-table motor sizing, a Goodman-diagram shaft fatigue check, bearing and linear-guide life, and screw, belt and gear calculators.

Quiz answers and "module complete" marks are stored in the browser's `localStorage`, so progress stays on the device you use.

## Viewing locally

Open `docs/index.html` in any modern browser. No server is required.

## Deploying with GitHub Pages

The workflow in `.github/workflows/pages.yml` publishes the `docs/` folder whenever it changes on `main`.

1. In the repository, go to **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **GitHub Actions**.
3. Merge to `main` (or run the workflow manually from the **Actions** tab).

If you'd rather not use Actions, choose **Deploy from a branch** instead, with branch `main` and folder `/docs`. Either option serves the same file.

## Repository layout

```
docs/
  index.html        # the entire course: content, styles, labs and quizzes
  .nojekyll         # serve files as-is, skip Jekyll processing
.github/workflows/
  pages.yml         # GitHub Pages deployment
```

## Notes on the engineering content

Formulas follow standard references (Shigley's *Mechanical Engineering Design* for fatigue, shafts, bearings, screws and gears; common servo and motor-control practice elsewhere). Calculators are first-pass design aids. Check final designs against manufacturer data and the full methods (for example AGMA for gears and the bearing maker's life calculator).
