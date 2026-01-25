




---
title: "Lecture HW2 — CAVE System"
date: 2025-12-02
draft: false
tags: ["IGD301", "lecture", "vr", "CAVE System"]
---




### 1. Difference between a CAVE system and Head-Mounted Displays (HMDs)

A CAVE (Cave Automatic Virtual Environment) is a room-scale immersive display: stereo projections are shown on multiple surfaces (walls, floor, sometimes ceiling), so the user stands inside the display space. The system is typically combined with position tracking so that the rendered viewpoint updates with the user’s motion and preserves a natural perspective.

An HMD delivers the visuals through a head-worn device, with the virtual scene presented individually to each user. The user’s viewpoint is updated primarily through head tracking.

The key difference is the relationship between display and space: a CAVE places imagery on surrounding physical surfaces and the user is inside that space; an HMD places imagery directly in the user’s personal field of view.

---

### 2. Advantages and disadvantages

This comparison focuses on immersion, usability, visual quality, and collaboration. The paper explicitly compares multiple interface types along dimensions such as field of view, intrusiveness, visual acuity, and multi-user support. 

#### 2.1 Advantages of CAVE

A CAVE can provide a near “full” surrounding field of view, with fast and natural look-around behavior (the table characterizes its FOV as Full and look-around speed as Fast). It is also non-intrusive (listed as None), meaning it does not block the face or isolate the user from the physical room, which supports comfort, longer sessions, and face-to-face communication.

The CAVE is described as a nonintrusive, high-resolution VR interface that outperforms other paradigms on several immersive visualization problems, and it is well suited for co-located discussion and shared viewing in the same space. 

#### 2.2 Disadvantages of CAVE

A CAVE requires dedicated space and substantial hardware setup (projection, synchronization, calibration, and tracking). In multi-user situations, perspective is usually correct only for the primary tracked viewer; others will see a mismatched viewpoint unless additional techniques are used, which can introduce tradeoffs such as changes in brightness, refresh rate, or other display constraints. 

In terms of visual clarity, the table reports that CAVE visual acuity is not the best among compared displays (e.g., CAVE 20/110 versus CRT 20/45), reflecting limitations of projection-based display chains. 

#### 2.3 Advantages of HMD

A practical advantage of HMDs is deployment: they do not require a dedicated room-scale installation, and they are easier to move and reproduce. For individual immersion, the table reports a large field of view (about 100°–140°) and full look-around capability, which supports strong personal presence. 

#### 2.4 Disadvantages of HMD

HMDs are highly intrusive (listed as Full), since the device blocks the real world and adds wearing burden. Visual quality can also be a constraint; the table reports relatively low visual acuity for the HMD case (20/425), making clarity and comfort common limiting factors.

For collaboration, HMDs tend to be more individual: multi-user shared experiences typically require multiple devices and additional synchronization mechanisms, which increases complexity. 

---

### 3. Where the CAVE fits in Milgram’s Reality–Virtuality Continuum

Milgram’s continuum ranges from the real environment through augmented reality (AR) and augmented virtuality (AV) to fully virtual environments (VR/VE). A CAVE primarily delivers computer-generated 3D content and aims at immersive surround presentation, so it sits on the virtual environment (VE) side of the continuum.

Compared with an HMD, a CAVE more easily preserves real-world cues because users remain in a physical room and can still perceive their bodies, the floor, and co-located people. For that reason, it still belongs to VE, but it can be argued to lie closer to the boundary toward augmented virtuality (AV) in terms of subjective experience.

---

### 4. Does the position change when more people experience the CAVE at the same time?

In terms of system category, the CAVE remains a virtual-environment display because the primary content remains virtual; the paradigm does not change simply because more users are present.

However, the experience can diverge across users in a shared CAVE. If viewpoint rendering is optimized for a single tracked viewer, that person receives correct perspective while others may experience reduced immersion (closer to “shared stereo projection” than fully consistent VE). The paper notes that multi-user operation involves tradeoffs and that different interface paradigms have different costs for collaboration. 

So the position on the continuum does not fundamentally change, but simultaneous multi-user viewing can reduce immersion for some participants, shifting their subjective experience slightly toward the real side.

