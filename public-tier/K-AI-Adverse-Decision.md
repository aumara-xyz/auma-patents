# AI Adverse Decision Explanation and Contestation Evidence Engine

**Inventor:** Peter Michael Viviani  
**Assignee:** AUMARA LLC  
**Docket:** AUMARA-K-PROV-001  
**Filing Date:** 2026  
**Application Type:** Provisional Patent Application

---

## Cross-Reference to Related Applications

This provisional application is related by common inventorship and common ownership to: CONTRIBUTOR-AWARE ADAPTATION (CAA), filed March 21, 2026; and RISK DRIFT SENTINEL (RDS), filed March 21, 2026, docket AUMARA-RDS-PROV-001. Related applications are identified for context only. The present invention does not require any component of the related applications to be practiced.

---

## Field of the Invention

The invention relates to computer-implemented compliance systems for automated and AI-assisted decisions, and more particularly to per-decision explanation, bias-audit evidence, adverse action documentation, consumer or applicant notice, appeal and contestation routing, human review, protected-class proxy analysis, and cross-jurisdiction evidence generation for employment, credit, housing, insurance, education, government benefits, legal services, and other consequential decisions.

---

## Background of the Invention

Automated decision systems are increasingly used in hiring, promotion, credit, lending, housing, insurance, education, government benefits, and similar domains. Legal authorities include the Equal Employment Opportunity Commission's application of Title VII and the ADA to algorithmic employment selection tools, New York City Local Law 144 regulating Automated Employment Decision Tools, Colorado's Anti-Discrimination in AI Law, California employment automated-decision regulations under the Fair Employment and Housing Act, the Fair Credit Reporting Act, the Equal Credit Opportunity Act, and state consumer protection statutes.

Existing systems include applicant tracking systems, HR platforms, credit scoring systems, loan origination systems, model monitoring dashboards, fairness toolkits, adverse action notice generators, and AI governance platforms. These systems do not usually preserve a single cross-law evidence object showing how an AI system contributed to a decision, which legal notice regime applied, which factors were adverse, what model score and threshold were used, whether protected-class proxies were implicated, whether bias-audit metrics existed, what explanation was given, how contestation was routed, and whether human review was meaningful.

The technical gap is binding an AI-assisted decision to jurisdiction-specific obligation atoms, model trace data, protected/proxy feature analysis, notice timing, appeal routing, human review state, and retention policy in a regulator-ready object.

---

## Summary of the Invention

Disclosed is an AI Adverse Decision Explanation and Contestation Evidence Engine. The engine receives a decision event, model trace, applicant or consumer context, jurisdictional context, protected/proxy feature analysis, score and threshold data, human review events, applicable legal obligation records, and outcome data. It generates an Adverse Decision Explanation Object that supports notices, explanations, contestation, human review, bias audit, regulator export, and litigation defense.

The system is architecture-agnostic and may be implemented in HR technology, lending platforms, housing platforms, education systems, insurance systems, benefits systems, GRC systems, model gateways, MLOps tools, or SaaS compliance infrastructure.

---

## Detailed Description of Preferred Embodiments

### 1. System Components

A **decision event collector** receives decisions from applicant tracking systems, HRIS systems, credit or lending systems, tenant screening systems, insurance systems, education systems, benefits systems, or other consequential decision platforms. A **model trace collector** receives model identity, model version, input feature records, score, confidence, threshold, ranking, reason codes, prompt or retrieval trace, and agent tool use where applicable.

A **legal obligation resolver** determines applicable laws and policy rules based on decision domain, jurisdiction, subject residence or work location, entity location, product type, decision effect, and system role. The resolver returns obligation atoms such as notice required, bias audit required, explanation required, adverse action notice required, consumer disclosure required, appeal required, human review required, record retention required, and regulator export required.

An **explanation generator** selects explanation factors from model traces and legally permissible disclosure templates. A **contestation router** creates channels for appeal, human review, correction, adverse action response, or data access. A **bias evidence module** aggregates decision objects for protected-class or proxy analysis, audit summaries, and adverse impact calculations.

### 2. Core Data Object: ADVERSE_DECISION_EXPLANATION_OBJECT

The most important non-obvious object is the **ADVERSE_DECISION_EXPLANATION_OBJECT** — a per-decision object that binds model contribution, legal obligation, explanation, appeal, and bias evidence.

Key fields:
- `decision_event_id`: UUID.
- `domain`: ENUM {employment, promotion, credit, lending, housing, insurance, education, government_benefits, legal_services, healthcare_access, other_consequential_decision}.
- `decision_subject_token`: STRING PSEUDONYMOUS.
- `jurisdiction_set`: ARRAY of applicable jurisdiction codes.
- `decision_outcome`: ENUM {approved, denied, ranked_lower, screened_out, referred, price_increased, benefit_reduced, condition_imposed, manual_review, other_adverse_effect}.
- `adverse_effect_flag`: BOOLEAN.
- `automated_system_role`: ENUM {sole_decision, substantial_factor, recommendation, ranking, screening, summarization, administrative_support}.
- `model_trace_ref`: model_id, model_version, deployment_id, score, threshold, confidence, rank_position, reason_codes, prompt_hash, retrieval_corpus_id, input_feature_hash, output_hash, and trace_uri.
- `feature_factor_records`: ARRAY, each including feature_id, feature_name_public, value_bucket, contribution_direction ENUM {positive, negative, neutral}, contribution_magnitude FLOAT, adverse_factor_flag, sensitive_attribute_flag, **proxy_attribute_score** FLOAT, data_source, and correction_available_flag.
- `applicable_obligation_atoms`: ARRAY, each including law_id, section_ref, obligation_type ENUM {pre_notice, post_notice, bias_audit, adverse_action_notice, explanation, appeal, human_review, correction, retention, regulator_export}, timing_rule, template_id, required_fields, and evidence_required.
- `notice_state`: notice_required, notice_template_id, generated_timestamp, delivered_timestamp, delivery_channel, delivery_proof_hash, and language_code.
- `explanation_state`: explanation_required, explanation_type ENUM {adverse_action, AEDT_notice, consumer_AI_notice, contestation_explanation, internal_audit, litigation_hold}, disclosed_factors, suppressed_factors, suppression_basis, and explanation_hash.
- `contestation_state`: contestation_required, channel, deadline, request_id, status ENUM {not_offered, offered, requested, acknowledged, in_human_review, resolved, escalated, closed}, reviewer_id, outcome, and corrected_decision_ref.
- `human_review_state`: required_flag, reviewer_role, reviewer_id, review_timestamp, review_latency_seconds, reviewer_inputs_seen, override_flag, rationale_text_hash, and **meaningful_review_score**.
- `bias_audit_link`: audit_id, audit_period, comparison_groups_available, adverse_impact_ratio, selection_rate_data_ref, audit_publication_ref, and limitation_notes.
- `retention_state`: retention_period, legal_hold_flag, deletion_eligible_date, and export_package_ref.
- `evidence_hash` and `previous_event_hash`: Hash chain fields.
- `signature_block`: Ed25519 digital signature.

### 3. Obligation Atom Compilation

The legal obligation resolver uses decision context to produce a set of obligation atoms. For example, an employment screening event for a New York City candidate may produce an AEDT notice atom and bias audit atom. A California employment decision may produce retention and discrimination evidence atoms. A credit denial may produce adverse action explanation atoms. A Colorado high-risk consequential decision may produce consumer notice, risk management, impact assessment, and appeal atoms.

### 4. Explanation Factor Selection

The system distinguishes internal explanation factors from public explanation factors. Internal factors may include model weights, protected-class test results, prompt traces, and fraud rules. Public factors may use reason codes, factor labels, value buckets, or grouped features. The system stores both the public explanation and the private trace so that future audits can verify what was disclosed and why.

### 5. Contestation and Human Review

When contestation is required or offered, the system creates a request path and binds it to the original decision object. Human review records identify what information the reviewer saw, how long review took, whether the reviewer overrode the model, and whether the review was meaningful.

---

## Claims

1. A computer-implemented method comprising: receiving an AI-assisted decision event for a decision subject; determining a decision domain and jurisdictional context; resolving one or more legal obligation atoms applicable to the decision event; generating an adverse decision explanation object binding model trace data, decision outcome, feature factor records, legal obligation atoms, notice state, explanation state, contestation state, and human review state; and storing the object for audit, notice, contestation, or regulator export.

2. A system comprising one or more processors and memory storing instructions that, when executed, cause the system to generate jurisdiction-specific notices and explanations for AI-assisted adverse decisions by selecting obligation atoms, public explanation factors, delivery templates, appeal channels, human review requirements, and retention rules.

3. A non-transitory computer-readable medium storing instructions that, when executed, cause processors to aggregate adverse decision explanation objects into a bias audit evidence package including selection rates, adverse impact ratios, model identifiers, audit period, notice proof, and limitation notes.

4. The method of claim 1, wherein the decision domain is employment, promotion, credit, lending, housing, insurance, education, government benefits, legal services, healthcare access, or another consequential decision.

5. The method of claim 1, wherein the model trace data includes model identifier, model version, score, threshold, confidence, rank position, reason codes, prompt hash, retrieval corpus identifier, input feature hash, output hash, and trace URI.

6. The system of claim 2, wherein each legal obligation atom includes law identifier, section reference, obligation type, timing rule, template identifier, required fields, and evidence required.

7. The method of claim 1, wherein feature factor records include contribution direction, contribution magnitude, adverse factor flag, sensitive attribute flag, proxy attribute score, data source, and correction availability.

8. The system of claim 2, wherein the explanation state stores disclosed factors, suppressed factors, suppression basis, and explanation hash.

9. The method of claim 1, wherein a contestation state references a corrected decision object generated after appeal or human review.

10. The medium of claim 3, wherein a bias audit evidence package links many decision explanation objects to an audit period and public audit summary.

11. The method of claim 1, wherein human review state includes reviewer inputs seen, review latency, override flag, rationale hash, and meaningful review score.

12. The system of claim 2, wherein a pre-execution governance layer prevents an adverse decision when required notice or contestation atoms are absent.

13. The method of claim 1, wherein a risk drift state machine escalates the model when adverse impact metrics or human oversight degradation exceed thresholds.

14. The system of claim 2, wherein structured memory retrieval provides jurisdictional obligation anchors to the resolver.

15. The method of claim 1, wherein the adverse decision explanation object is stored in an append-only governance audit log with a hash-linked prior event.

---

## Abstract

An AI adverse decision explanation and contestation evidence engine creates per-decision evidence objects for AI-assisted consequential decisions. The object binds decision outcome, domain, jurisdiction, model trace data, feature factors, legal obligation atoms, notice state, explanation state, contestation state, human review state, bias audit links, retention state, and evidence hashes. The system resolves jurisdiction-specific obligations, generates notices and explanations, routes appeals and human review, aggregates bias audit evidence, and exports regulator-ready packages. Optional embodiments integrate pre-execution governance, risk drift state machines, structured memory, specialist routing, and append-only audit logs.

---

*AUMARA LLC · Peter Michael Viviani · AUMARA-K-PROV-001 · Provisional filed 2026*  
*Contact: peter@aumara.xyz*
