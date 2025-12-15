# Dataset Labeling Guideline for Tablet Visual Inspection

## 1. Purpose
This document defines standardized labeling rules for tablet image datasets used in AI-assisted visual inspection.

The purpose is to ensure consistent, reproducible, and QC-aligned labeling of normal and defective tablet images.

---

## 2. Labeling Scope
This guideline applies to:

- Single-tablet images
- Images used for training, validation, and testing datasets
- Normal vs defect classification for MVP stage

Multi-class defect labeling may be added in later phases.

---

## 3. Reference Documents
Labeling rules are based on the following design documents:

- QC-Based Tablet Visual Defect Definition (`qc_defect_definition.md`)
- Image Feature Definition (`image_feature_definition.md`)
- MVP Inspection Flow Design (`mvp_inspection_flow.md`)

---

## 4. Label Categories

### 4.1 Normal
An image is labeled as Normal when:

- No visible cracks, breakage, or chipping are present
- No foreign matter is observed on the tablet surface
- Color and surface texture fall within acceptable limits
- Tablet shape and geometry are intact

Minor cosmetic variations within QC acceptance range are classified as Normal.

---

### 4.2 Defect
An image is labeled as Defect when one or more of the following conditions are met:

- Visible crack, breakage, or chipping
- Presence of foreign matter on the tablet surface
- Abnormal discoloration beyond acceptable range
- Shape deformation or structural damage

If any defect is clearly observable, the image must be labeled as Defect regardless of defect size.

---

## 5. Labeling Rules and Principles

### 5.1 Conservative Labeling Rule
When labeling is ambiguous, the image should be labeled as Defect.

This conservative approach aligns with pharmaceutical QC risk management principles.

---

### 5.2 Single Label Policy (MVP Stage)
- Each image receives only one label: Normal or Defect
- Images showing multiple defect types are still labeled as Defect

Detailed defect categorization may be introduced in future versions.

---

### 5.3 Image Quality Considerations
Images with the following issues should be excluded or flagged:

- Severe blur
- Insufficient lighting
- Partial tablet visibility
- Background interference affecting tablet segmentation

Such images should not be used for training without review.

---

## 6. Labeling Procedure
The recommended labeling workflow is as follows:

1. Verify image quality and visibility
2. Inspect tablet appearance based on QC criteria
3. Assign Normal or Defect label
4. Record labeling decision and reviewer information if applicable

---

## 7. Label Consistency Check
To ensure labeling reliability:

- Periodic review of labeled samples is recommended
- Disagreements should be resolved using QC defect definitions
- Reference images for Normal and Defect should be maintained

---

## 8. Application in AI Development
This labeling guideline supports:

- Dataset construction for model training
- Reduction of label noise
- Improved model interpretability
- Alignment between AI outputs and QC expectations

---

## 9. Notes
This guideline defines baseline labeling rules for MVP development and may be refined based on product-specific QC requirements and regulatory standards.
