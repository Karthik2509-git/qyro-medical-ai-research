# Changelog

All notable changes to the QYRO Medical AI research documentation and dataset curation pipelines will be documented in this file.

---

## [1.0.0] - 2026-07-02
### Added
* 📂 **Dataset Factory v1.0:** Released the first stable version of the automated curation, audit, and cleaning pipeline.
* 🛡️ **Deduplication Audit:** Added global MD5 hashing to prevent data leakage (identified and resolved 145 duplicate files).
* ⚙️ **Class Remapping & Pruning:** Implemented programmatic remapping to the 5 clinical classes and pruned 8,012 noisy/irrelevant labels (e.g., milia, keloids, flat warts).
* 🔍 **Negative Sample Retention:** Retained 28 background images to teach the detector what *not* to detect in clinical settings.
* 📈 **Comparative Audits:** Documented baseline (v1) and calibration (v2) performance metrics in [README.md](file:///c:/Users/KARTHIK%20V/OneDrive/Desktop/Qyro-Acne/temp_research_repo/README.md).
* 📝 **Public Documentation Release:** Added CITATION.cff, CONTRIBUTING.md, ROADMAP.md, SECURITY.md, and LICENSE_NOTICE.md.
* 🔒 **IP Protection:** Updated public `.gitignore` rules to completely isolate proprietary source code, model weights, and clinical reasoning engine details.

---

## [0.9.0] - 2026-05-28
### Added
* 📥 **Ingestion Pipeline:** Initial import and structure mapping of raw Kaggle and Roboflow datasets.
* 🩺 **Audit Framework:** Drafted the dataset registry and audit protocols to evaluate raw annotation formats and image resolutions.
* 📐 **Resolution Profile:** Audited aspect ratios, verifying that 100% of candidate images have been padded/resized to standard 640x640 resolutions.
