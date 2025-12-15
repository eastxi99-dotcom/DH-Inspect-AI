# Image Feature Definition for Tablet Visual Inspection

## 1. Purpose
This document defines image-based features used to translate QC visual inspection criteria into measurable parameters for AI-assisted tablet inspection.

The purpose is to bridge pharmaceutical QC defect definitions with objective image processing indicators.

---

## 2. Reference Document
This feature definition is based on the following QC document:

- QC-Based Tablet Visual Defect Definition (`qc_defect_definition.md`)

---

## 3. Image Input Specification
- Image Type: Tablet image (single tablet per image)
- Format: JPEG or PNG
- Background: Uniform background preferred
- Orientation: No strict orientation requirement
- Resolution: Sufficient to clearly observe tablet edges and surface texture

---

## 4. Feature Categories Overview
The following feature categories are used for defect detection:

- Shape and contour features
- Area-based features
- Surface texture features
- Intensity and color distribution features

---

## 5. Feature Definition by Defect Type

### 5.1 Crack and Breakage
Associated QC Defects:
- Crack
- Breakage
- Chipping

Image Features:
- Contour discontinuity
- Edge irregularity
- Sudden changes in contour curvature
- Local gaps or breaks in the tablet boundary

Evaluation Concept:
- Comparison of detected contour against an expected continuous outline
- Detection of abnormal breaks or missing segments

---

### 5.2 Area Loss and Structural Damage
Associated QC Defects:
- Breakage
- Chipping

Image Features:
- Tablet area reduction ratio
- Missing region detection
- Comparison with reference normal tablet area

Evaluation Concept:
- Calculate tablet area after segmentation
- Compare area ratio to predefined acceptance threshold

---

### 5.3 Surface Foreign Matter
Associated QC Defects:
- Foreign Matter

Image Features:
- Localized intensity or color anomalies
- Abnormal texture patterns on tablet surface
- Small isolated regions not matching tablet material

Evaluation Concept:
- Detection of pixel clusters deviating from normal surface distribution
- Identification of non-uniform surface regions

---

### 5.4 Discoloration
Associated QC Defects:
- Discoloration

Image Features:
- Global and local intensity distribution
- Histogram deviation from reference normal tablet
- Color or grayscale variance across tablet surface

Evaluation Concept:
- Compare intensity histogram against normal reference range
- Flag images exceeding acceptable deviation limits

---

### 5.5 Shape Deformation
Associated QC Defects:
- Shape Deformation

Image Features:
- Aspect ratio
- Circularity or symmetry metrics
- Deviation from standard geometric profile

Evaluation Concept:
- Quantitative comparison of tablet geometry against predefined shape parameters

---

## 6. Feature-to-Decision Mapping
Each extracted feature contributes to the final inspection decision:

- Minor deviation within tolerance: Normal
- Significant deviation exceeding threshold: Defect
- Multiple minor deviations: Defect (combined rule)

Decision logic may be rule-based in MVP stage and expanded to ML/DL models in later phases.

---

## 7. Application in MVP Development
These features serve as:

- Guidance for initial image processing implementation
- Reference for dataset labeling consistency
- Baseline inputs for simple classification models

---

## 8. Notes
Feature thresholds and evaluation logic should be adjustable depending on tablet formulation, shape, and QC standards.

This document represents a conceptual design and will be refined during implementation and testing.
