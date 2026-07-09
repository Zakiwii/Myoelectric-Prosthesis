# EMG Myoelectric Prosthesis

A myoelectric wrist/hand prosthesis controlled by EMG (electromyography) signals, developed as a Master's thesis (PFE) project at USTHB (Université des Sciences et de la Technologie Houari Boumediene), Algiers.

> 🎓 Defended with highest honors (*mention très bien*).

![Prototype](media/photo.jpg)
<!-- Replace the line above with your own image path once uploaded, or add more images below -->

## Overview

This project implements a low-cost, functional prosthetic wrist that translates forearm EMG muscle signals into automated wrist movements via a servo-driven mechanism. The goal was to build an accessible, reproducible design using widely available components rather than expensive commercial EMG modules.

## How It Works

1. An EMG sensor module picks up electrical activity from the forearm muscles (bipolar signal, powered by a symmetric ±9V supply).
2. The raw signal is conditioned and thresholded to detect muscle contraction events.
3. A Digispark ATtiny85 microcontroller reads the processed signal and generates a manual PWM control signal.
4. An MG996R servo motor executes the corresponding wrist movement.
5. Power is regulated through an LM2596 buck converter for stable operation.

## Hardware

- **Microcontroller:** Digispark ATtiny85
- **EMG sensing:** EMG module (MyoWare-style), symmetric ±9V supply
- **Actuation:** MG996R servo motor
- **Power regulation:** LM2596 buck converter
- **PCB:** Custom-designed in KiCad (schematic capture, DRC, ground planes, Gerber export)
- **Enclosure:** 3D-modeled in Fusion 360, 3D-printed

## Repository Structure

```
prothese-emg/
├── hardware/
│   ├── kicad/          # Schematic, PCB layout, Gerber files
│   └── enclosure/      # Fusion 360 / STEP / STL files
├── firmware/
│   └── attiny85/        # C/C++ firmware for the ATtiny85
├── docs/
│   ├── thesis.pdf        # Full thesis document (French)
│   └── diagrams/         # System architecture diagrams
└── media/
    └── photos, demo video
```

## Firmware

Written in C/C++ for the ATtiny85 (Digispark board), including manual PWM generation for servo control and EMG signal threshold calibration logic.

## Skills & Tools Used

`KiCad` · `Fusion 360` · `Arduino IDE / Micronucleus` · `C/C++` · `EMG signal processing` · `PCB design (DRC, Gerber export)`

## Author

**Senouci Abderraouf Zaki** — M2 Electronics and Embedded Systems, USTHB.
