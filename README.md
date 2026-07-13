# Audiologist Skills for PTA and Tympanometry AI Research

Version: 1.0.0  
Release date: 13 July 2026

This package contains the exact locked system-prompt texts used in the formal evaluations reported in:

> *Development and Component-Level Internal Testing of Audiologist-Guided AI for Audiogram Extraction, Audiological Rule Conformance, and Chinese Reporting*

## Contents

### 1. Image-recognition skill

File: [`prompts/audiogram_tympanometry_image_recognition_v10_locked.txt`](prompts/audiogram_tympanometry_image_recognition_v10_locked.txt)

- Formal version: `pta_tymp_recognition_only_v10_locked_boundary_abg_reflex500_skill`
- Used for the 105-case internally held-out image-recognition evaluation.
- Inputs were de-identified PTA and tympanometry images.
- The task was limited to visual extraction and prespecified rule-derived fields.
- Clinical diagnosis, treatment, urgency, and patient-management advice were prohibited.

### 2. Structured reasoning and Chinese reporting skill

File: [`prompts/structured_audiology_reasoning_and_chinese_reporting_v11.txt`](prompts/structured_audiology_reasoning_and_chinese_reporting_v11.txt)

- Formal version: `raw_pta_tymp_reasoning_v11_full_frequency_history_integrated`
- Used for the 95-case structured-input evaluation and report generation.
- Inputs were human-adjudicated structured PTA/tympanometry values and de-identified clinical context, not images.
- The skill calculated prespecified audiological fields and generated a Chinese professional report and a Chinese patient-facing report.
- The patient-facing instructions prioritize accuracy, short sentences, familiar words, and avoidance of unexplained technical units or treatment directives.

## Important study boundary

The two skills were evaluated as separate components. The reporting skill received adjudicated structured values rather than outputs from the image-recognition skill. The study therefore did not test an end-to-end clinical system or autonomous diagnostic performance.

## Integrity verification

`manifest.json` records the formal prompt version, evaluation case count, character count, and SHA-256 hash for each exact system prompt. The hashes exclude the final newline added to each text file.

## Data and privacy

This package contains no patient records, clinical images, case-level inputs, model outputs, hidden scoring references, local filesystem paths, or API credentials. Raw clinical records and source audiological images are not publicly available under hospital data-governance and research-ethics requirements.

## Intended use

These prompts are released for research reproducibility and further evaluation. They are not a medical device and should not be used for autonomous diagnosis, treatment, or patient management. Local audiological rules, equipment output limits, symbols, language, and clinical pathways may differ and require prospective validation.

## License

The prompt and documentation content in this repository is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0). See [LICENSE](LICENSE).
