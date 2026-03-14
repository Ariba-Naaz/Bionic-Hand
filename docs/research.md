# 📚 Research & References

This document compiles all research sources, references, and findings used during the design of the Bionic Hand CAD model.

---

## 🖐️ Human Hand Anatomy

### Key Joint Terminology
| Abbreviation | Full Name | Location |
|---|---|---|
| **MCP** | Metacarpophalangeal | Knuckle (base of finger) |
| **PIP** | Proximal Interphalangeal | Middle finger joint |
| **DIP** | Distal Interphalangeal | Fingertip joint |
| **CMC** | Carpometacarpal | Base of thumb / palm arch |
| **IP** | Interphalangeal | Thumb's single finger joint |

### Degrees of Freedom per Joint (Natural Hand)
| Joint | Motion Type | Range (approx.) |
|---|---|---|
| MCP (fingers) | Flexion/Extension | 0°–90° |
| MCP (fingers) | Abduction/Adduction | ±20° |
| PIP | Flexion/Extension | 0°–110° |
| DIP | Flexion/Extension | 0°–70° |
| Thumb CMC | Flexion/Extension | 0°–50° |
| Thumb CMC | Abduction/Adduction | 0°–70° |
| Thumb CMC | Opposition/Rotation | ~90° |

---

## 📐 Dimension Reference — Self-Measured

All primary dimensions used in this CAD model are derived from direct measurements of the designer's own hand using a ruler and digital caliper.

### Measurements Taken
- Proximal phalanx length (all 5 fingers)
- Middle phalanx length (fingers 2–5)
- Distal phalanx length (all 5 fingers)
- Joint width at MCP, PIP, DIP
- Metacarpal length (all 5)
- Palm width and depth
- Thumb segment lengths

> 📁 Raw measurement data: `docs/dimensions.md`

---

## 📄 Academic & Technical Sources

### Biomechanics & Anthropometry
- Studies on average human hand proportions and phalanx length ratios
- Range-of-motion data for finger and thumb joints from biomechanics literature
- Anthropometric databases (used for cross-validating self-measured dimensions)

### Prosthetics & Bionic Hand Research
- Published designs of open-source prosthetic hands:
  - **e-NABLE Community** — open-source 3D printed prosthetic hand designs
  - **InMoov** — open-source 3D printed humanoid robot hand
- Research papers on underactuated robotic hand design
- Technical reports on tendon-driven finger mechanisms

---

## 🎥 Video & Tutorial References

### Fusion 360 Specific
- Joint creation and motion limits in Fusion 360 (Autodesk official tutorials)
- As-Built Joints vs Joints — workflow and best practices
- Assembly techniques for multi-body mechanical designs
- Parametric modelling and constraints in Fusion 360

### Mechanical Design Concepts
- Linkage mechanisms for robotic fingers
- Joint tolerance design for 3D-printed mechanisms
- Degrees of freedom analysis for robotic hands

---

## 🔗 Useful Links

| Resource | URL |
|---|---|
| Fusion 360 Help Center | https://help.autodesk.com/view/fusion360/ENU/ |
| e-NABLE Community | https://enablingthefuture.org |
| InMoov Project | https://inmoov.fr |
| Thingiverse — Robotic Hand Designs | https://www.thingiverse.com |

---

## 📝 Notes

- Self-measured dimensions are the **primary reference** — this ensures the model reflects a real, specific hand rather than averaged data.
- Academic sources were used to **validate proportions** and joint motion ranges, not as the primary dimensional source.
- All YouTube tutorial references were used for **Fusion 360 technique**, not anatomical data.
