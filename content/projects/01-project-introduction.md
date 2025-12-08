---
title: "HB_DFab: Bridging the Gap in Custom Manufacturing"
description: "A complete ecosystem for automated carbon fiber bicycle fabrication."
tags: ["Filament Winding", "Process Engineering", "Capstone"]
image: "/images/bike-hero.jpg"
draft: false
---

## The Design Thesis
I am working to **lower the cost of entry** for custom carbon bicycle manufacturing. My goal is to automate the labor-intensive parts of the process using novel methods and machines built entirely in-house.

The industry forces a binary choice: **Custom Metal** (Heavy, limited tuning) or **Custom Carbon** (Extremely expensive). This project proves we don't have to choose.

---

## Technical Sub-Systems
To achieve this, I could not just build a bike. I had to build the factory first. I engineered my own manufacturing equipment and software control logic to make this workflow possible.

{{< cards >}}
  {{< card link="/projects/02-filament-winder-build/" title="The Machine: 3-Axis Winder" image="/images/winder/winder-hero.jpeg" subtitle="Hardware Design & Motion Control" >}}

  {{< card link="/docs/02-winder-engineering/" title="The Code: G-Code Generator" image="/images/code-hero.jpg" subtitle="Algorithm & Pattern Logic" >}}
{{< /cards >}}

---

## Manufacturing Methods
### 1. Automated Filament Winding
I utilize a custom 3-axis winder to produce carbon tubing. This allows me to tune the stiffness and compliance of the frame via code rather than manual layup.

### 2. Trapped Rubber Molding
Moving away from expensive metal molds, I utilize 3D printed tooling (High-Temp PLA) paired with heat-expanding silicone mandrels to consolidate the composite parts under high pressure.

### 3. Hybrid Metal Lugs
By utilizing **Metal Powder Casting** for junctions, I can create complex, custom geometries without the massive tooling costs of traditional monocoque molds.

*Follow the sub-project links above for detailed engineering logs.*