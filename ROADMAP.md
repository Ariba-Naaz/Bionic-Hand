# 🗺️ Project Roadmap — Bionic Hand CAD

This document outlines the planned development stages for the Bionic Hand CAD project, from the current implementation to a fully articulated, assembly-ready model.

---

## ✅ Stage 1 — Finger Design 

**Goal:** Model all four fingers with functional flexion and extension.

- [x] Design phalanx geometry (proximal, middle, distal) for all four fingers
- [x] Implement flexion/extension at MCP, PIP, and DIP joints
- [x] Derive dimensions from self-measured hand proportions
- [x] Validate joint motion in Fusion 360 simulation
- [ ] Add abduction/adduction at MCP joints *(in progress)*

---

## 🔄 Stage 2 — Thumb Design

**Goal:** Fully articulated thumb with all natural degrees of freedom.

- [ ] Model thumb phalanges (proximal, distal) and metacarpal
- [ ] Implement flexion/extension at MCP joint
- [ ] Implement flexion/extension + abduction/adduction at CMC joint
- [ ] Add supination/pronation (rotation) at CMC joint
- [ ] Validate full thumb motion range against natural hand

---

## 🔲 Stage 3 — Palm Arch (4th & 5th CMC Joints)

**Goal:** Replicate the natural palm curvature essential for realistic gripping.

- [ ] Model carpometacarpal joints for ring and pinky fingers
- [ ] Implement flexion/extension at both CMC joints
- [ ] Integrate with existing finger assemblies
- [ ] Validate palm arch curvature against anatomical reference

---

## 🔲 Final Stage — Full Assembly & Integration

**Goal:** A single, cohesive bionic hand assembly with all joints functional.

- [ ] Assemble all finger + thumb + palm components
- [ ] Resolve any component clashing or joint conflicts
- [ ] Run full motion simulation across all degrees of freedom
- [ ] Export assembly for documentation and presentation
- [ ] Generate STL exports for 3D print feasibility check

---

## 🔲 Bonus Stage — Wrist Movements

**Goal:** Extend the model with a functional wrist joint.

- [ ] Design wrist joint geometry
- [ ] Implement flexion/extension
- [ ] Implement radial/ulnar deviation
- [ ] Optional: Pronation/supination of the wrist
- [ ] Integrate wrist with full hand assembly

---

## 🔭 Future Possibilities (Post-Project)

These are exploratory ideas beyond the current scope:

- **Actuation Design** — Route tendon/cable paths or servo motor mounts through the model for physical build feasibility
- **3D Printing Prototype** — Print individual components in PLA/PETG and test real-world articulation
- **Sensor Integration** — Plan housing for flex sensors or encoders at key joints
- **Soft Robotics Variant** — Explore redesigning joints for pneumatic actuation
- **Simulation Export** — Import into ROS/Gazebo or similar for motion planning tests

---

*Last updated: March 2026*
