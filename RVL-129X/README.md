A simplified version of the BKM-129X compatible board.

Should be able to be created at $25-30, with the ADG1611 being the most expensive component.

This requires an Arduino Nano v3 loaded with the latest BKM-129X-MCU code from https://github.com/skumlos/bkm-129x-mcu

For more information go to https://immerhax.com/?p=422

You are welcome to clone, produce and sell hardware based on this. Please keep changes and so on open source.

Cool kids give credit where due.

Thanks goes out to Nick Carney and Bob from RetroRGB for rigorious testing!

--------

Compatibility list and tested consoles (including issues):

PVM-9L2
- SNES (US region, CSYNC)
- Mega Drive 2 (EU region, 60 Hz modded with DFO for "true" 60 Hz, CSYNC)
- Master System 1 (EU region, 60 Hz modded with DFO for "true" 60 Hz, CSYNC)
- PC-Engine (White, with THS7374 external RGB amp, CSYNC)

BVM-D14
- Genesis 1 (60 Hz, CSYNC)

BVM-D9
- Nomad (60 Hz, Triple bypass modded, CSYNC)
- SNES (US region, CSYNC)
- Master System (60 Hz, sync issues like original 129X)
- TurboGrafx/PC-Engine (60 Hz, sync issues like original 129X)

---------

Board revision history:

D: Fix THS7374 filter bypass, move to Kicad 5

C: Rearranged some components for nicer layout

B: Added R29, R30, R31 to compensate for overbrightness

A: Changed R9 to 0 Ohm / jumper

---------

Copyright © 2020 Martin Hejnfelt <martin@hejnfelt.com>
This work is free. You can redistribute it and/or modify it under the
terms of the Do What The Fuck You Want To Public License, Version 2,
as published by Sam Hocevar. See the LICENSE file for more details.

