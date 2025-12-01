---
title: "Machine Design: The 3-Axis Filament Winder"
date: 2024-03-25
description: "Designing, building, and programming a custom CNC machine for automated composite fabrication."
tags: ["Machine Design", "Klipper", "Python", "Composites"]
author: "Harley Bondini"
type: "blog"
layout: "single"
draft: false
---

# The Goal
To democratize custom carbon fiber tubing, I needed a way to produce consistent, high-performance laminates without the $50,000 price tag of industrial winders. My solution was to engineer a **3-Axis Filament Winder** from the ground up.

![ The Finished Machine ](/images/winder/winder-hero.jpg)
*The machine in operation, laying a ±45° helical pattern on a mandrel.*

---

## 1. Mechanical Design: The "Active Eye"
Most DIY winders use a static delivery ring. This causes the fiber to twist and fray when winding high angles. I engineered a **3rd Axis (Active Delivery Eye)** that rotates in sync with the carriage direction.

<video width="100%" controls autoplay loop muted playsinline>
  <source src="/images/winder/winder-closeup.mov" type="video/mp4">
  <source src="/images/winder/winder-closeup.mov" type="video/quicktime">
  Your browser does not support the video tag.
</video>
*Close-up of the Z-Axis rotating the eyelet to keep the carbon tow flat against the mandrel.*

### Key Features:
* **Motion System:** Custom 3-Axis (Rotational Spindle, Linear Carriage, Rotating Delivery Eye).
* **The "Spine":** A rigid steel core supports the flexible silicone mandrel, preventing whip at high RPM.

---

## 2. The "Brain": Klipper & Electronics
Most DIY winders use Arduino (Marlin). I chose **Klipper** because of its ability to handle high-speed kinematics. Winding non-cylindrical shapes requires rapid acceleration changes, and Klipper's "Input Shaping" helps smooth out the vibration.

<video width="100%" controls muted playsinline>
  <source src="/images/winder/winder-wide.mov" type="video/mp4">
  <source src="/images/winder/winder-wide.mov" type="video/quicktime">
  Your browser does not support the video tag.
</video>
*The full motion system running a dry-wind test pattern.*

---

## 3. The Logic: Solving "Pattern Drift"
The hardest part of this build was the math. Initial tests showed "Pattern Drift," where the fibers would leave gaps after several rotations.

### The "Closed-Loop" Algorithm
I wrote a custom **G-Code Generator** that runs in the browser. It calculates the **"Integer + Fraction"** ratio, dividing the mandrel circumference by the tow width (3mm) to find the exact number of passes needed.

> *"The code forces the machine to synchronize. After every Round Trip, the mandrel has rotated exactly One Integer Turn + One Bandwidth."*

---

## 4. Fabrication & Assembly
The frame is built from 2020/2040 aluminum extrusions. All custom brackets were printed in **ASA** to withstand the mechanical stress of the tensioner (approx 2kg load).

* **Wiring:** Custom crimped looms for the NEMA 23 motors.
* **Tensioner:** A spring-loaded dancer arm maintains constant tension on the carbon tow.

*You can view the full G-Code Generator tool in the [Project Docs](/docs/02-winder-engineering).*