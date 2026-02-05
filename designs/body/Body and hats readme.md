# Qlubi Body Printing Guide

The Qlubi body is fully 3D printed and designed to be easily produced using the files included in this repository. Users may either print the entire body in one print or print individual parts separately to customise colours, materials, or finishes.

---

## Available Files

The repository contains multiple options depending on how you would like to print your Qlubi body.

### Qlubi Full

- `Qlubi full.stl`  
  Contains all body and hat components combined into a single print file. 

---

### Qlubi Body Zip

- `Qlubi body.zip`  
  Contains all Qlubi body components as separate files.  
  This allows users to print body sections individually or in different colours and materials.

---

### Hats Zip

- `Hats.zip`  
  Contains all hat components as separate files.  
  Hats can be printed individually and swapped depending on user preference.

---

## Printing Options

Users have two primary approaches when printing Qlubi.

---

## Option 1 — Print Entire Body at Once

1. Import `Qlubi full.stl` into your slicer.
2. Split the model into objects and orient as relevant as can be seen in image.
3. Enable supports as required.

### Recommended Print Settings

- Infill: **5–15%**
  - Use higher infill for lighter or more translucent materials to reduce light leakage.
  - Use lower infill for darker or more opaque materials.

- Layer Height: **0.16 mm**

- Supports: **Snug supports recommended**

This method is the fastest and simplest way to produce a complete Qlubi enclosure.

---

## Option 2 — Print Parts Separately

Users may unzip the body and hat archives to print components individually.

### Benefits of Printing Parts Separately

- Allows multi-colour printing
- Allows mixing materials
- Enables easier reprinting of damaged or modified parts
- Supports aesthetic customisation and personal styling

### Process

1. Extract `Qlubi body.zip`.
2. Extract `Hats.zip`.
3. Import individual STL files into your slicer.
4. Arrange and print parts according to your chosen colour or material layout.

Recommended print settings remain the same as printing the full body unless specific materials require adjustment.

---

## Material Considerations

- Lighter or translucent filaments may allow more internal light leakage and benefit from higher infill percentages.
- Darker or opaque filaments naturally reduce light leakage.

---

## Assembly

Line up all printed parts and press them together as designed.

Ensure that the springs are correctly placed in position between the base and the upper casing before fully closing the body. Proper spring placement is required for correct button interaction and device function.

![Spring positioning for base](https://github.com/makser-cisial/Qlubi-light-pal/blob/main/designs/body/images/Base%20spring%20positioning.png)

![Spring positioning for casing](https://github.com/makser-cisial/Qlubi-light-pal/blob/main/designs/body/images/Casing%20spring%20positioing%20.png)

---

## Troubleshooting

If parts do not fit correctly:

- Confirm scaling has not been altered in the slicer
- Confirm supports were removed cleanly
- Confirm correct parts were printed for the intended assembly

---

