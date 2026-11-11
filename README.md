# Mechatronic Lessons

An interactive course on electromechanical systems and robotics, covering mechanics, electronics, sensing, actuators, mechanisms, control and estimation, machine-element and precision design, robot manipulators and robot mechanisms.

The whole course is a single static page (`docs/index.html`) with no build step and no dependencies beyond Google Fonts. It works on desktop and mobile.

**Live site:** https://jackhale98.github.io/mechatronic-lessons/ (after GitHub Pages is enabled, see below)

## What's inside

36 modules in 11 parts. Every module has a theory section, a "Key relations" table, at least one interactive lab, and a short quiz. Key results are derived step by step in fold-out sections.

| Part | Modules |
| --- | --- |
| I · Mechanics fundamentals | 01 Rotational dynamics & power |
| II · Electronics | 02 Circuit fundamentals · 03 Capacitors, inductors & filters · 04 Diodes, transistors & H-bridges · 05 PWM & power electronics |
| III · Embedded & signals | 06 Microcontrollers, ADCs & sampling |
| IV · Sensors | 07 Sensors: encoders, bridges & more |
| V · Actuators | 08 Magnetics & electromagnetic actuators · 09 The DC motor model · 10 Brushless, steppers & servos |
| VI · Power transmission | 11 Gears, belts & screws · 12 Linkages · 13 Cams |
| VII · Modeling & control | 14 System models & step response · 15 Feedback & PID · 16 Frequency response & cascaded loops · 17 State space, observers & Kalman filters · 18 Resonance & vibration suppression · 19 Friction & nonlinearities · 20 System identification & testing |
| VIII · Integration | 21 Power, wiring & safety · 22 Motion profiles & motor sizing |
| IX · Machine elements | 23 Shafts, keys & couplings · 24 Bearings & linear guides · 25 Screws, belts & gear strength · 26 Precision design & error budgets |
| X · Robot manipulators | 27 Rigid-body motion · 28 Forward kinematics · 29 Jacobians & singularities · 30 Inverse kinematics & trajectories · 31 Manipulator dynamics · 32 Robot control |
| XI · Robot mechanisms | 33 Cable & tendon transmissions · 34 Series-elastic & compliant actuation · 35 Teleoperation & haptics · 36 Parallel mechanisms |

Also included:

- **Formula sheet**: every module's key equations on one page.
- **Bench projects**: seven hands-on exercises using a gearmotor with an encoder, an H-bridge driver and a dev board.

Labs include a flywheel spin-up, a loaded voltage divider, an RC filter scope, coil flyback, an interactive H-bridge, PWM current ripple, sampling and aliasing, an animated quadrature encoder, a DC motor torque–speed explorer, BLDC commutation, gear-ratio optimization, second-order step response with poles, a PID position loop, Bode/phase-margin loop shaping, wire-drop and regeneration calculators, index-table motor sizing, a Goodman-diagram shaft fatigue check, bearing and linear-guide life, screw, belt and gear calculators, a 3D orientation explorer, planar-arm kinematics with a manipulability ellipse, draggable inverse kinematics, a 2-link dynamics simulation, model-based tracking control, impedance control against a wall, cable-routing friction, actuator impedance, delayed bilateral teleoperation, a draggable five-bar parallel mechanism, solenoid and voice-coil force, IMU tilt estimation with a Kalman filter, input shaping and notch filters, stick-slip and PI hunting, stepped-sine frequency-response measurement, least-squares parameter fitting, an error budget, a four-bar explorer with coupler curves, and cam motion-law and sizing tools.

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

Formulas follow standard references (Shigley's *Mechanical Engineering Design* for fatigue, shafts, bearings, screws and gears; standard robotics texts for kinematics, dynamics and control; common servo and motor-control practice elsewhere). Calculators are first-pass design aids. Check final designs against manufacturer data and the full methods (for example AGMA for gears and the bearing maker's life calculator).
