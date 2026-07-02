# Security Policy

This document outlines the security, data privacy, and patient safety policies for the QYRO Medical AI research repository.

---

## 1. Patient Data & PHI Policy

As a research-focused project, **no Patient Health Information (PHI), patient records, or personally identifiable clinical images are permitted or stored in this repository.**

* **No PHI Allowed:** All images, metadata, and testing cases used during research are sourced from public, anonymized academic dataset repositories.
* **No Diagnostic Claims:** No diagnostic assertions, prescriptions, or clinical triage operations are conducted using this repository.
* **Prohibited Submissions:** Do not open issues, submit pull requests, or upload attachments containing personal medical images, names, or contact information. Any such submissions will be immediately and permanently deleted.

---

## 2. Responsible Disclosure

If you discover a security vulnerability (such as exposed credentials, local path disclosures, or metadata leakage in documentation):

1. **Do NOT open a public issue.**
2. Report the vulnerability privately by contacting the maintainer at **karthikvanapalli08@gmail.com**.
3. We will review and address the vulnerability as a high priority.

---

## 3. Model & Output Safety

Because QYRO is designed to explore AI in clinical workflows, model safety is a key research area. We implement the following guidelines:
* **Clinically Calibrated Safeguards:** We test decision staging logic to ensure it doesn't fail silently (for instance, flagging close-up nose comedones even if generic counts are low).
* **Bias Assessment:** We audit our datasets for class imbalance (such as whitehead under-representation) to understand model limitations and document them transparently in our public reports.
