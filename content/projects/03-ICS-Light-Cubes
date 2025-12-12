---
title: "ICS Light Cubes"
subtitle: "A modular, reconfigurable lighting ecosystem designed for adaptive environments."
date: 2024-03-21
tags: ["Product Design", "Mechatronics", "CNC", "SLA Printing"]
image: "/images/cubes/cube-hero.jpg" 
draft: false
---

<div style="margin-bottom: 2rem; padding: 1.5rem; background: #f4f4f4; border-radius: 8px; border-left: 5px solid #333;">
    <h3 style="margin-top: 0;">📥 Engineering Defense Deck</h3>
    <p>This project was presented as a technical manufacturing defense. You can view the full slide deck detailing the electrical topology and CAM strategies below.</p>
    <a href="https://hbdfab.blob.core.windows.net/assets/ICS-Light-Cubes%20(1).pptx" style="display: inline-block; padding: 10px 20px; background: #333; color: white; text-decoration: none; font-weight: bold; border-radius: 4px;">
        Download Presentation (.pptx)
    </a>
</div>

## 1. The Design Problem
**The Limitations of Static Lighting**
Residential lighting forces a binary choice: high-intensity overhead lighting (stimulation) or fixed ambient lamps (cord-restricted). There was no solution for "migratory" lighting that moves with the user without the friction of cables.

* **Objective:** Create a tangible, battery-free lighting object that transitions from a single task light to a linear array in seconds.
* **Philosophy:** "Tangible Interaction." Eliminating switches in favor of physical docking as the trigger for illumination.

---

## 2. System Architecture
### Contact-Based Power Topology
To eliminate cables while maintaining safety, I engineered a contact-based power architecture using the **USB-A Standard (5V)**.

![System Diagram](/images/cubes/cube-pogo.jpg)
*Detail of the spring-loaded pogo interface and magnetic alignment guides.*

* **SELV Compliance:** By utilizing 5V DC, the system remains within Safety Extra Low Voltage limits, making the exposed contact pads on the base station "human-safe" to touch.
* **The Interconnect:** I selected **Spring-Loaded Pogo Pins** rated for 10,000 cycles. These provide 2.5mm of vertical travel, absorbing minor planarity variances in the wooden housing to ensure constant electrical contact.
* **Magnetic Assist:** Embedded Neodymium magnets provide a "self-aligning" force, pulling the cube into the correct docking position to guarantee pin-to-pad alignment without user effort.

---

## 3. Mechanical Design
### The Serviceability Mandate
A core requirement was that the device must be repairable. I refused to use permanent adhesives to seal the electronics inside the wood.

**The "Fastmount" Inspiration**
I researched architectural panel mounting systems and adapted the geometry of the industrial **Fastmount** friction-clip system for 3D printing.

* **The Challenge:** Creating a snap-fit mechanism that holds the assembly under tension but releases with a specific force ($>15N$) for disassembly.
* **The Solution:** I iterated through dozens of 3D printed clip profiles to tune the tolerances. The final design allows the internal electronics core to "snap" into the wooden shell, holding the optical diffuser flush against the Douglas Fir housing.

---

## 4. Manufacturing Process
### Hybrid Fabrication Strategy
The aesthetic required the warmth of natural grain, but the mechanics required the precision of engineering plastics.

| Component | Manufacturing Method | Material |
| :--- | :--- | :--- |
| **Housing** | Subtractive (CNC Machining) | Solid Douglas Fir |
| **Diffuser** | Additive (SLA Printing) | Translucent Resin |
| **Chassis** | Additive (FDM Printing) | PETG / PLA+ |

![CNC Process](/images/cubes/cnc-process.jpg)
*The Douglas Fir housing being machined. Note the "Through-Bore" strategy.*

---

## 5. Failure Analysis & Process Control
### The "Flip Cut" Failure
Early manufacturing attempts relied on double-sided machining (flipping the wood stock). This resulted in critical failures due to registration errors.

![Failure Analysis](/images/cubes/cube-fail.jpg)
*Left: Grain fracture due to misalignment. Right: The corrected process.*

* **The Failure:** When flipping the stock, registration errors of $<0.5mm$ caused the wall thickness to vary, leading to grain run-out and structural cracking under clamping pressure.
* **The Engineering Fix:** I redesigned the part to utilize a **Single-Setup Through-Bore**. By machining the entire internal cavity from one side and profiling the exterior in the same operation, I guaranteed vertical concentricity and eliminated the registration variable entirely.

---

## 6. Future Development
* **Scale:** Transitioning from batch prototyping to a 4-axis turning center for higher throughput.
* **Material:** Investigating cast optical silicone to replace the SLA resin for improved impact resistance.