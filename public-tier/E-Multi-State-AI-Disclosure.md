# Multi-State AI Disclosure Obligation Compiler

**Inventor:** Peter Michael Viviani  
**Assignee:** AUMARA LLC  
**Docket:** AUMARA-E-PROV-001  
**Filing Date:** 2026  
**Application Type:** Provisional Patent Application

---

## Cross-Reference to Related Applications

This provisional application is related by common inventorship and/or common ownership to: PALADIN PROTOCOL (U.S. Provisional No. 63/978,890, filed February 9, 2026); CONTRIBUTOR-AWARE ADAPTATION (CAA), filed March 21, 2026; RISK DRIFT SENTINEL (RDS), filed March 21, 2026, docket AUMARA-RDS-PROV-001; and TETRAHEDRON OF INTELLIGENCE, filed April 29, 2026, docket AUMARA-TETRA-PROV-001. Related applications are identified as commonly owned context and optional implementation disclosures only.

---

## Field of the Invention

The invention relates to computer-implemented legal and regulatory compliance infrastructure for artificial intelligence systems, and more particularly to runtime compilation of state-specific artificial-intelligence disclosure, notice, impact-assessment, appeal, retention, and regulator-export obligations into executable product instructions and per-transaction evidence records.

---

## Background of the Invention

United States artificial-intelligence regulation is fragmenting across states and use cases. Colorado enacted a statute directed to high-risk AI systems used in consequential decisions, effective June 30, 2026. Texas enacted the Texas Responsible AI Governance Act, effective January 1, 2026. Utah enacted an Artificial Intelligence Policy Act. California enacted and advanced multiple AI transparency laws. Additional states are introducing bills directed to employment, insurance, housing, education, healthcare, generative AI, companion chatbots, and synthetic media.

Existing privacy consent management systems can store notices and obtain consent. Feature-flag systems can display different screens based on jurisdiction. GRC systems can store policies and assign tasks. Such prior systems do not convert a live AI transaction into a jurisdiction-specific executable compliance bundle. They generally do not determine whether a specific AI interaction is a high-risk consequential decision, generative-AI interaction, employment automated-decision event, synthetic-content event, health-related AI interaction, minor-facing interaction, insurance decision, or frontier-model release event, and then bind that classification to legally required timing, disclosure language, human review, appeal routing, bias-audit linkage, retention period, and evidence package.

---

## Summary of the Invention

The invention provides a multi-state AI disclosure obligation compiler. In one embodiment, the system receives an AI transaction context, resolves applicable jurisdictions, classifies the AI use case, identifies legal obligation atoms, resolves conflicts among overlapping legal duties, generates runtime product instructions, injects or exposes disclosure and workflow requirements through an API, and stores a per-transaction evidence record.

The invention is architecture-agnostic. It may be implemented as a gateway, library, sidecar service, SaaS platform, GRC integration, model-serving plug-in, browser component, mobile SDK, HR-system plug-in, insurance-system plug-in, healthcare-system plug-in, education-system plug-in, or application-layer policy engine.

---

## Detailed Description of Preferred Embodiments

### 1. System Components

The system includes: (a) a **jurisdiction resolver** that receives signals such as declared residence, billing address, employment location, IP-derived region, device geolocation, user role, and contract governing-law fields, outputting one or more applicable jurisdictions with confidence scores; (b) an **AI-use classifier** that determines whether the transaction involves a consequential decision, employment screening, insurance pricing or underwriting, credit, lending, housing, healthcare, education, legal service, essential government service, biometric, minor-facing, companion, synthetic-content, training-data disclosure, frontier-model, or generative-AI interaction; (c) a **statutory obligation store** containing machine-readable legal obligation atoms, each including a law identifier, jurisdiction, section reference, effective date, actor type, covered system category, triggering condition, required action, timing, required evidence, retention rule, enforcement authority, penalty class, and conflict-priority metadata; (d) an **obligation atom compiler** that filters candidate atoms and resolves conflicts; (e) a **runtime instruction generator**; (f) a **disclosure template manager**; (g) an **appeal and human-review router**; (h) an **evidence recorder**; (i) a **retention engine**; and (j) a **regulator-export engine**.

### 2. Core Data Object: AI_OBLIGATION_BUNDLE_OBJECT

The most important non-obvious data object is the **AI_OBLIGATION_BUNDLE_OBJECT**. It binds a specific AI transaction to executable obligations and proof.

Key fields:
- `bundle_id`: UUID. Unique identifier for the compiled obligation bundle.
- `transaction_context_id`: UUID. Identifier for the AI interaction, decision, release, or workflow event.
- `subject_token`: Pseudonymous identifier for the affected consumer, applicant, employee, student, patient, insured, user, or household.
- `actor_role`: ENUM {developer, deployer, provider, employer, insurer, school, healthcare_provider, government_entity, platform, vendor, processor, controller, business_associate, other}.
- `system_role`: ENUM {foundation_model, frontier_model, generative_ai_service, high_risk_system, automated_decision_system, chatbot, companion_bot, synthetic_content_tool, model_gateway, decision_support_tool, other}.
- `jurisdiction_inputs`: Declared residence, billing state, employment state, IP region, device region, confidence weights, timestamp, and source metadata.
- `resolved_jurisdictions`: ARRAY of objects each containing jurisdiction_code, jurisdiction_type, basis, confidence_score, law_version, effective_date, and conflict_priority.
- `decision_context`: consequential_decision_flag, generative_interaction_flag, employment_ads_flag, insurance_flag, education_flag, healthcare_flag, minor_flag, synthetic_content_flag, companion_flag, biometric_flag, and automated_decision_level.
- `obligation_atoms`: ARRAY including atom_id, law_id, section_ref, jurisdiction_code, obligation_type, triggering_condition, actor_requirement, timing_requirement, template_id, evidence_fields_required, retention_rule_id, enforcement_authority, penalty_class, and status.
- `conflict_resolution`: conflicts_detected, controlling_rule_ids, superseded_rule_ids, rationale_code, human_review_required, and legal_review_flag.
- `runtime_actions`: ARRAY including action_type, target_surface, UI_location, API_endpoint, insertion_text_ref, timing, blocking_flag, acknowledgment_required, appeal_route_id, human_review_route_id, and expiration_condition.
- `execution_proof`: action_execution_timestamp, delivery_state, acknowledgment_timestamp, template_hash, screen_or_API_hash, operator_id, system_signature, and audit_log_ref.

One transaction_context_id may generate multiple AI_OBLIGATION_BUNDLE_OBJECT records when multiple jurisdictions apply.

### 3. Compilation Method

In one embodiment, the system: (a) receives an AI transaction context before, during, or after an AI interaction; (b) normalizes subject, actor, jurisdiction, AI-system, and decision-context attributes; (c) classifies the AI system and transaction against a taxonomy of covered state-law AI categories; (d) retrieves candidate legal obligation atoms; (e) filters candidate atoms by jurisdiction, effective date, actor role, covered system category, and triggering condition; (f) resolves conflicts and cumulative obligations; (g) generates runtime actions such as display notice, obtain acknowledgment, block workflow, enable appeal, route to human review, attach watermark metadata, retain evidence, publish public summary, or create regulator package; (h) delivers the runtime actions to the application or AI gateway; (i) captures proof of execution; and (j) stores the AI_OBLIGATION_BUNDLE_OBJECT for later audit, consumer request, litigation hold, or regulator export.

### 4. Conflict Resolution

When two or more state requirements apply, the system may select the strictest timing requirement, display the most specific disclosure, combine non-conflicting notices, suppress redundant statements, preserve separate statutory evidence fields, require human review where any applicable law requires it, or flag legal review when obligations conflict.

### 5. Runtime Injection

The generated runtime actions may be inserted into a web application, mobile application, HR platform, insurance platform, education system, health system, chatbot, API response, email, document, or synthetic-content manifest. The invention covers both visible disclosures and machine-readable disclosures.

---

## Claims

1. A computer-implemented method comprising: receiving an artificial-intelligence transaction context; resolving at least one applicable jurisdiction for the transaction context; classifying an artificial-intelligence system or use into a covered legal category; identifying one or more legal obligation atoms associated with the jurisdiction and category; compiling the legal obligation atoms into one or more runtime product actions; causing the runtime product actions to be executed by a software system; and storing proof of execution in an audit record.

2. A computer-implemented system comprising one or more processors and memory storing instructions that, when executed, cause the system to generate an AI_OBLIGATION_BUNDLE_OBJECT including jurisdiction inputs, resolved jurisdictions, artificial-intelligence system references, decision-context attributes, obligation atoms, runtime actions, execution proof, and retention-export state.

3. A non-transitory computer-readable medium storing instructions that cause one or more processors to convert state artificial-intelligence disclosure and decision obligations into executable user-interface, application-programming-interface, evidence-retention, appeal, and human-review actions for an artificial-intelligence transaction.

4. The method of claim 1, wherein the covered legal category includes a high-risk artificial-intelligence system used in a consequential decision.

5. The method of claim 1, wherein the covered legal category includes an employment automated decision system.

6. The method of claim 1, wherein the covered legal category includes a generative artificial-intelligence interaction requiring disclosure to a user.

7. The method of claim 1, wherein the covered legal category includes synthetic audio, image, video, or text content requiring a watermark, manifest, provenance signal, or disclosure.

8. The method of claim 1, further comprising resolving a conflict among multiple state obligations by selecting a stricter timing requirement, combining notices, preserving separate evidence fields, or flagging legal review.

9. The system of claim 2, wherein the runtime product actions include at least one of displaying notice text, injecting disclosure language, obtaining acknowledgment, enabling appeal, routing to human review, blocking an automated decision, retaining a screen proof, producing a bias-audit reference, or generating a regulator package.

10. The system of claim 2, wherein the execution proof includes a template hash, display or API hash, timestamp, actor identifier, system signature, and append-only audit-log reference.

11. The method of claim 1, wherein the obligation atoms include law identifiers, section references, effective dates, actor types, triggering conditions, timing requirements, evidence requirements, retention rules, enforcement authorities, and penalty classes.

12. The method of claim 1, further comprising updating the statutory obligation store when a new state artificial-intelligence law, regulation, attorney-general guidance, or rulemaking becomes effective.

13. The system of claim 2, wherein the obligation bundle is generated before execution of an AI action and is used to allow, block, modify, or reroute the AI action.

14. The method of claim 1, wherein a regulator-export package is generated from the stored proof of execution and associated decision records.

15. The system of claim 2, implemented using a structured memory field that stores legal obligation atoms, a specialist routing lattice that classifies obligation contexts, and an append-only governance audit log.

---

## Abstract

A computer-implemented multi-state artificial-intelligence obligation compiler receives an AI transaction context, resolves applicable jurisdictions, classifies the AI use, identifies state-law obligation atoms, compiles the atoms into runtime software actions, executes or causes execution of disclosures, notices, appeal paths, human-review routes, retention requirements, and regulator-export actions, and stores proof of execution. A core AI_OBLIGATION_BUNDLE_OBJECT binds jurisdiction inputs, resolved jurisdictions, AI system references, decision context, obligation atoms, runtime actions, conflict resolution, execution proof, and retention-export state. The system may be implemented as an AI gateway, SaaS compliance service, model-serving plug-in, SDK, GRC integration, or application-layer policy engine.

---

*AUMARA LLC · Peter Michael Viviani · AUMARA-E-PROV-001 · Provisional filed 2026*  
*Contact: peter@aumara.xyz*
