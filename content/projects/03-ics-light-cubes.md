---
title: "ICS Light Cubes"
subtitle: "A modular, reconfigurable lighting ecosystem designed for adaptive environments."
date: 2024-03-21
tags: ["Product Design", "Mechatronics", "CNC", "SLA Printing"]
image: "/images/cubes/cube-hero.jpg" 
presentation: "https://hbdfab.blob.core.windows.net/assets/ICS-Light-Cubes%20(1).pptx"
draft: false
tech_specs:
  - label: "Material"
    value: "Douglas Fir, SLA Resin, PLA"
  - label: "Software"
    value: "Fusion 360, Rhino"
  - label: "Tools"
    value: "3-Axis CNC, Form 3L"
---

## 1. Concept & Ideation
**The Limitations of Static Lighting**
Residential lighting forces a binary choice: high-intensity overhead lighting (stimulation) or fixed ambient lamps (cord-restricted). There was no solution for "migratory" lighting that moves with the user without the friction of cables.

* **Objective:** Create a tangible, battery-free lighting object that transitions from a single task light to a linear array in seconds.
* **Philosophy:** "Tangible Interaction." Eliminating switches in favor of physical docking as the trigger for illumination.

![Concept Sketches](/images/cubes/light-sketches.jpg)
*Initial exploration of form and modularity.*

---

## 2. Prototyping
Defining the scale was critical. The object had to feel substantial enough to be furniture, but light enough to be portable.

{{< portfolio_grid >}}
  {{< project_card link="#" title="Size Comparison" image="/images/cubes/size-comparisons.jpg" >}}        
  {{< project_card link="#" title="Early FDM Prototype" image="/images/cubes/3d-printed-light-prototype.jpg" >}}
{{< /portfolio_grid >}}

---

## 3. System Architecture
### Contact-Based Power Topology
To eliminate cables while maintaining safety, I engineered a contact-based power architecture using the **USB-A Standard (5V)**.

![System Diagram](/images/cubes/cube-internal.jpg)
*5V Power topology and interconnects.*

* **SELV Compliance:** By utilizing 5V DC, the system remains within Safety Extra Low Voltage limits, making the exposed contact pads on the base station "human-safe" to touch.
* **Magnetic Assist:** Embedded Neodymium magnets provide a "self-aligning" force, pulling the cube into the correct docking position to guarantee pin-to-pad alignment without user effort.

---

## 4. Mechanical Design
### The Serviceability Mandate
A core requirement was that the device must be repairable. I refused to use permanent adhesives to seal the electronics inside the wood.

![Serviceability Mandate](/images/cubes/serviceability-mandate.heic)

**The "Fastmount" Inspiration**
I researched architectural panel mounting systems and adapted the geometry of the industrial **Fastmount** friction-clip system for 3D printing. The final design allows the internal electronics core to "snap" into the wooden shell.

![Clip System Detail](/images/cubes/clip-system-wood.jpg)
*Detail of the friction-clip system.*

![Internal Core](/images/cubes/light-internals.jpg)
*The internal electronics core assembly.*

![Tolerance Testing](/images/cubes/fit-testing.jpg)
*Tolerance testing the friction fit of the internal chassis.*

---

## 5. Manufacturing Process
### Hybrid Fabrication Strategy
The aesthetic required the warmth of natural grain, but the mechanics required the precision of engineering plastics.

| Component | Manufacturing Method | Material |
| :--- | :--- | :--- |
| **Housing** | Subtractive (CNC Machining) | Solid Douglas Fir |
| **Diffuser** | Additive (SLA Printing) | Translucent Resin |
| **Chassis** | Additive (FDM Printing) | PETG / PLA+ |

<video width="100%" controls autoplay loop muted playsinline>
    <source src="/images/cubes/cnc-process.jpg.MOV" type="video/mp4">
    <source src="/images/cubes/cnc-process.jpg.MOV" type="video/quicktime">
    Your browser does not support the video tag.
</video>
*The Douglas Fir housing being machined.*

**Failure Analysis & Process Control**
Early manufacturing attempts relied on double-sided machining (flipping the wood stock). This resulted in critical failures due to registration errors. I redesigned the part to utilize a **Single-Setup Through-Bore** to guarantee vertical concentricity.

{{< portfolio_grid >}}
  {{< project_card link="#" title="Grain Fracture Analysis" image="/images/cubes/cube-fail.jpg" >}}       
  {{< project_card link="#" title="SLA Support Failure" image="/images/cubes/failed-sla.jpg" >}}
{{< /portfolio_grid >}}

---

## 6. Final Validation
Testing the human scale of the finished assembly.

![Human Scale](/images/cubes/me-with-light-project.jpg)
*Scale comparison of the finished assembly.*

