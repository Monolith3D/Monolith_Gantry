# Sheet Metal Parts

This folder contains the sheet metal components required for the **3030 Monolith gantry**.

These parts are intended to be sent to a sheet metal fabrication service for cutting and forming before assembly.

---

# Ordering Instructions

## Understanding the File Names

The STEP file names include important information about:

- Required quantity
- Part name
- Acceptable material thickness
- Required finished stack thickness

**Please read the file name carefully before ordering.**

There are two different thickness conventions used in this folder:

1. **Thickness options** — either listed thickness is acceptable.

2. **Specified thickness** — the listed thickness is required to achieve the correct assembled stack height. For parts requiring a **5 mm total thickness**, two **2.5 mm parts may be stacked together**. This is often preferable because the closest commonly available single-sheet option is **4.7 mm**, which does not provide the required stack height, while **2.5 mm material is typically readily available**.

These are not interchangeable.

---

## Quantity Prefix

The quantity shown with each file indicates the **total number of finished parts required**.

For example:

```text
2x
Sheet_metal_9mm_tensioner_c_4.7-5mm.step
```

This means:

- Order **2 pieces**
- Each piece may be made from either **4.7 mm or 5.0 mm material**
- Both thicknesses are acceptable for this component

Different fabrication services offer different standard material thicknesses, so the files allow either option where appropriate.

---

### Combined Spacer Part

The following individual spacer file is required at **4x pieces, 1.5 mm thick each**:

`Sheet_metal_9mm_spacer_c_1.5mm.step`

Because these parts are relatively small, some fabrication services may not be able to manufacture them individually due to minimum part-size requirements.

For that reason, the following combined version is also provided:

`Combined_Sheet_metal_9mm_spacer_c_1.5mm.step`

The combined file joins the required spacers together with small connecting tabs so the assembly can be ordered as one larger part.

After fabrication:

- Cut the individual spacers apart at the connecting tabs.
- File or sand the remaining connection points smooth.
- Remove any burrs before assembly.
- Verify that the finished spacers remain flat.

The combined file is only a **manufacturing convenience** and does not change the required final spacer thickness or quantity.

---

## Questions / Discord

If you have questions about the **3030 Monolith conversion**, sheet metal ordering, assembly, fitment, or current development, you can usually find me on Discord as:

**WolfKnifeLaserBacon**

You can find me in the **[Monolith Discord](https://discord.gg/monolith3d)** or in the dedicated **[3030 Monolith Development Thread](https://discord.com/channels/1227971059764953230/1537888786921427094)**.

I’m happy to help clarify file requirements, ordering details, assembly questions, or anything else that comes up during your build.

**Don’t be shy — your question may prompt an addition to this README and earn you a nice special thanks in the main README!**