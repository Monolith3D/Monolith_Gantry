# Monolith 3030 Sheet Metal Gantry

## Rat Rig V-Core 3.1 Modification

This user mod adapts the **Monolith gantry system** for use with a **Rat Rig V-Core 3.1** using a 3030-based sheet-metal gantry arrangement.

The current design is being developed around a **V-Core 3.1 500**, but there should be no major obstacle to adapting the design to other V-Core 3.1 sizes by adjusting the extrusion, rail, and belt lengths as required.

Most of the assembly and hardware remain based on the **standard Monolith BOM**. This repository primarily contains the parts and dimensional changes required to adapt Monolith to the V-Core 3.1 frame.

## Current Status

- **Current printer:** Rat Rig V-Core 3.1 500
- **Drive configuration:** AWD
- **Current gantry variant:** Standard Monolith rail arrangement
- **Development status:** Work in progress

The current release is designed around an **AWD Monolith configuration**.

A **2WD version is planned** and will be adapted in a future revision.

---

## Planned Variants

The project is intended to support several different Monolith/V-Core 3.1 configurations.

### Variant 1 — Standard Monolith

Standard Monolith Y-rail placement with the standard forward-mounted X rail.

**Status:** Current development configuration

### Variant 2 — Stock VC3.1 Y Rails / Top-Mounted X

Uses the **stock V-Core 3.1 Y-rail placement** with a **top-mounted X rail**.

**Status:** Planned

### Variant 3 — Stock VC3.1 Y Rails / Forward-Mounted X

Uses the **stock V-Core 3.1 Y-rail placement** with a **forward-mounted X rail**.

**Status:** Planned

### Variant 4 — Standard Monolith Y Rails / Top-Mounted X

Uses the **standard Monolith Y-rail placement** with a **top-mounted X rail**.

**Status:** Planned

---

# VC3.1 500 Dimensions

## Forward-Mounted X / Inner-Mounted Y

This is the current standard Monolith-style configuration.

| Component | Length |
|---|---:|
| X beam | 594 mm |
| X linear rail | 570 mm |
| Y linear rails | 550 mm — stock VC3.1 |
| Rear extrusion length | 510 mm |

## Top-Mounted X / Stock Y Placement

| Component | Length |
|---|---:|
| X beam | TBD |
| X linear rail | TBD |
| Y linear rails | 550 mm — stock VC3.1 |
| Rear extrusion length | 510 mm |

Additional dimensions will be added as the alternate variants are completed and verified.

---

# BOM

Most hardware remains standard Monolith. The following lists the hardware currently identified for the **3030 V-Core 3.1 conversion**.

## 9 mm Belt Configuration

### Belting

| Qty | Part |
|---:|---|
| TBD | 9 mm GT2 belt |

Final belt length will be added after the belt path is finalized.

### Bearings, Pins, and Spacers

| Qty | Part |
|---:|---|
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
|---:|---|
| 4 | GT2 20T 9 mm pulley |
| 4 | GT2 20T 9 mm pulley, de-hubbed |

### Set Screws and Nuts

| Qty | Part |
|---:|---|
| 8 | M4 × 2.5 set screw |
| 4 | M3 hex nut |

### M3 Hardware

| Qty | Part |
|---:|---|
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
|---:|---|
| 6 | M5 2020 T-nut |
| 8 | M5 washer |
| 6 | M5 × 8 BHCS |
| 2 | M5 × 30 BHCS |

### M6 / 3030 Hardware

| Qty | Part |
|---:|---|
| 16 | M6 3030 T-nut |
| 16 | M6 washer |
| 16 | M6 × 10 BHCS |

---

## 10 mm Belt Configuration

A 10 mm belt configuration is also planned.

### Belting

| Qty | Part |
|---:|---|
| TBD | 10 mm GT2 belt |

Additional pulley, bearing, spacer, and hardware requirements will be documented once the 10 mm configuration has been finalized and tested.

---

# Compatibility

Currently designed around:

- Rat Rig V-Core 3.1
- 500 mm VC3.1 frame
- Monolith gantry
- AWD
- 3030 extrusion
- 9 mm GT2 belts

Other V-Core 3.1 sizes should be adaptable by changing the appropriate extrusion, linear-rail, and belt lengths.

## Future Compatibility

Planned development includes:

- 2WD
- 10 mm belts
- Stock VC3.1 Y-rail placement
- Standard Monolith Y-rail placement
- Top-mounted X rail
- Forward-mounted X rail
- Additional VC3.1 frame sizes

---

# Assembly

Unless otherwise noted, assembly follows the **standard Monolith assembly procedure and BOM**.

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

Dimensions, hardware quantities, and CAD may change as additional configurations are built and tested.

Parts marked **TBD** have not yet been finalized and should not be treated as manufacturing dimensions.

If you build or adapt this mod for another V-Core 3.1 size, contributions, measurements, and feedback are welcome.
