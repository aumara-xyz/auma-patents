# Per-Patient Surgical Erasure and Contribution Graph System for Medical AI

**Inventor:** Peter Michael Viviani  
**Assignee:** AUMARA LLC  
**Application Docket:** AUMARA-D-PROV-001  
**Filing Date:** Provisional filed 2026  
**Application Type:** Provisional Patent Application

---

## Title of Invention

Per-Patient Surgical Erasure and Contribution Graph System for Medical AI Training Data

---

## Summary of Invention

The present invention provides a per-patient surgical erasure and contribution graph system for medical AI. The system constructs a Patient Contribution Graph linking patient tokens to source records, surgical media segments, frames, clips, annotations, labels, embeddings, features, augmented samples, synthetic derivatives, training runs, adapter weights, checkpoints, evaluation sets, deployed model versions, and downstream outputs.

The system receives an erasure, restriction, revocation, or segmentation event and selects a deletion, quarantine, retraining, adapter regeneration, or machine unlearning action based on data type, legal basis, consent status, contribution type, model dependency, and operational risk. The system generates an erasure certificate with residual influence scores and retained-exception records.

Key innovations: (1) A graph-structured contribution model spanning the complete lineage from patient source records through all derivative machine learning artifacts. (2) Legal-scope-aware erasure planning that selects actions based on HIPAA designated record set status, 42 CFR Part 2 SUD record flags, consent basis, and applicable restrictions. (3) Residual influence verification using membership inference tests, influence functions, shadow models, and gradient attribution to produce a measured residual influence score. (4) Retained-exception record tracking with legal basis, retention period, and access controls. (5) Append-only governance audit log for all graph updates, erasure actions, and certificates.

---

## Claims

1. A computer-implemented method comprising: receiving medical data associated with a patient token; tracking derivative artifacts generated from the medical data during preprocessing, annotation, augmentation, embedding, training, validation, or deployment; constructing a patient contribution graph linking source record nodes, derivative artifact nodes, model artifact nodes, and contribution edges; receiving an erasure, restriction, or consent revocation event; selecting an action for affected graph nodes; executing or recording the action; and generating an erasure certificate.

2. A system comprising one or more processors and memory storing instructions that, when executed, cause the system to build and query a patient-to-model contribution graph for surgical video, imaging, EHR records, annotations, embeddings, synthetic derivatives, training runs, adapters, checkpoints, evaluation sets, and deployed model versions.

3. A non-transitory computer-readable medium storing instructions that, when executed, cause processors to verify machine unlearning by computing residual influence evidence after patient-specific deletion, quarantine, retraining, adapter regeneration, model retirement, or machine unlearning.

4. The method of claim 1, wherein source record nodes include designated record set flags, Part 2 flags, consent basis, restriction codes, deidentification state, storage URI, and content hash.

5. The system of claim 2, wherein derivative artifact nodes include frame, clip, patch, mask, annotation label, embedding, feature vector, augmented sample, synthetic sample, train split item, validation item, test item, prompt example, or evaluation case.

6. The method of claim 1, wherein contribution edges include direct copy, derived from, annotated from, embedded from, augmented from, synthetic seeded by, trained on, evaluated on, indexed in, merged into, or deployed as relationships.

7. The system of claim 2, wherein an erasure plan selects among delete, quarantine, mask, relabel, exclude future, retrain shard, regenerate adapter, machine unlearn, retire model, and retain exception actions.

8. The medium of claim 3, wherein residual influence evidence is computed using membership inference tests, influence functions, shadow models, pre/post output comparison, gradient attribution, adapter difference, or validation probes.

9. The method of claim 1, wherein retained exception records identify exception basis, retention period, access controls, and reviewer.

10. The system of claim 2, wherein probabilistic lineage is reconstructed using content hashes, timestamps, shard identifiers, dataset manifests, feature stores, or embedding index metadata.

11. The method of claim 1, wherein the erasure certificate includes affected node identifiers, selected actions, retained exceptions, residual influence score, validation tests, performance delta, and evidence hash.

12. The system of claim 2, wherein contributor-aware adaptation records provide per-contributor gradient or adapter attribution used to regenerate or unlearn a model artifact.

13. The method of claim 1, wherein a pre-execution governance layer blocks use of a restricted patient-linked artifact before model training or inference.

14. The system of claim 2, wherein a risk drift state machine monitors clinical performance or safety after patient-specific erasure.

15. The method of claim 1, wherein each graph update, erasure action, and certificate is stored in an append-only governance audit log.

---

## Abstract

A per-patient surgical erasure and contribution graph system constructs a patient-to-model graph for medical AI training data. The graph links patient source records, surgical video, imaging, annotations, embeddings, synthetic derivatives, training runs, adapters, checkpoints, evaluation artifacts, and deployed models. Upon erasure, restriction, or consent revocation, the system traverses affected nodes, selects deletion, quarantine, retraining, adapter regeneration, unlearning, retirement, or retained-exception actions, verifies residual influence, and generates an erasure certificate. Optional embodiments integrate contributor-aware adaptation, pre-execution governance, risk drift monitoring, structured memory, specialist routing, and append-only audit logs.

---

*AUMARA LLC · Peter Michael Viviani · AUMARA-D-PROV-001 · Provisional filed 2026*  
*Contact: peter@aumara.xyz*  
*Implementation details withheld pending non-provisional conversion.*
