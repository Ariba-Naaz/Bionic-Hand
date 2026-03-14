# 🧩 Challenges & Solutions

A running log of significant problems encountered during the design process and how they were resolved.

---

## Challenge 1 — Joint Dimension Accuracy

**Stage:** Stage 1 (Finger Design)  
**Status:** ✅ Resolved

### Problem
Translating real hand measurements into precise CAD geometry proved more complex than expected. Small inaccuracies in joint radii caused two key issues:
- **Binding** — joints would not rotate freely due to geometry overlap
- **Excessive play** — overly loose joints that didn't reflect realistic tolerances

When dimensions were taken from a ruler, the precision was limited, and scaling small anatomical features (like the curved articulation surface of a DIP joint) introduced cumulative errors.

### Solution
- Re-measured key dimensions using a more methodical approach, noting both the length and the width of each phalanx segment
- Cross-referenced measurements against published anthropometric ratio tables to sanity-check proportions
- Used **parametric modelling** in Fusion 360 — all joint radii and phalanx lengths were defined as named parameters, making iteration fast and consistent
- Added small tolerance offsets to joint contact surfaces to allow realistic clearance

### Lesson Learned
Design for parametric flexibility from the start. Hard-coding dimensions makes iteration slow and error-prone.

---

## Challenge 2 — Movement Constraints in Fusion 360

**Stage:** Stage 1 (Finger Design)  
**Status:** ✅ Resolved

### Problem
Fusion 360's joint system has two distinct workflows — **Joints** and **As-Built Joints** — and using them incorrectly resulted in:
- Joint origins snapping to wrong positions
- Motion limits not applying as expected
- Components rotating around unintended axes

Initial attempts to set up revolute joints for finger flexion produced erratic rotations because the joint origin planes were not aligned with the anatomical rotation axis of each joint.

### Solution
- Studied the difference between Joints (you define the origin) vs As-Built Joints (Fusion 360 uses current position)
- Adopted a strict convention: **always define joint origins on the rotation axis of the physical joint**, using the midpoint of the joint's cylindrical surface
- Set explicit **minimum and maximum rotation limits** on each revolute joint to match physiological ranges of motion
- Tested each joint independently before assembling fingers

### Lesson Learned
Joint origin placement is the most critical step in Fusion 360 assembly design. Take time to define it precisely before adding motion constraints.

---

## Challenge 3 — Assembly Alignment Issues

**Stage:** Stage 1 → Assembly  
**Status:** ✅ Resolved

### Problem
When bringing individual finger components together into a hand assembly, misaligned joint origins caused:
- Unexpected out-of-plane rotations
- Component clashing at joint interfaces
- Fingers pointing in inconsistent directions relative to the palm reference plane

The root cause was that each finger component had been modelled in isolation without a shared global coordinate reference.

### Solution
- Established a **global origin convention** at the start of each new component: all finger models use the same palm plane as their base reference
- Used Fusion 360's `Align` tool to correct existing misalignments before re-jointing
- Used `Capture Position` after alignment to lock corrected positions before adding joints
- Created a **master palm sketch** as a layout reference for placing all MCP joint origins relative to each other

### Lesson Learned
Define a shared coordinate reference before modelling any component intended for assembly. Retroactive alignment is time-consuming and error-prone.

---

## Challenge 4 — Reference Data for Human Hand Proportions

**Stage:** Research / Stage 1  
**Status:** ✅ Resolved

### Problem
Publicly available hand dimension data varies significantly between sources:
- Different studies report different average phalanx lengths
- Ratios between finger segments differ depending on the study population
- Most data is presented as population averages, not individual-specific measurements

Using averaged data would produce a hand that doesn't accurately represent any specific person's anatomy.

### Solution
- Decided to use **self-measured dimensions as the primary source** — this produces a model based on a real, specific hand
- Used academic anthropometric studies only for **validation and sanity checks** (e.g., confirming that measured ratios fall within normal ranges)
- Documented all raw measurements in `docs/dimensions.md` for reproducibility

### Lesson Learned
For a single-person-reference model, self-measurement is more accurate than population averages. Always document your measurement methodology.

---

## Ongoing Challenges

### Abduction/Adduction at MCP Joints
**Status:** 🔄 In Progress  
Adding lateral spreading movement to the MCP joints requires a 2-DoF joint setup (revolute for flex/ext + another axis for abd/add). This is more complex than a single revolute joint and is currently being explored.

### Thumb Opposition Geometry
**Status:** 🔲 Not Started  
The saddle joint geometry at the thumb's CMC joint is anatomically unique and significantly more complex than the hinge joints of the fingers. This will be the primary design challenge of Stage 2.
