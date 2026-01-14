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
    value: "Hard Maple, Walnut, SLA Resin"
  - label: "Software"
    value: "Fusion 360, Rhino"
  - label: "Tools"
    value: "3-Axis CNC, Form 3L"
---

## 1. The Design Problem
**The Limitations of Static Lighting**
Residential lighting forces a binary choice: high-intensity overhead lighting (stimulation) or fixed ambient lamps (cord-restricted). There was no solution for "migratory" lighting that moves with the user without the friction of cables.

* **Objective:** Create a tangible, battery-free lighting object that transitions from a single task light to a linear array in seconds.
* **Philosophy:** "Tangible Interaction." Eliminating switches in favor of physical docking as the trigger for illumination.

---

## 2. System Architecture
### Contact-Based Power Topology
To eliminate cables while maintaining safety, I engineered a contact-based power architecture using the **USB-A Standard (5V)**.

![System Diagram](/images/cubes/cube-internal.jpg)
*5v Led Lights*

* **SELV Compliance:** By utilizing 5V DC, the system remains within Safety Extra Low Voltage limits, making the exposed contact pads on the base station "human-safe" to touch.
* **The Interconnect:** I selected **Spring-Loaded Pogo Pins** rated for 10,000 cycles. These provide 2.5mm of vertical travel, absorbing minor planarity variances in the wooden housing to ensure constant electrical contact.
* **Magnetic Assist:** Embedded Neodymium magnets provide a "self-aligning" force, pulling the cube into the correct docking position to guarantee pin-to-pad alignment without user effort.

---

## 3. Mechanical Design
### The Serviceability Mandate
A core requirement was that the device must be repairable. I refused to use permanent adhesives to seal the electronics inside the wood.

![Serviceability Mandate](/images/cubes/serviceability-mandate.heic)

**The "Fastmount" Inspiration**
I researched architectural panel mounting systems and adapted the geometry of the industrial **Fastmount** friction-clip system for 3D printing.

* **The Challenge:** Creating a snap-fit mechanism that holds the assembly under tension but releases with a specific force ($>15N$) for disassembly.
* **The Solution:** I iterated through dozens of 3D printed clip profiles to tune the tolerances. The final design allows the internal electronics core to "snap" into the wooden shell, holding the optical diffuser flush against the Douglas Fir housing.

![Internal Electronics Core](/images/cubes/light-internals.jpg)

---

## 4. Manufacturing Process
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

---

## 5. Failure Analysis & Process Control
### The "Flip Cut" Failure
Early manufacturing attempts relied on double-sided machining (flipping the wood stock). This resulted in critical failures due to registration errors.

![Failure Analysis](/images/cubes/cube-fail.jpg)
*Left: Grain fracture due to misalignment. Right: The corrected process.*

* **The Failure:** When flipping the stock, registration errors of $<0.5mm$ caused the wall thickness to vary, leading to grain run-out and structural cracking under clamping pressure.
* **The Engineering Fix:** I redesigned the part to utilize a **Single-Setup Through-Bore**. By machining the entire internal cavity from one side and profiling the exterior in the same operation, I guaranteed vertical concentricity and eliminated the registration variable entirely.

![Failed SLA Print](/images/cubes/failed-sla.jpg)
*Early resin printing failures showing support detachment.*

---

## 6. Future Development
* **Scale:** Transitioning from batch prototyping to a 4-axis turning center for higher throughput.
* **Material:** Investigating cast optical silicone to replace the SLA resin for improved impact resistance.