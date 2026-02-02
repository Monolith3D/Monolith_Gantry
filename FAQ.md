# FAQ

## Configuration Options

### What does NP and FT mean?
- No Protrusion (NP) means the rear and front motors mounts don't protrude out of the frame perimeter
- Full Travel (FT) means the motor mounts protrude 4mm out of the frame, but it lets you get full travel (check configurator for distances)
- What should I pick?
  - If you want to stick with regular panels and don't need the overtravel, choose NP
  - If you want overtravel, pick FT, you will either need [Monolith Panels](https://github.com/Monolith3D/Monolith_Panels) or 4040 verticals to space out the panels

### How much overtravel is there?
- Stock Voron: +10mm
- Monolith default config (spaced out panels or 4040): +13mm for all versions
- Monolith zero protrusion config (stock frame and panels):
  - VT 2WD: +9mm
  - VT AWD: +5mm
  - V2 2WD: +7mm
  - V2 AWD: +1mm
- X travel and front corner losses with AWD will be toolhead dependent
- To switch between the two configs won't require the reprinting of motor mounts

### Should I choose printed or sheet metal?
- Both have rougly the same performance
- Sheet metal pulls heat away from motors and doesn't melt, letting you run higher motor currents or hotter chambers
- Sheet metal is more work, because of reaming bearing holes, countersinking, and harder assembly
- Sheet metal is also more noisy due to more transfer of vibrations

### What are long-shaft stepper motors?
- For 9mm belts, regular stepper shafts (24mm) aren't long enough to reach the double shear bearing
- For 6mm belts, regular steppers work in crazy ivan mode (up on one side, down on the other)
  - However, this does not work for front motor mounts on the trident because of the leadscrews intersecting with the motors
- Double shear is necessary to tension belts enough without bending the shaft
- Minimum for 9mm is 37mm (S37)
- Minimum for 6mm is 35mm (S35)
- Reccommended motors:
   - OMC 17HS19-2504S-H-V1
   - LDO 42STH48-2504AH (S55)
   - LDO-42STH48-2504AH (S45R) - Monolith edition, with 2M long cables
 
### What Z joints should I use for flying gantries?
- For printed gantries use printed Z joints
- For sheetmetal use hybrid or slm
- Double Z joints are recommended for better rigidity

## Sourcing

### What are live shafts?
- Live shafts rotate with the pulley, instead of idlers rotating around the shaft
- Bearings are mounted in the joint and let the shaft freely rotate
- F695 bearings can handle much higher loads than the small bearings in pulley idlers

### What are dehubbed pulleys, and why are they necessary? 
- Dehubbed pulleys are regular pulleys but with their hub removed, and a new bottom flange inserted
- This is necessary for belts to pass through without rubbing 
<img width="1097" height="511" alt="image" src="https://github.com/user-attachments/assets/0c2dffe4-09ba-4466-a23e-b328fd4f5d03" />

### Why do I need 2.5mm long grub screws?
- These need to be short enough to not rub on belts for dehubbed pulleys
- The max length is 2.7mm
- If you can't find 2.5mm grub screws you can either:
   - File down 3mm grub screws
   - Buy pressfit pulleys
   - Use retaining compound

### Should I use gt3 belts?
- GT3 doesn't signifcantly improve IS results, and requires significantly more tension to match GT2
- If you want to improve on belts, increasing belt width is more beneficial
- [Tests](https://monolith-gantry-updates.zen3d.eu/gt3-vs-gt2-epdm-belt-recommendation/)
- The recommended belts are GT2 EPDM because of temp resistance

### What preload do I need for rails
- Y: Rail Z0 / No Preload
  - Belt tension preloads them, and any extra preload can cause unnecessary wear or binding
- X rail: Z2 / Highest Preload available
  - This is very important for toolhead rigidity

## Printing

### What materials should I use? [^1]
- Use filled filament for 9/10mm belts, and is recommended for 6mm belts
- Unfilled abs can crack/split with high belt tension
- Chamber temp < 65C
  - ABS (don't get filament thats blended or has lots of addatives) 
  - ASA
  - ABS/PC
  - ABS+CF/GF
  - ASA+CF/GF
- Chamber temp < 100C
  - PET+CF/GF (needs to be annealed)
  - PC-PBT-GF/CF (can be annealed for more temp resistance)
  - EZPCCF
  - PCCF (Usually needs 100C chamber temp to print, otherwise it is not good)
- Chamber temp < 150C
  - PPS-CF (needs to be annealed
  - PEKKA-CF
  - PSU
- Chamber temp > 150C
  - PPSU
  - PEI
  - TPI
  - LCP
  - Realistically, you should do sheetmetal

### What print settings should I use?
- 8 walls, 8 top/bottom layers, 40% infill

## Compatability 
### What toolheads can I use?
- Monolith has a flipped belt path, so toolhead designs need to be designed with different belt clamps
   - Many toolheads make use of the [SLM Belt Clamp](https://github.com/Monolith3D/MISC/tree/main/Monolith_SLM_belt_clamps)
- Toolhead designs:
   - [Archetype](https://github.com/Armchair-Heavy-Industries/Archetype), with [Monolith Belt Clamps](https://github.com/Thescarecow/Archetype_Rail_Carriage_Clamp_Mod) (these are for Expiremental branch)
   - [Banantis](https://github.com/jakub874/Banantis)
   - [DK's Monolith Toolhead](https://github.com/Kizime123/DKs-Monolith-Toolhead)
   - [FiberSteam Toolhead](https://github.com/Shamoon78/Angry_Tool_Head/)
   - [FiberStream Toolhead](https://www.printables.com/model/1219174-fiberstream-toolhead)
   - [Gustav Railway Toolhead](https://github.com/RCI-Nicket/Gustav-Railway-Toolhead)
   - [Stormbreaker-Toolhead](https://github.com/Gr33n5murf/Stormbreaker-Toolhead)
   - [Takeoff-Toolhead](https://github.com/Kizime123/Takeoff-Toolhead)
   - [Trinity-Toolhead](https://github.com/WV-design/Trinity-toolhead/)
   - [UAP](https://www.printables.com/model/1353685-uap-v6)
   - [Xol-Toolhead](https://github.com/Armchair-Heavy-Industries/Xol-Toolhead), with [Monolith_Xol-Carriage](https://github.com/Armchair-Heavy-Industries/Armchair-Usermods/tree/main/files/Xol-Toolhead/Monolith_Xol-Carriage)

## Assembly
### How do I assemble the XY joints?
<img width="1099" height="812" alt="image" src="https://github.com/user-attachments/assets/6d975dc8-8fa2-4cc9-8afb-4e36bc1cead4" />

### What brackets should I use for the rear extrusion for Trident?
- In Full Travel (FT) mode, rotate the stock brackets 180 degrees
- In No Protrusion (NP) mode, use regular 2020 brackets

### What are these little tabs/slots for?
 - They are for zipties to route your motor cables

<img width="300" alt="Screenshot 2026-01-29 160532" src="https://github.com/user-attachments/assets/be283dfb-eb03-4698-96d5-42196b98dab0" /> <img width="300" alt="Screenshot 2026-01-29 160635" src="https://github.com/user-attachments/assets/fda1d349-ea72-4637-b222-f2da3d12a523" /> 

## What are these clips for?
- They are spacers for FT mode for flying gantries
- These are also found within Z-joint spacers in case you forget to print them

<img width="300" height="293" alt="Screenshot 2026-01-30 124453" src="https://github.com/user-attachments/assets/f36208f0-3ca5-471a-a4c7-9212b0cbc990" /> <img width="300" height="293" alt="Screenshot 2026-01-30 123742" src="https://github.com/user-attachments/assets/00f594dd-4058-4886-a0e7-bb5863437e76" />

| NP mode | FT mode |
| :---: | :---: |
|  <img width="300" alt="Screenshot 2026-01-30 123721" src="https://github.com/user-attachments/assets/34c86fa5-d8b5-4e11-b064-aebee5f0bfc6" /> | <img width="300" alt="Screenshot 2026-01-30 123708" src="https://github.com/user-attachments/assets/8ab6f6b8-92ed-4f50-8a67-31660c5a70f3" /> |

### How much should I tension my belts?
- [Belt tension Calculator (Lukes Lab)](https://www.lukeslabonline.com/pages/belt-tension-calculator)
- For large builds, the built-in tension range isn't enough, so you can use a pretensioner

## What if I want to use endstops for homing?
- X Endstop: [CAD](CAD/VIII_X_endstop), [STL](STLs/X_endstop_housing.stl)
- Y_endstop: [CAD](CAD/VII_Y_endstop), [STL](STLs/Y_endstop_housing.stl)

## General Questions

### Is a 2020 frame enough?
- For 9mm AWD, upgrading the frame is important for achieving good Input Shaper graphs
- You can either upgrade to 4040 verticals or add [structural panels](https://github.com/Monolith3D/MISC/tree/main/Structural_Side_Panels_V2-VT)
   - The most beneficial sides to add panels on are the left and right, because of Y-axis forces
 -  Differences in rigidity:

| 2020 Frame | Structural Panels except Front |
| :---: | :---: |
| <img src="https://github.com/user-attachments/assets/ad24cb2f-a143-44fe-a2bc-bacabee6dfa0" width="300" /> | <img src="https://github.com/user-attachments/assets/21606be1-958f-4e7f-997b-2631a8e731ca" width="300" /> |

### Why is the belt path flipped?
- The flipped belt is necessary for new idler locations for shorter belt paths
- Reduction of 10-15 cm from stock voron belt path
- Adding AWD doesn't increase belt path, unlike other AWD mods for stock gantry

### Why are the Y-rails on the inside?
- The XY joints are more rigid with the rails facing inside
- Reduces issues caused by bimetallic expansion  
  - The X and Y rails are in the same plane, so no upward bending
 
### Why Front X Rail instead of Top Rail?
- Carriage is closer to belts and closer to the center of mass (COM) of the toolhead
- [More indepth explanation](https://monolith-gantry-updates.zen3d.eu/com-position-top-vs-front-rail/)

### Is there a difference between 2.4 and Trident (Flying vs Fixed Gantry)?
- Trident is more rigid, and has a higher max Input Shaper values
- However, 2.4 can be upgraded to get to near Trident rigidty using:
  - Rigid Z joints 
  - Double Z joints (2 carriages on each Z rail)
- There is roughly a 10-15% increase for Trident for sufficently rigid printers with:
  - 4040 extrusions
  - Structural Panels
  - Double Rigid Z joints for 2.4
  - Com optimized rigid toolhead

**Written by: Renovic**
[^1]: Based on Scarecrow's list
