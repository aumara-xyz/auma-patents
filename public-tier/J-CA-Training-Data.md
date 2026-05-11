# California AI Training Data and Frontier Model Transparency Evidence Compiler

**Inventor:** Peter Michael Viviani  
**Assignee:** AUMARA LLC  
**Docket:** AUMARA-J-PROV-001  
**Filing Date:** 2026  
**Application Type:** Provisional Patent Application

---

## Cross-Reference to Related Applications

This provisional application is related by common inventorship and common ownership to: CONTRIBUTOR-AWARE ADAPTATION (CAA), filed March 21, 2026; and RISK DRIFT SENTINEL (RDS), filed March 21, 2026, docket AUMARA-RDS-PROV-001. Related applications are identified for context only. The present invention does not require any component of the related applications to be practiced.

---

## Field of the Invention

The invention relates to computer-implemented compliance infrastructure for generative artificial intelligence developers and frontier model developers, and more particularly to training data documentation, dataset summarization, substantial modification tracking, synthetic data disclosure, provenance disclosure, safety framework linkage, incident reporting evidence, watermark or content transparency evidence, and public disclosure package generation for systems made available to Californians or otherwise subject to California artificial intelligence transparency laws.

---

## Background of the Invention

California AB 2013 added Title 15.2 to the California Civil Code concerning artificial intelligence training data transparency. The law requires developers of generative artificial intelligence systems released on or after January 1, 2022 and made available to Californians to post documentation regarding data used to train the system, including high-level summaries of datasets, sources or owners, purpose, number of data points, protected or copyrighted content indicators, collection periods, first-use dates, modifications, and synthetic data use.

California SB 53, the Transparency in Frontier Artificial Intelligence Act, concerns frontier model safety and transparency, including governance frameworks, transparency reports, and safety incident mechanisms. California SB 942, the California AI Transparency Act, concerns AI-generated content disclosures, detection tools, manifest disclosures, and latent disclosures for covered providers.

Generative AI developers have training data manifests, dataset cards, data lakes, licensing records, web crawl logs, synthetic generation systems, fine-tuning pipelines, model release notes, safety evaluation records, incident tickets, and content provenance tooling. But these artifacts are not organized around statutory release-triggered disclosure. The technical problem is to convert internal training data lineage into a public, statute-aligned, trade-secret-minimized, release-specific evidence package while preserving internal proof of how the disclosure was generated.

---

## Summary of the Invention

Disclosed is a California AI Training Data and Frontier Model Transparency Evidence Compiler. The compiler receives training dataset lineage, dataset ownership data, licensing metadata, copyright and personal data flags, data collection windows, preprocessing and modification records, synthetic data generation records, fine-tuning records, evaluation records, model release records, content provenance capabilities, frontier model safety framework records, and safety incident records. The compiler produces a Training Data Transparency Evidence Object and one or more public disclosure packages.

The invention is architecture-agnostic and may be implemented as a developer compliance tool, data catalog plugin, model registry extension, ML pipeline plugin, release management system, SaaS platform, on-prem appliance, or governance evidence service.

---

## Detailed Description of Preferred Embodiments

### 1. System Components

A **training lineage connector** imports dataset identifiers, file manifests, dataset cards, source logs, web crawl metadata, license metadata, content categories, collection periods, preprocessing operations, deduplication records, safety filtering records, fine-tuning records, validation records, and synthetic data generation records.

A **model release connector** receives model family, model version, release date, intended availability, California availability, substantial modification flags, release notes, API endpoints, model cards, safety evaluations, and frontier model status.

A **disclosure policy compiler** maps statutory disclosure elements to internal records. It selects high-level fields appropriate for public disclosure while preserving a private evidence record. It may generalize, bucket, redact, or aggregate internal records to avoid exposing trade secrets, security-sensitive details, or personal data.

A **frontier and content transparency linker** links training data disclosures to safety governance frameworks, model capability evaluations, incident reporting objects, AI-generated content provenance tools, detection tools, manifest disclosure settings, and latent disclosure settings.

### 2. Core Data Object: TRAINING_DATA_TRANSPARENCY_EVIDENCE_OBJECT

The most important non-obvious object is the **TRAINING_DATA_TRANSPARENCY_EVIDENCE_OBJECT** — a release-bound object, not merely a dataset card.

Key fields:
- `evidence_id`: UUID.
- `model_release_id`: STRING.
- `california_availability_flag`: BOOLEAN.
- `released_on_or_after_2022_01_01_flag`: BOOLEAN.
- `substantial_modification_flag`: BOOLEAN.
- `disclosure_trigger_state`: ENUM {not_triggered, triggered_pre_release, triggered_public_update, triggered_substantial_modification, exception_claimed, completed}.
- `dataset_summaries`: ARRAY of DATASET_DISCLOSURE_SUMMARY. Each includes `dataset_id`, `public_dataset_name`, `source_or_owner_category`, `source_or_owner_public_text`, `intended_purpose_text`, `data_point_count_bucket`, `data_modality` ARRAY of {text, image, video, audio, code, tabular, biometric, sensor, other}, `data_category_tags`, `collection_start_date`, `collection_end_date`, `ongoing_collection_flag`, `first_used_date`, `copyrighted_material_indicator` ENUM {yes, no, unknown, mixed}, `personal_information_indicator` ENUM {yes, no, unknown, mixed}, `sensitive_personal_information_indicator`, `child_data_indicator`, `license_basis_category` ENUM {owned, licensed, public_domain, user_generated, web_crawl, synthetic, government, mixed, unknown}, `modification_summary_text`, `synthetic_data_role` ENUM {none, seed, generated, augmented, evaluation, mixed}, and `public_redaction_basis`.
- `private_lineage_refs`: ARRAY of internal_dataset_id, storage_uri, manifest_hash, license_record_hash, preprocessing_pipeline_hash, and access_control_label.
- `excluded_dataset_records`: ARRAY of dataset_id, exclusion_basis, approver_id, and evidence_hash.
- `public_disclosure_package_ref`: package_id, generated_timestamp, publication_url, package_hash, template_version, human_approver_id, and publication_status ENUM {draft, approved, published, superseded}.
- `frontier_model_state`: frontier_flag, compute_or_capability_basis, safety_framework_ref, transparency_report_ref, catastrophic_risk_eval_refs, incident_reporting_channel_ref, and whistleblower_policy_ref.
- `content_transparency_state`: detection_tool_available, manifest_disclosure_available, latent_disclosure_enabled, provenance_standard_refs, watermarking_capability_ref, and user_option_state.
- `validation_state`: completeness_score FLOAT, missing_required_elements ARRAY, conflict_flags ARRAY, and legal_review_state ENUM {not_started, in_review, approved, rejected}.
- `evidence_hash` and `previous_evidence_hash`: Hash chain fields.
- `signature_block`: Ed25519 digital signature.

A model_release_id has one active TRAINING_DATA_TRANSPARENCY_EVIDENCE_OBJECT and may have prior superseded objects.

### 3. Release-Triggered Compilation

When a model is prepared for release, the compiler determines whether the model is a generative AI system or service, whether it was released or substantially modified after the relevant date, and whether it is made publicly available to Californians. If triggered, the compiler retrieves required dataset summaries and generates a disclosure package before public release. When a model is substantially modified, the compiler creates a new evidence object that inherits prior dataset summaries and adds modification records.

### 4. Redaction and Public/Private Split

The compiler maintains a private evidence layer and a public disclosure layer. The private evidence layer stores internal lineage, exact hashes, storage URIs, license details, and evidence of completeness. The public layer contains the high-level summary required for publication. Redaction rules may remove exact URLs, security-sensitive details, trade secrets, or individual-level data while preserving statutory fields.

### 5. Synthetic Data and Modification Tracking

The compiler identifies synthetic data used for training, validation, fine-tuning, or augmentation. It stores whether synthetic data was generated from seed data, whether the seed data was public, licensed, or proprietary, and whether synthetic data serves a functional need such as privacy protection, balance, edge-case generation, or safety evaluation.

---

## Claims

1. A computer-implemented method comprising: receiving training data lineage records for a generative artificial intelligence system; receiving a model release record; determining whether a public training data documentation obligation is triggered; generating a training data transparency evidence object that binds the model release record to dataset summaries, private lineage references, synthetic data records, modification records, and public disclosure package state; and generating a public disclosure package from the evidence object.

2. A system comprising one or more processors and memory storing instructions that, when executed, cause the system to: map internal dataset lineage fields to statutory disclosure fields; apply public redaction rules; preserve private evidence hashes; detect substantial model modifications; and publish or stage a release-specific training data disclosure package.

3. A non-transitory computer-readable medium storing instructions that, when executed, cause processors to link a model release transparency object to frontier model safety framework records, safety incident reporting records, content provenance capability records, manifest disclosure records, and latent disclosure records.

4. The method of claim 1, wherein the dataset summaries include source or owner category, intended purpose, data point count bucket, modality, collection period, first-use date, copyright indicator, personal information indicator, modification summary, and synthetic data role.

5. The system of claim 2, wherein a private lineage reference includes an internal dataset identifier, storage URI, manifest hash, license record hash, preprocessing pipeline hash, and access control label.

6. The method of claim 1, wherein the public disclosure package is generated from a private evidence object using redaction rules that preserve statutory fields while suppressing trade-secret, security-sensitive, or personal data.

7. The system of claim 2, wherein a substantial modification of the generative artificial intelligence system creates a new evidence object linked to a prior superseded evidence object.

8. The medium of claim 3, wherein content transparency capability records include detection tool availability, manifest disclosure availability, latent disclosure enablement, provenance standard references, and watermarking capability reference.

9. The method of claim 1, further comprising computing a completeness score and identifying missing required disclosure elements before public release.

10. The system of claim 2, wherein excluded dataset records identify an exclusion basis, approver, and evidence hash.

11. The method of claim 1, wherein synthetic data records identify seed data category, generation purpose, development phase, and relationship to the intended purpose of the system.

12. The system of claim 2, wherein contributor-aware adaptation records provide contributor or dataset lineage for fine-tuned adapters.

13. The method of claim 1, wherein a pre-execution governance layer blocks release of a model until the training data transparency evidence object reaches an approved state.

14. The system of claim 2, wherein structured memory stores statutory disclosure requirements and prior disclosure packages used by the compiler.

15. The method of claim 1, wherein every generation, approval, publication, and supersession event is recorded in an append-only governance audit log.

---

## Abstract

A California AI training data and frontier model transparency evidence compiler converts internal training data lineage into public and private disclosure packages. The compiler generates a release-bound evidence object containing model release identifiers, dataset summaries, private lineage references, synthetic data records, substantial modification state, public disclosure package state, frontier model safety references, content provenance records, and validation state. The system maps internal records to statutory disclosure fields, applies redaction rules, detects substantial modifications, computes completeness, and stores tamper-evident evidence. Optional embodiments integrate contributor-aware adaptation, pre-execution governance, risk drift states, structured memory, specialist routing, and append-only audit logs.

---

*AUMARA LLC · Peter Michael Viviani · AUMARA-J-PROV-001 · Provisional filed 2026*  
*Contact: peter@aumara.xyz*
