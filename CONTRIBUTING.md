# Contributing to QYRO Medical AI Research

Thank you for your interest in contributing to the QYRO Medical AI project! As an active medical AI research effort, we prioritize scientific rigor, documentation integrity, patient privacy, and clinical safety.

This document outlines our standards and workflow for contributions.

---

## 1. Research Contribution Scope

We welcome contributions across several key research areas:
* **Dataset Audits:** Identifying labels, exposure biases, or duplicates in public dermatological datasets.
* **Clinical Calibration Suggestions:** Refining severity score rules and mixed-pattern warning criteria.
* **Methodology Reviews:** Improving evaluation metrics and standardizing classes.
* **Documentation:** Enhancing explanations, diagrams, or references.

*Note: Since the core model training and source code are proprietary, software development contributions are currently focused on validation tooling, documentation, and research design.*

---

## 2. Commit Message Conventions

We follow clear semantic commit prefixes to keep the repository history readable and structured:

* `docs:` Documentation improvements (e.g., `docs: update dataset audit metrics`)
* `chore:` Repository maintenance, git configuration (e.g., `chore: update public gitignore`)
* `style:` Layout, formatting, or spelling updates.
* `refactor:` Restructuring documentation or reports without changing content.

**Example Commit Message:**
```bash
docs: add audit findings for Kaggle dataset duplicates
```

---

## 3. Branch Naming Conventions

When working on a research proposal, document update, or audit report, please name your branch according to the following conventions:

* `research/` — Research reports, clinical mapping, or academic notes (e.g., `research/acne04-audit`)
* `docs/` — General repository documentation updates (e.g., `docs/contributing-guidelines`)
* `feature/` — Non-proprietary validation tools or scripts (e.g., `feature/duplicate-hash-script`)
* `fix/` — Fixing typos or layout rendering bugs (e.g., `fix/readme-table-alignment`)

---

## 4. Coding Standards

If you are developing non-proprietary diagnostic tools, preprocessing scripts, or validation utilities:
* **Python Code:** Adhere strictly to **PEP 8** style guidelines.
* **Comments and Docstrings:** Maintain comprehensive docstrings explaining the clinical/mathematical rationale behind functions.
* **No Hardcoded Paths:** Always use relative or absolute path anchoring based on the script location to prevent local machine path leakage.

---

## 5. Dataset Requirements

When proposing the integration of new public dermatology datasets:
1. **License Compliance:** The dataset must permit research or non-commercial use. Proprietary or patient-identifiable datasets without proper consent agreements are strictly prohibited.
2. **Annotation Standards:** Bounding boxes must correspond to our 5 clinical lesion subtypes (*Blackhead*, *Whitehead*, *Papular*, *Purulent*, *Cystic*).
3. **Audit First:** Any dataset must undergo a documented programmatic and visual audit (as detailed in [dataset_audit_plan.md](file:///c:/Users/KARTHIK%20V/OneDrive/Desktop/Qyro-Acne/docs/dataset_audit_plan.md)) before candidate selection.

---

## 6. Responsible Disclosure & Issue Reporting

When reporting issues or proposing changes:
* **Do NOT upload patient images or PHI:** Never include any Protected Health Information (PHI) or personal patient photos in issues or PRs. Only use anonymized, public research dataset images.
* **Describe the Context:** Provide the dataset ID (e.g., DS001), the tool version, and the clinical reason for the issue.
