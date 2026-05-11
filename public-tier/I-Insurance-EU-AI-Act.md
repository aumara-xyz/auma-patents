# Insurance AI Compliance Evidence System for EU AI Act Annex III High-Risk Insurance Decisions

**Inventor:** Peter Michael Viviani  
**Assignee:** AUMARA LLC  
**Docket:** AUMARA-I-PROV-001  
**Filing Date:** 2026  
**Application Type:** Provisional Patent Application

---

## Cross-Reference to Related Applications

This provisional application is related by common inventorship and common ownership to: CONTRIBUTOR-AWARE ADAPTATION (CAA), filed March 21, 2026; and RISK DRIFT SENTINEL (RDS), filed March 21, 2026, docket AUMARA-RDS-PROV-001. Related applications are identified for context only. The present invention does not require any component of the related applications to be practiced.

---

## Field of the Invention

The invention relates to computer-implemented compliance systems for insurance artificial intelligence, and more particularly to per-decision evidence generation, high-risk classification, technical documentation, human oversight logging, automated decision explanation, contestation routing, post-market monitoring, and operational resilience evidence for AI systems used in life insurance, health insurance, pricing, underwriting, eligibility, risk assessment, claims triage, and related insurance decisions.

---

## Background of the Invention

Regulation (EU) 2024/1689, the Artificial Intelligence Act, classifies certain AI systems as high-risk. Annex III includes AI systems used for risk assessment and pricing in relation to natural persons in the case of life and health insurance. High-risk AI obligations include risk management, data governance, technical documentation, record keeping, transparency, human oversight, accuracy, robustness, cybersecurity, and post-market monitoring. GDPR Article 22 separately addresses decisions based solely on automated processing that produce legal or similarly significant effects. DORA may apply to insurers and reinsurers as financial entities with operational resilience obligations.

Insurance pricing and underwriting systems already use actuarial models, machine learning models, external data, health data, lifestyle factors, claim histories, geospatial data, broker inputs, manual exceptions, and core policy administration systems. Existing actuarial governance does not automatically create EU AI Act technical documentation, per-decision high-risk evidence, protected/proxy feature analysis, human oversight records, GDPR Article 22 contestation trails, or DORA-linked incident and operational resilience evidence.

---

## Summary of the Invention

Disclosed is an Insurance AI Compliance Evidence System that produces an Insurance Decision Compliance Object for each relevant insurance pricing, underwriting, risk assessment, or eligibility decision. The object binds applicant or policy subject pseudonym, product type, jurisdiction, EU AI Act high-risk status, model identity, model version, input feature set, protected/proxy feature analysis, actuarial basis, decision outcome, premium effect, human oversight state, explanation state, contestation state, post-market monitoring state, and operational resilience linkages.

The invention may be implemented as a core insurance plugin, MLOps extension, actuarial governance module, GRC platform, SaaS compliance service, cloud service, or on-premise evidence appliance.

---

## Detailed Description of Preferred Embodiments

### 1. System Components

A **decision event collector** receives underwriting, pricing, renewal, eligibility, rider, exclusion, claim, or risk assessment events. A **high-risk classifier** determines whether the event involves life or health insurance risk assessment or pricing for a natural person.

A **feature analyzer** parses model inputs into feature categories: actuarial features, medical features, financial features, behavioral features, geolocation features, inferred health features, wearable-derived features, protected or sensitive features, and proxy features. The analyzer computes proxy relationships and records data source.

A **human oversight recorder** stores whether a decision was automated, human-reviewed, human-overridden, or human-approved. It records reviewer role, review timing, rationale, override reason, and customer-facing explanation state.

A **documentation generator** assembles technical documentation, deployer logs, risk management evidence, fundamental rights impact assessment support, GDPR Article 22 explanation support, adverse-decision explanations, contestation records, and post-market monitoring evidence.

### 2. Core Data Object: INSURANCE_DECISION_COMPLIANCE_OBJECT

The most important non-obvious object is the **INSURANCE_DECISION_COMPLIANCE_OBJECT** — a per-decision regulatory object linking actuarial basis, high-risk AI requirements, GDPR automated decision rights, and operational resilience.

Key fields:
- `decision_id`: UUID. Unique decision event.
- `subject_token`: STRING PSEUDONYMOUS. Natural person token.
- `jurisdiction_set`: ARRAY of EU member state, EEA, UK, or other relevant jurisdictions.
- `product_type`: ENUM {life, health, disability, long_term_care, accident, supplemental_health, other}.
- `decision_type`: ENUM {quote, underwriting_acceptance, underwriting_decline, premium_pricing, renewal, exclusion, rider, claim_triage, risk_score, eligibility}.
- `ai_role`: ENUM {sole_decision, substantial_assistance, recommendation, pricing_component, risk_scoring_component, explanation_only}.
- `eu_ai_act_status`: ENUM {annex_III_high_risk, potential_high_risk, exception_asserted, non_high_risk, out_of_scope}.
- `gdpr_article22_status`: ENUM {solely_automated_significant_effect, human_in_loop, explicit_consent, contract_necessity, authorized_by_law, not_applicable}.
- `input_feature_records`: ARRAY, each including feature_id, feature_name, value_bucket, source_system, data_category, sensitive_data_flag, protected_attribute_flag, **proxy_attribute_score** FLOAT 0.0-1.0, actuarial_basis_ref, and permitted_use_basis.
- `actuarial_basis_refs`: ARRAY of actuarial_table_id, study_ref, jurisdictional_filing_ref, approved_date, and hash.
- `decision_output`: outcome, premium_amount, pricing_delta, risk_score, confidence_score, reason_codes, and threshold_ref.
- `human_oversight_state`: required_flag, reviewer_id, reviewer_role, review_timestamp, review_latency_seconds, override_flag, override_reason, and **meaningful_review_score**.
- `explanation_state`: customer_notice_required, notice_template_id, explanation_generated_timestamp, factors_disclosed, factors_suppressed, and suppression_basis.
- `contestation_state`: contestation_available, contestation_channel, deadline, request_id, status ENUM {not_offered, offered, requested, under_review, resolved, escalated}, and outcome.
- `bias_and_proxy_metrics`: protected_group_test_refs, proxy_correlation_scores, adverse_impact_ratios, calibration_by_group, and mitigation_refs.
- `post_market_monitoring_refs`: metric_id, period, drift_score, complaint_count, incident_count, and corrective_action_ref.
- `dora_operational_link`: ict_service_ref, incident_ref, critical_provider_ref, resilience_test_ref, and outage_impact_flag.
- `evidence_hash` and `previous_decision_hash`: Hash chain fields.
- `signature_block`: Ed25519 digital signature.

### 3. High-Risk Classification Method

For each decision event, the system identifies whether the subject is a natural person, whether the decision concerns risk assessment or pricing, whether AI output materially influenced the decision, and whether profiling occurred. If the event falls within life or health insurance risk assessment or pricing, the object is tagged as Annex III high-risk unless a documented exception state is asserted with rationale, approver, supporting evidence, and exportable record.

### 4. Proxy and Actuarial Analysis

The system computes whether an input feature is sensitive, protected, or likely a proxy for a sensitive or protected attribute. The system may use controlled testing datasets, synthetic cohorts, statistical correlations, or external fairness test results. Each feature used to raise price, decline coverage, or impose an exclusion may be linked to an actuarial basis record.

### 5. Explanation and Contestation

The system generates decision explanations suitable for customer notice, internal review, regulator audit, or GDPR Article 22 contestation. Explanation detail may be filtered to avoid revealing trade secrets, fraud controls, or protected health data, while preserving reason codes and contestation routes.

---

## Claims

1. A computer-implemented method comprising: receiving an insurance decision event involving an artificial intelligence system; determining whether the event concerns risk assessment or pricing for a natural person in life insurance or health insurance; generating an insurance decision compliance object binding model state, input feature records, actuarial basis records, decision output, human oversight state, explanation state, and contestation state; and storing the object for technical documentation, audit, or regulator export.

2. A system comprising one or more processors and memory storing instructions that, when executed, cause the system to classify insurance AI decision events as high-risk, potential high-risk, non-high-risk, or exception asserted; analyze input features for sensitive attributes, protected attributes, and proxy attributes; link model outputs to actuarial basis records; and generate per-decision evidence packages.

3. A non-transitory computer-readable medium storing instructions that, when executed, cause processors to generate a customer explanation and contestation record for an insurance AI decision by selecting reason codes, determining disclosure filters, identifying contestation channels, and binding the explanation to a hashed decision compliance object.

4. The method of claim 1, wherein the decision event is a quote, underwriting acceptance, underwriting decline, premium pricing, renewal, exclusion, rider, claim triage, risk score, or eligibility decision.

5. The method of claim 1, wherein the input feature records include source system, data category, sensitive data flag, protected attribute flag, proxy attribute score, actuarial basis reference, and permitted use basis.

6. The system of claim 2, wherein proxy attribute analysis is performed using controlled testing datasets, synthetic cohorts, statistical correlation, or external fairness test results.

7. The method of claim 1, wherein the human oversight state includes reviewer role, review timestamp, review latency, override flag, override reason, and meaningful review score.

8. The medium of claim 3, wherein the disclosure filters identify factors disclosed to a customer and factors suppressed based on trade secret, fraud control, or protected health information basis.

9. The system of claim 2, further comprising post-market monitoring records aggregating drift, complaints, incidents, and corrective actions across decision compliance objects.

10. The method of claim 1, further comprising linking a decision compliance object to an operational resilience incident record when an ICT service failure affects pricing or underwriting.

11. The system of claim 2, wherein a high-risk exception assertion is stored with rationale, approver, supporting evidence, timestamp, and object hash.

12. The method of claim 1, wherein a risk drift state machine updates post-market monitoring state for the model associated with the decision event.

13. The system of claim 2, wherein a pre-execution governance layer prevents execution of a prohibited insurance AI use before a decision compliance object is generated.

14. The method of claim 1, wherein structured memory retrieval supplies jurisdiction-specific insurance AI obligations to the explanation or contestation module.

15. The system of claim 2, wherein each decision compliance object is stored in an append-only governance audit log.

---

## Abstract

An insurance AI compliance evidence system generates a per-decision compliance object for life or health insurance AI pricing, underwriting, eligibility, and risk assessment events. The object binds product type, jurisdiction, high-risk status, model state, input feature records, sensitive and proxy feature analysis, actuarial basis references, decision output, human oversight, explanation, contestation, post-market monitoring, and operational resilience links. The system supports EU AI Act Annex III high-risk classification, GDPR Article 22 explanation and contestation evidence, and regulator-ready technical documentation. Optional embodiments integrate risk drift states, pre-execution governance, structured memory, specialist routing, and append-only audit logs.

---

*AUMARA LLC · Peter Michael Viviani · AUMARA-I-PROV-001 · Provisional filed 2026*  
*Contact: peter@aumara.xyz*
