# Qlubi Face Lithophane Guide

The face of Qlubi is created using a 3D printed lithophane panel. This panel displays an image chosen by the user and is illuminated from behind by Qlubi’s internal lighting system.

This guide explains how to generate the lithophane file and prepare it for printing and assembly. One can also use the premade STL models in this folder and skip to step 4.

---

## Creating the Lithophane

Qlubi uses a lithophane generated using the following tool:

👉 https://www.lithophanemaker.com/Night%20Light%20Lithophane.html

---

## Step 1 — Enter the Required Settings

Enter the following settings exactly as listed below before uploading your image. This ensures you understand the size and shape limitations your image must fit within.

- Lithophane resolution: **0.25 mm/pixel**
- Maximum thickness: **2 mm**
- Minimum thickness: **0.5 mm**
- Frame width: **0 mm**
- Slot width: **10 mm**
- Slot depth: **10 mm**
- Adapter thickness: **2 mm**
- Light-to-lithophane distance: **30 mm**
- Radius of curvature / flatness: **67.5 mm**
- Night light width: **64 mm**
- Night light height: **64 mm**
- 
![Lithophane measurements and site](https://github.com/makser-cisial/Qlubi-light-pal/blob/main/designs/face/images/Lithophane%20face%20measurements.jpg)

---

## Step 2 — Upload and Adjust Your Image

1. Upload an image of your choice.
2. Adjust your image cropping and scaling so that the important parts of the image fit well within the defined square lithophane area.

Users may use any image they like whoever simple, black and white images on a plain background are ideal for a clear uncluttered face. It is also ideal to centre one's image an not have details too close to the edges to ensure they are not obscured by the lip of the casing.

---

## Important Notes

- Do **not change any settings** listed above.
- The only setting that may be adjusted is **Lithophane resolution** if:
  - Your printer is capable of higher detail printing.
  - You want a higher resolution image result.

Changing other settings will cause the lithophane to not fit the Qlubi enclosure correctly.

---

## Step 3 — Download the Lithophane

Once all settings are entered and your image is positioned correctly:

1. Generate the lithophane.
2. Download the generated STL file.

---

## Step 4 — Preparing the Lithophane for Qlubi

Qlubi requires the lithophane to be combined with an inverse face cut file before printing.

### Process

1. Import your downloaded lithophane STL into your slicer.
2. Import the **Inverse Face Cut** file provided in this repository.
3. Set the Inverse Face Cut file as a **negative volume**.
4. Position the negative volume according to the **Face Layout for Slicer** reference file.
5. Slice and export the final print file.

![Layout image for comparison](https://github.com/makser-cisial/Qlubi-light-pal/blob/main/designs/face/images/layout%20image.png)


---

## Printing Recommendations

- Print using a light-coloured or white filament for best light diffusion.
- Use a fine layer height such as 0.10mm for best image quality.
- Infill settings only impact base so anywhere from 5% to 15% is ideal
- Ensure consistent extrusion for smooth gradient transitions.

---

## Result

Once printed and installed, the lithophane becomes the illuminated face of Qlubi, allowing each device to have a unique and personal visual identity.

---

## Troubleshooting

If the lithophane does not fit:

- Confirm all dimensions were entered correctly.
- Confirm the inverse face cut file was used.
- Confirm the lithophane was not rescaled in the slicer.

---

