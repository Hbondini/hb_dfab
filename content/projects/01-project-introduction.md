---
title: "Capstone: Carbon Fiber Bicycle"
description: "A complete ecosystem for automated carbon fiber bicycle fabrication."
tags: ["Filament Winding", "Process Engineering", "Capstone"]
image: "/images/capstone/bike-assembly.heic"
draft: false
---

## Design Outline
To create a full vertically integrated manufacturing process for custom carbon fiber bicycles, using a range of digital fabrication techniques.

---

## Technical Sub-Systems
To achieve this, I could not just build a bike. I had to build the factory first. I engineered my own manufacturing equipment and software control logic to make this workflow possible.

{{< cards >}}
  {{< card link="/projects/02-filament-winder-build/" title="The Machine: 3-Axis Winder" image="/images/winder/winder-hero.jpeg" subtitle="Hardware Design & Motion Control" >}}

  {{< card link="/docs/02-winder-engineering/" title="The Code: G-Code Generator" image="/images/winder/winder-code-generator.png" subtitle="Algorithm & Pattern Logic" >}}
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