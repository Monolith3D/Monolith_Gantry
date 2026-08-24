# Monolith 3030 Sheet Metal Gantry

## Rat Rig V-Core 3.1 Modification

This user mod adapts the **Monolith gantry system** for use with a **Rat Rig V-Core 3.1** using a 3030-based sheet-metal gantry arrangement.

The current design is being developed around a **V-Core 3.1 500**, but other V-Core 3.1 sizes should be adaptable by changing the required extrusion, linear-rail, and belt lengths.

Most assembly procedures and hardware remain based on the standard Monolith BOM. This repository primarily contains the parts, dimensions, and hardware changes required to adapt Monolith to the V-Core 3.1 frame, along with additional information gathered during development.

For current development notes, reference information, and questions, see the dedicated Discord discussion:

💬 [Monolith V-Core 3.1 User Mod Development Thread](https://discord.com/channels/1227971059764953230/1537888786921427094)

---

## Current Status

- **Current printer:** Rat Rig V-Core 3.1 500
- **Drive configuration:** AWD
- **Gantry configuration:** Standard Monolith rail arrangement
- **X beam:** 594 mm
- **X linear rail:** 570 mm
- **Y linear rails:** 550 mm — stock VC3.1
- **Development status:** Work in progress

The current release is designed around an **AWD Monolith configuration**.

A 2WD version may be adapted in a future revision.

No single toolhead has been selected as the required configuration. One of the goals of the project is to support multiple compatible toolhead and tool-changing options where practical.

---

# Design Direction

After spending considerably more time in CAD and experimenting with several different rail arrangements, the **standard Monolith rail configuration has proven to be the most practical and optimal solution for the V-Core 3.1**.

Several alternatives were investigated, including:

- Stock V-Core 3.1 Y-rail locations
- Top-mounted Y rails
- Bottom-mounted Y rails
- Mixed top/bottom Y-rail arrangements
- Top-mounted X rail
- Forward-mounted X rail

While some of these arrangements are technically possible, the required offsets, clearance compromises, loss of usable travel, increased complexity, and additional custom geometry outweigh their advantages.

In particular, a **top-mounted X rail is not a practical solution for this conversion** without introducing compromises that defeat much of the purpose of using Monolith in the first place.

Because of this, development will now focus solely on the **standard Monolith rail arrangement** rather than maintaining multiple substantially different gantry variants.

### Going forward, development will focus on:

- Standard Monolith rail geometry
- Different belt widths and belt configurations
- AWD
- Potential 2WD adaptation
- Multiple toolhead options
- Tool changer compatibility
- Additional V-Core 3.1 frame sizes where practical

The goal is to refine one solid Monolith-based architecture rather than divide development between several compromised rail configurations.

---

# X Travel

One unavoidable difference between the stock V-Core 3.1 gantry and the Monolith 3030 conversion is the available X-axis travel.

For the **V-Core 3.1 500**:

| Configuration | X Linear Rail | Approximate X Travel |
| --- | ---: | ---: |
| Stock V-Core 3.1 | 600 mm | ~500–520 mm |
| Monolith 3030 | 570 mm | ~470 mm conservative |

The Monolith conversion therefore sacrifices approximately **30–50 mm of total X travel**, depending on the exact stock configuration and toolhead geometry.

The current **~470 mm** figure should be considered a conservative design target rather than an absolute mechanical limit.

Actual usable travel may vary slightly depending on:

- Toolhead
- X carriage
- Endstop arrangement
- Probe placement
- Tool changer hardware
- Belt attachment geometry
- Required frame and enclosure clearances

For most applications, the reduction in X travel is considered an acceptable tradeoff for maintaining the standard Monolith geometry and its associated simplicity, belt routing, rigidity, and performance.

Toolhead-specific travel information will be documented as configurations are tested.

---

# VC3.1 500 Dimensions

## Standard Monolith Configuration

This is the supported and actively developed configuration.

| Component | Length |
| --- | ---: |
| X beam | 594 mm |
| X linear rail | 570 mm |
| Y linear rails | 550 mm — stock VC3.1 |
| Rear extrusion | 510 mm |
| Expected X travel | ~470 mm conservative |

Additional dimensions will be added as the design is finalized and verified.

---

# BOM

Most hardware remains standard Monolith.

The following lists the hardware currently identified for the **3030 V-Core 3.1 conversion**.

## 9 mm Belt Configuration

### Belting

| Qty | Part |
| ---: | --- |
| TBD | 9 mm GT2 belt |

Final belt lengths will be added after the belt path and tensioning requirements have been finalized.

### Bearings, Pins, and Spacers

| Qty | Part |
| ---: | --- |
| 6 | 695 bearing |
| 24 | F695 flanged bearing |
| 2 | 0.2 mm shim |
| 22 | 0.5 mm shim |
| 14 | 1 mm shim |
| 6 | D5 × 40 smooth pin |
| 4 | D5 × 5 compression spring |
| 4 | M3 × D5 × 30 round standoff |
| 14 | M3 × D6 × 30 spacer |
| 2 | M5 × D10 × 5 shaft collar |
| 16 | M5 × D8 × 5 spacer |

### Pulleys

| Qty | Part |
| ---: | --- |
| 4 | GT2 20T 9 mm pulley |
| 4 | GT2 20T 9 mm pulley, de-hubbed |

### Set Screws and Nuts

| Qty | Part |
| ---: | --- |
| 8 | M4 × 2.5 set screw |
| 4 | M3 hex nut |

### M3 Hardware

| Qty | Part |
| ---: | --- |
| 24 | M3 washer |
| 8 | M3 × 4 BHCS |
| 20 | M3 × 6 BHCS |
| 6 | M3 × 6 FHCS |
| 6 | M3 × 8 BHCS |
| 2 | M3 × 8 FHCS |
| 4 | M3 × 40 BHCS |
| 14 | M3 × 45 BHCS |

### M5 Hardware

| Qty | Part |
| ---: | --- |
| 6 | M5 2020 T-nut |
| 8 | M5 washer |
| 6 | M5 × 8 BHCS |
| 2 | M5 × 30 BHCS |

### M6 / 3030 Specific Hardware

| Qty | Part |
| ---: | --- |
| 16 | M6 3030 T-nut |
| 16 | M6 washer |
| 16 | M6 × 10 BHCS |

---

## 10 mm Belt Configuration

A **10 mm belt configuration** is also planned.

### Belting

| Qty | Part |
| ---: | --- |
| TBD | 10 mm GT2 belt |

Additional pulley, bearing, spacer, and hardware requirements will be documented once the 10 mm configuration has been finalized and tested.

---

# Toolhead Compatibility

The 3030 Monolith conversion is not intended to be locked to a single toolhead.

Development will include evaluation and documentation of compatible toolhead configurations as they are modeled and tested.

Because toolhead geometry directly affects available travel, each supported configuration may have slightly different:

- Maximum X travel
- Maximum Y travel
- Probe clearance
- Endstop position
- Belt attachment position
- Frame clearance
- Docking clearance

Where possible, toolhead-specific travel limits and required parts will be documented separately.

---

# Tool Changer Compatibility

Tool changer compatibility is an active area of development.

The standard Monolith rail arrangement provides the most sensible foundation for investigating tool changing without creating separate gantry architectures for each configuration.

Future development may include:

- Tool docks
- Toolhead-specific carriages
- Dock mounting solutions
- Umbilical management
- CAN toolhead support
- Parking clearance
- Automatic tool changing
- Toolhead-specific travel limits

Tool changer support should currently be considered **experimental until individual configurations have been physically tested**.

---

# Compatibility

Currently designed around:

- Rat Rig V-Core 3.1
- 500 mm VC3.1 frame
- Standard Monolith gantry geometry
- AWD
- 3030 extrusion
- 9 mm GT2 belts
- 570 mm X linear rail
- 550 mm Y linear rails

Other V-Core 3.1 sizes should be adaptable by changing the appropriate extrusion, linear-rail, and belt lengths.

## Planned Development

Current development priorities include:

- 10 mm belts
- Additional belt configurations
- Additional toolhead options
- Tool changer compatibility
- 2WD adaptation
- Additional V-Core 3.1 frame sizes
- Verified travel measurements
- Final belt lengths
- Assembly documentation

Alternate top/bottom Y-rail arrangements and top-mounted X-rail configurations are **not currently planned for further development**.

---

# Assembly

Unless otherwise noted, assembly follows the standard Monolith assembly procedure and BOM.

Only components or assembly steps that differ from standard Monolith will be documented here.

Builders should verify:

- Belt alignment
- Pulley and bearing spacing
- Linear-rail alignment
- X/Y squareness
- Gantry clearance
- Toolhead clearance
- Endstop location
- Full X/Y travel

before operating the printer at high acceleration or speed.

---

# Notes

This project is under active development.

Dimensions, hardware quantities, belt lengths, and CAD may change as the design is built and tested.

Parts marked **TBD** have not yet been finalized and should not be treated as manufacturing dimensions.

The **~470 mm X travel figure is currently a conservative estimate** for the V-Core 3.1 500 Monolith configuration. Final usable travel will depend partially on the selected toolhead and associated hardware.

If you build or adapt this mod for another V-Core 3.1 size, contributions, measurements, testing, and feedback are welcome.

Find me everywhere — literally — on Discord:

**WolfKnifeLaserBacon**

---

## Special Thanks

Special thanks to the [**Monolith community**](https://discord.gg/monolith3d) on Discord and to **CloakedWayne** for the development of the **Monolith gantry** — the de facto solution for speed, simplicity, and quality.

Additional thanks to:

- **Maurice** — Testing and confirmations
- **[your name here / USERNAME]** — [CONTRIBUTION]

The 3030 Monolith would not be where it is today without the ideas, feedback, testing, and support contributed along the way.

Thank you to everyone who helped turn the concept into a finished design.

---

## Support Me

**NOT required, but very much appreciated!!**

If you'd like to support my work and future development, you can do so through Ko-fi:

[Support me on Ko-fi](https://ko-fi.com/wolfknifelaserbacon)

Every bit of support helps with continued development, prototyping, testing, and future projects.

Thank you!