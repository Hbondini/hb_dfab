---
title: "Machine Design: 3-Axis Filament Winder"
description: "Designing, building, and programming a custom CNC machine for automated composite fabrication."
tags: ["Machine Design", "Klipper", "Composites"]
image: "/images/winder/winder-hero.jpeg"
draft: false
---

# The Goal
To democratize custom carbon fiber tubing for the **HB_DFab Capstone**, I needed a way to produce consistent, high-performance laminates without the $50,000 price tag of industrial winders. My solution was to engineer a **3-Axis Filament Winder** from the ground up.

![ The Finished Machine ](/images/winder/winder-hero.jpeg)
*The machine in operation, laying a ±45° helical pattern on a mandrel.*

---

## 1. Mechanical Design: The "Active Eye"
Most DIY winders use a static delivery ring. This causes the fiber to twist and lay unevenly on the mandrel when winding high angles. I engineered a **3rd Axis (Active Delivery Eye)** that rotates in sync with the carriage direction.

<video width="100%" controls autoplay loop muted playsinline>
  <source src="/images/winder/winder-closeup.mov" type="video/mp4">
  Your browser does not support the video tag.
</video>
*Close-up of the Z-Axis rotating the eyelet to keep the carbon tow flat against the mandrel.*

### Key Features:
* **Motion System:** Custom 3-Axis (Rotational Spindle, Linear Carriage, Rotating Delivery Eye).
* **The "Spine":** A rigid steel core supports the flexible silicone mandrel, preventing whip at high RPM.

---

## 2. The "Brain": Klipper & Electronics
Most DIY winders use Arduino (Marlin). I chose **Klipper** because of its ability to handle high-speed kinematics.

<video width="100%" controls muted playsinline>
  <source src="/images/winder/winder-wide.mov" type="video/mp4">
  Your browser does not support the video tag.
</video>
*The full motion system running a dry-wind test pattern.*

---

## 3. The Logic: Solving "Pattern Drift"
The hardest part of this build was the math. Initial tests showed "Pattern Drift," where the fibers would leave gaps after several rotations. I wrote a custom **G-Code Generator** that calculates the **"Integer + Fraction"** ratio to lock the pattern.

> *You can view the full G-Code Generator tool and try the math yourself in the [Project Docs](/docs/02-winder-engineering).*