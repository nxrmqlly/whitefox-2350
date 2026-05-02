# whitefox :: an RP2350B devboard
> 💥 very chonky!

![whitefox v1 magazine page](assets/whitefox-zine.png)

## What's this? ooh shiny.

whitefox is a Raspberry Pi RP2350B based **devboard** with *47 exposed GPIO, a 3x3 neopixel grid, a charging circuit and a MicroSD card reader* onboard!
Some may even say that it is *batteries included* but sorry we don't include batteries :(

## Why?

I wanted to have a go at making a devboard so I initially thought of using the RP2040 Chip but that thing is old now and very overused so here
we are with the RP2040's successor, the RP2350! Most RP2350 boards (like the Raspberry Pi Pico *2*) use the QFN-60 layout on the RP2350A chip 
and I haven't really seen devboards use the RP2350B, which is a QFN-80 chip, meaning it exposes the full power of the RP2350 in a bigger die.

## The PCB

The Schematic is a combination of very many different projects and the official and amazing
[Hardware design with RP2350](https://pip-assets.raspberrypi.com/categories/1214-rp2350/documents/RP-008280-DS-1-hardware-design-with-rp2350.pdf)
The PCB is configured in a 4 layer stackup as follows (from the top): `SIG / GND / PWR / SIG` and includes copper pours on all layers except
the PWR layer (duh.)
Most components are SMD on top of the board, only the JST connector is through hole.

The PCB exposes two 2x16 standard 2.54 mm pitch header holes on both sides and an additional 1x3 2.54mm pitch connector as a debug header.

| What                                       | Image                                |
|--------------------------------------------|--------------------------------------|
| PCB                                        | ![pcb](./assets/pcb.png)             |
| [Schematic](./Docs/whitefox.pdf) | ![schematic](./assets/schematic.png) |

The PCB and Schematic are available in a high quality PDFs in [Docs/](Docs/)

## 3D stuff
| <center>Front</center>             | <center>Back</center>            |
|------------------------------------|----------------------------------|
| ![3d front](./assets/front_3d.png) | ![3d back](./assets/back_3d.png) |

## The BOM

Lazy to type it here so...

The full BOM can be found at [BOM/bom.csv](./BOM/BOM.csv)!

## Why the name?

> There are 2 hard problems in computer science: cache invalidation, **naming things**, and off-by-1 errors.
>
> *-- Leon Bambrick*

yeah that should be enough for an explanation.

## How to build / use it IRL

1. Spend some \$\$\$ get parts from the [BOM](./BOM/BOM.csv)
2. Use the gerbers from [production/gerbers.zip](production/gerbers.zip) to fabricate a PCB.
3. With some elbow grease and reference from the schematic, get to soldering the tiny SMD components
4. You're done! Go crazy

Alternatively, you can preserve your sanity and [get a PCBA service instead.](https://jlcpcb.com)
1. Gerbers are at [production/gerbers.zip](production/gerbers.zip)
2. JLCPCB BOM (not project bom!!) is at [production/jlc_bom.csv](production/jlc_bom.csv)
3. Pick and Place (CPL) file is at [production/positions.csv](production/positions.csv)

## Credits where credits are due.

Grateful for:
- [euvalennn's RPBoard^2](https://github.com/euvalennn/rpboard-squared) for a lot of design inspiration and schematic help.
- [Fallout by hackclub](https://fallout.hackclub.com/) for giving me the oppourtunity and public brand assets!
- hackclub slack for the coolest people that helped out!

## License

The hardware (PCB) is licensed under `CERN Open Hardware Licence Version 2 - Strongly Reciprocal` which means, you're all-right to copy my work and use it in yours but you must disclose your source code and project files to opensource repositories if you include part of my work in yours. See [LICENSE](LICENSE).
