
# Monolith 3030 Sheet-Metal Gantry

## Rat Rig V-Core 3.1 Usermod

This modification adapts the [Monolith Gantry](https://github.com/Monolith3D/Monolith_Gantry) for the **Rat Rig V-Core 3.1**, using a 3030-based sheet-metal gantry.

The current design is developed around the **V-Core 3.1 500 AWD** and supports both **9 mm and 10 mm GT2 belts**. Support for 2WD is planned for a later release.

💬 [**Development Discussion — Monolith Discord**](https://discord.com/channels/1227971059764953230/1537888786921427094)

## Design and Compatibility

This conversion retains the **standard Monolith X/Y rail positions and gantry geometry**. Alternative rail positions were evaluated but offered no worthwhile advantage.

Development will focus on refining the standard Monolith arrangement rather than introducing alternate rail layouts.

- AWD with 9 mm or 10 mm GT2 belts
- 2WD planned for a later release
- Multiple toolhead and toolchanger options
- Stock V-Core 3.1 550 mm Y rails are compatible
- Approximately 470 mm of conservative X travel on the V-Core 3.1 500
- 3030 extrusion or stainless-steel tube X-beam options

## Dimensions — V-Core 3.1 500

| Component | Original CAD | Documented Build |
|:---|---:|---:|
| X beam | 594 mm | 590 mm |
| X rail (MGN12H) | 570 mm | 565 mm |
| Y rails (MGN12C) | 550 mm | 565 mm |
| Rear extrusion | 508 mm* | 525 mm |

The stock 550 mm Y rails are compatible. For newly purchased rails, **565 mm MGN12C rails** are recommended.

The documented build dimensions are reference measurements from the physical build and may differ from the original CAD.

## Stainless-Steel X Beam

A **590 mm stainless-steel tube with a 1.5 mm wall thickness** is available as an alternative to the 3030 extrusion X beam.

The tube is compatible with both the **9 mm and 10 mm belt configurations**, provided that the pulleys, idlers, belt attachments, spacers, and related hardware match the selected belt width.

Nuts can be pressed directly into the tube, providing mounting points without conventional extrusion T-nuts. Verify nut locations, thread engagement, and hardware against the current CAD before assembly.

Special thanks to **Veylon** for making this option available.

If you are interested in a stainless-steel X beam, please consider purchasing directly from [**Veylon**](https://discord.com/users/352790875560214538) on Discord to support his work.

## BOM and Assembly

The following BOM covers the conversion-specific components for the **V-Core 3.1 500 AWD**. Standard V-Core hardware, electronics, motors, fasteners, and Monolith components should be sourced from the relevant base-build documentation.

### Main Components

| Component | Quantity | Notes |
|:---|---:|:---|
| 3030 X beam or stainless-steel X tube | 1 | 590 mm documented build length |
| MGN12H X rail | 1 | 565 mm documented build length |
| MGN12C Y rails | 2 | 550 mm stock rails compatible; 565 mm recommended for new rails |
| GT2 belt | 2 | 9 mm or 10 mm width; approximately 2.61–2.62 m per belt for the current AWD layout |
| GT2 drive pulleys | 4 | Must match the selected belt width and motor configuration |
| GT2 idlers or tensioners | As required | Must match the selected belt width |
| Monolith sheet-metal gantry plates | 1 set | Use the compatible Monolith AWD configuration |
| 3030 or stainless-steel tube mounting hardware | As required | Match the selected X-beam option |
| Rail mounting hardware | As required | Match the selected rail lengths and mounting pattern |
| Toolhead mounting hardware | As required | Depends on the selected toolhead or toolchanger |

### Bearings, Pins, and Spacers

| Quantity | Part |
|---:|:---|
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

| Quantity | Part |
|---:|:---|
| 4 | GT2 20T, 9 mm pulley |
| 4 | GT2 20T, 9 mm de-hubbed pulley |

### Set Screws and Nuts

| Quantity | Part |
|---:|:---|
| 8 | M4 × 2.5 set screw |
| 4 | M3 hex nut |

### M3 Hardware

| Quantity | Part |
|---:|:---|
| 24 | M3 washer |
| 8 | M3 × 4 BHCS |
| 20 | M3 × 6 BHCS |
| 6 | M3 × 6 FHCS |
| 6 | M3 × 8 BHCS |
| 2 | M3 × 8 FHCS |
| 4 | M3 × 40 BHCS |
| 14 | M3 × 45 BHCS |

### M5 Hardware

| Quantity | Part |
|---:|:---|
| 6 | M5 2020 T-nut |
| 8 | M5 washer |
| 6 | M5 × 8 BHCS |
| 2 | M5 × 30 BHCS |

### M6 and 3030-Specific Hardware

| Quantity | Part |
|---:|:---|
| 16 | M6 3030 T-nut |
| 16 | M6 washer |
| 16 | M6 × 10 BHCS |

The current design supports **9 mm and 10 mm belts**. Select all pulleys, idlers, belt attachments, spacers, and related hardware for the chosen belt width. The pulley list above reflects the current 9 mm AWD configuration. Do not mix 9 mm and 10 mm belt hardware unless the component is specifically designed for both widths.

The stainless-steel tube X beam can be used with either belt width. 2WD is not included in the current BOM and is planned for a later release.

Final belt lengths should be verified during assembly. Before operation, check rail alignment, belt routing, gantry squareness, X-beam mounting, nut engagement, pulley spacing, and toolhead clearances.

## Development Status

**Work in progress.** Dimensions and hardware requirements may change as the design is tested and refined.

The current design supports AWD with either 9 mm or 10 mm belts and can use either a 3030 extrusion or the stainless-steel X tube option.

Future development includes 2WD, additional V-Core sizes, toolhead compatibility, and toolchanger support.

Feedback, testing, and contributions are welcome.

Find me everywhere — literally — on Discord:

**WolfKnifeLaserBacon**

---

## Special Thanks

Special thanks to the [**Monolith community**](https://discord.gg/monolith3d) and **CloakedWayne** for developing the Monolith gantry — the de facto solution for speed, simplicity, and quality.

Additional thanks to:

- **Maurice** — Testing and confirmations
- [**Veylon**](https://discord.com/users/352790875560214538) — Stainless-steel X beam option and community support
- Everyone contributing feedback, ideas, testing, and assistance

This project would not be possible without the work and support of the Monolith community.

## Support Me

Not required, but greatly appreciated!

If you would like to support continued development, prototyping, and testing:

[**Support me on Ko-fi**](https://ko-fi.com/wolfknifelaserbacon)

Thank you!
