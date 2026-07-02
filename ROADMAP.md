# QYRO Medical AI Research Roadmap

This document outlines the development phases, clinical validation strategies, and publication milestones for the QYRO Medical AI project.

---

## Phase 1: Dataset Acquisition & Quality Standardization (Completed)
* **Goal:** Standardize and sanitize noisy open-source dermatology datasets.
* **Milestones:**
  * ✅ Implemented **Dataset Factory v1.0** to automate curation.
  * ✅ Formulated an **Annotation Audit Protocol** to identify label coordinates errors.
  * ✅ Programmatically mapped classes to 5 target clinical subclasses: *Blackhead*, *Whitehead*, *Papular*, *Purulent*, and *Cystic*.
  * ✅ Ran global MD5 hashing to deduplicate images (removing 145 global duplicates) to prevent split leakage.
  * ✅ Integrated public datasets **DS001 (Roboflow)** and **DS002 (Kaggle)**.

---

## Phase 2: Model Training Calibration & Baseline Performance (In Progress)
* **Goal:** Establish reliable object detection baselines on the sanitized dataset.
* **Milestones:**
  * 🔄 Fine-tuning **Ultralytics YOLO** configurations with custom anchor points.
  * 🔄 Optimizing training hyper-parameters (learning rates, batch sizes, weight decay) to prevent VRAM overflow.
  * 🔄 Performing comparative audits between baseline training runs (v1) and sanitization/calibration runs (v2).
  * 🔄 Validating bounding box precision and recall improvements.

---

## Phase 3: Clinical Inference & Reasoning Calibration (In Progress)
* **Goal:** Build a robust, explainable rule engine that maps raw machine learning outputs to dermatologist-aligned severity staging.
* **Milestones:**
  * ✅ Formulated the **Severity Normalization (Area Coverage %)** multiplier to correct close-up photo bias.
  * ✅ Implemented **Stage 0 Reassurance Flow** to prevent false alarms on clear/minimal-acne skin.
  * ✅ Coded the **Close-Up Nose Safeguard** to ensure dense comedones on the nose bypass reassurance discounts.
  * ✅ Added **Mixed Pattern Detection** warning triggers when inflammatory and comedonal lesion counts overlap within 15%.
  * 🔄 Developing mock staging tests to verify that clinical staging remains highly consistent across various mock test cases.

---

## Phase 4: External Benchmarking & Cross-Validation (Planned)
* **Goal:** Validate model generalization on external datasets.
* **Milestones:**
  * ⬜ Integrate and process dataset **DS003 (ACNE04)** as an independent evaluation set.
  * ⬜ Benchmark classification accuracy against the **ISIC Dermatology Archive (DS005)**.
  * ⬜ Perform out-of-distribution (OOD) tests on chest/back acne vs facial acne.

---

## Phase 5: Clinical Collaboration & Safety Validation (Planned)
* **Goal:** Partner with medical professionals to validate diagnostic accuracy and safety.
* **Milestones:**
  * ⬜ Share the audit reports and pipeline methodologies with collaborating clinical researchers.
  * ⬜ Conduct blind evaluation studies where human dermatologists review and compare QYRO staging outputs.
  * ⬜ Incorporate clinician feedback to adjust decision boundaries and staging threshold rules.

---

## Phase 6: Academic Publication & Dissemination (Future)
* **Goal:** Present the QYRO pipeline, auditing findings, and explainable AI staging model in peer-reviewed dermatology AI venues.
* **Milestones:**
  * ⬜ Write and submit a comprehensive research paper on the Dataset Factory curation methodology.
  * ⬜ Release supplementary research material and companion tables.
