# DORA Article 17-19 Self-Classifying AI Incident Evidence Engine

**Inventor:** Peter Michael Viviani  
**Assignee:** AUMARA LLC  
**Docket:** AUMARA-C-PROV-001  
**Filing Date:** 2026  
**Application Type:** Provisional Patent Application

---

## Cross-Reference to Related Applications

This provisional application is related by common inventorship and common ownership to: CONTRIBUTOR-AWARE ADAPTATION (CAA), filed March 21, 2026; and RISK DRIFT SENTINEL (RDS), filed March 21, 2026, docket AUMARA-RDS-PROV-001. These related applications are identified for context only. The present invention does not require any component of the related applications to be practiced.

---

## Field of the Invention

The invention relates to computer-implemented compliance infrastructure for artificial intelligence systems used by financial entities, and more particularly to automatic classification, deadline management, evidence capture, and regulator-package generation for ICT-related incidents involving AI models, AI agents, model-serving infrastructure, retrieval systems, critical third-party ICT service providers, and operational dependencies subject to the Digital Operational Resilience Act of the European Union.

---

## Background of the Invention

Regulation (EU) 2022/2554 (DORA) imposes obligations on financial entities for ICT risk management, incident management, classification, and reporting. Articles 17, 18, and 19 require financial entities to establish incident management processes, classify ICT-related incidents according to regulatory criteria, and report major ICT-related incidents through staged reports to competent authorities.

Existing tools include SIEM systems, cloud observability systems, ticketing systems, model observability tools, and GRC repositories. These systems record events or manage work, but they do not natively determine when an AI-specific failure mode becomes a DORA-classifiable ICT incident. An AI model may fail through drift, hallucination, corrupted retrieval, prompt injection, vendor model change, vector store poisoning, tool-calling loop, third-party cloud outage, privacy leakage, automated decision degradation, or human-overridden agent behavior. Conventional SOC tooling may see logs but not model semantics. Conventional MLOps tooling may see drift but not DORA materiality. Conventional GRC tooling may track policies but not start statutory reporting clocks based on live detection and classification events.

The regulatory gap is therefore technical: a financial entity must transform heterogeneous AI and ICT telemetry into a legally meaningful incident object, determine reportability under Article 18 criteria, start and manage Article 19 deadline clocks, assemble initial, intermediate, and final evidence packages, preserve third-party ICT provider causality, and later prove what was known at detection, what was known at classification, and why each report was or was not filed.

---

## Summary of the Invention

Disclosed is a self-classifying AI incident evidence engine for financial entities subject to DORA. The engine ingests AI telemetry, model-serving telemetry, agent traces, retrieval telemetry, cloud infrastructure telemetry, customer-impact metrics, transaction metrics, third-party ICT provider status, and security events. The engine constructs a DORA_AI_INCIDENT_EVIDENCE_OBJECT, evaluates incident criteria, determines whether the event is non-reportable, potentially reportable, major ICT-related, third-party-caused, cyber-threat-related, or serious-customer-impacting, and starts deadline clocks associated with initial notification, intermediate report, and final report obligations.

In one embodiment, the engine includes a detection normalizer, an AI-event interpreter, a DORA classification module, an impact metric aggregator, a third-party causality resolver, a deadline controller, a regulator package generator, and an append-only evidence ledger. The invention is architecture-agnostic and may be implemented as a SaaS platform, on-premise appliance, cloud-native service, model gateway, SIEM plugin, GRC plugin, MLOps extension, or air-gapped financial-sector compliance system.

---

## Detailed Description of Preferred Embodiments

### 1. System Components

A **detection normalizer** receives event streams from model-serving endpoints, agent orchestration frameworks, retrieval systems, vector databases, authentication services, cloud infrastructure, CI/CD pipelines, vendor APIs, ticketing systems, payment systems, trading systems, customer portals, and operational monitoring tools. The normalizer converts each source event into a normalized Evidence Source Record.

An **AI-event interpreter** classifies whether an event involves AI inference, AI training, fine-tuning, prompt processing, retrieval augmentation, agent tool use, model version change, prompt-template change, evaluation failure, drift signal, data-poisoning signal, safety-filter failure, automated decision failure, or human override.

A **DORA classification module** maps normalized events to classification criteria including service criticality, number or proportion of clients affected, duration, geographical spread, data loss, financial loss, reputational impact, transaction disruption, and involvement of a critical third-party ICT service provider.

A **deadline controller** creates a reporting clock set when detection or classification occurs. The clock set tracks initial notification, intermediate report, final report, customer notification, internal escalation, and supervisory-feedback deadlines.

A **regulator package generator** produces report packages that can be exported in human-readable, machine-readable, or authority-template formats. It generates an initial notification with known facts, an intermediate report with remediation status, and a final report with root cause, impact, duration, third-party causality, and lessons learned.

### 2. Core Data Object: DORA_AI_INCIDENT_EVIDENCE_OBJECT

The most important non-obvious object is the **DORA_AI_INCIDENT_EVIDENCE_OBJECT**. It binds AI-system state, ICT state, third-party causality, materiality criteria, and deadline clocks in a single tamper-evident object.

Key fields include:
- `incident_id`: UUID. Globally unique identifier.
- `entity_type`: ENUM {credit_institution, payment_institution, investment_firm, insurance_undertaking, reinsurance_undertaking, crypto_asset_service_provider, trading_venue, central_securities_depository, other_financial_entity}.
- `detection_timestamp` and `classification_timestamp`: RFC3339 datetimes.
- `classification_state`: ENUM {unclassified, monitoring, non_reportable, potentially_reportable, major_ict_incident, significant_cyber_threat, third_party_incident, customer_notification_required, final_closed}.
- `ai_involvement_type`: ARRAY of {inference_failure, model_drift, model_update, prompt_injection, retrieval_corruption, data_poisoning, safety_filter_failure, agent_tool_failure, autonomous_action_failure, human_override_failure, output_integrity_failure, privacy_leakage, other}.
- `ai_system_refs`: ARRAY of AI_SYSTEM_REF objects, each including model_id, model_version, deployment_environment, owner_team, vendor_id, and business_service_ref.
- `third_party_provider_refs`: Each includes provider_id, contract_id, critical_provider_flag, service_description, telemetry_source, incident_notice_ref, and causality_score FLOAT 0.0-1.0.
- `impact_metrics`: clients_affected, transactions_affected, transaction_value_eur, financial_loss_eur, duration_minutes, jurisdictions_affected, data_records_affected, and critical_services_affected.
- `dora_criteria_vector`: Booleans and scores for service_criticality, client_impact, duration, geographic_spread, data_loss, financial_loss, reputational_impact, economic_impact, and third_party_dependency.
- `deadline_clock_set`: Includes initial_notification_due, intermediate_report_due, final_report_due, customer_notice_due, clock_basis, and clock_status.
- `previous_object_hash` and `object_hash`: SHA-256 hash chain fields.
- `merkle_root`: Root binding this object to evidence source records and report packages.
- `signature_block`: Ed25519 digital signature over the canonical object.

### 3. Classification Method

The method receives a normalized event. The system identifies whether the event affects a regulated business service. If the event involves an AI system, the system enriches the event with model version, prompt template version, retrieval corpus version, agent tool policy, and vendor change history. The system then retrieves dependency graph data to determine affected ICT services and third-party providers. The system computes an impact vector and compares the vector to regulatory criteria. If the event crosses an entity-specific or regulator-defined threshold, the classification state changes and a reporting clock set is created.

In one embodiment, the classification module uses deterministic rules for hard criteria and learned classifiers for uncertain causality. In another embodiment, the module uses a confidence score and requires human confirmation before classifying an incident as major.

### 4. Deadline Method

When detection occurs, `detection_timestamp` is locked. When classification occurs, `classification_timestamp` is locked. The deadline controller computes due times for initial notification, outer initial reporting limit, intermediate report, final report, and customer communication. Each due time is represented as an absolute timestamp and as a status countdown.

### 5. Report Package Generation

The generator populates regulator templates from the evidence object. Fields unknown at initial notification are marked unknown with reason codes. Intermediate reports add remediation state, updated impact metrics, root-cause hypotheses, and affected services. Final reports add root cause, duration, losses, remediation, lessons learned, and third-party provider performance. The report package stores which facts were known at the time of submission to prevent later-created knowledge from contaminating historical evidence.

### 6. Tamper Evidence and Audit

The system may maintain an append-only ledger in which each evidence object, source record, clock update, classification decision, override, and report package is hashed and chained. The ledger may use Merkle roots, RFC 3161 timestamps, digital signatures, WORM storage, or equivalent tamper-evident mechanisms.

---

## Claims

1. A computer-implemented method comprising: ingesting telemetry from an artificial intelligence system and one or more information and communication technology systems of a financial entity; determining, by one or more processors, whether a detected event involving the artificial intelligence system affects a regulated financial service; generating a regulatory incident evidence object that binds artificial intelligence system state, information and communication technology service state, impact metrics, and one or more incident classification criteria; classifying the detected event into a reportability state; starting at least one regulatory reporting deadline clock based on a detection time or a classification time; and generating at least one report package from the regulatory incident evidence object.

2. A system comprising one or more processors and memory storing instructions that, when executed, cause the system to: normalize telemetry from model-serving infrastructure, agent traces, retrieval systems, cloud services, customer-impact systems, and third-party provider notices; correlate the telemetry to a financial service dependency graph; determine a major incident classification state; create a deadline clock set for staged regulatory reporting; and maintain a tamper-evident evidence ledger containing classification decisions, report packages, and source evidence.

3. A non-transitory computer-readable medium storing instructions that, when executed by one or more processors, cause the processors to produce an exportable DORA incident package by selecting evidence source records from an incident evidence object, populating staged report fields with facts known at a selected report time, and preserving unknown-field reason codes and evidence hashes.

4. The method of claim 1, wherein the artificial intelligence system state includes a model identifier, model version, prompt template version, retrieval corpus version, agent tool policy, and vendor update state.

5. The method of claim 1, wherein the impact metrics include number of clients affected, transactions affected, transaction value, financial loss, duration, geographic spread, data records affected, and critical services affected.

6. The method of claim 1, further comprising computing a third-party causality score linking a critical third-party ICT service provider to degradation of the artificial intelligence system or a dependent financial service.

7. The system of claim 2, wherein the deadline clock set includes due times for an initial notification, an intermediate report, a final report, and a customer notice.

8. The method of claim 1, wherein a human override of a classification state is stored with an override reason code, override user identity, timestamp, and object hash.

9. The system of claim 2, wherein the tamper-evident evidence ledger comprises hash-chained evidence objects and Merkle-rooted report packages.

10. The method of claim 1, wherein the report package distinguishes facts known at detection, facts known at classification, and facts learned after submission of a prior report.

11. The system of claim 2, wherein the system is implemented as a plugin to a security information and event management system, model observability system, governance risk and compliance system, or cloud monitoring system.

12. The method of claim 1, wherein classification state input is received from a risk drift state machine having formal states corresponding to compliance baseline, degraded oversight, drift, incident, and serious incident.

13. The system of claim 2, wherein the evidence ledger is implemented using an append-only governance audit log associated with a pre-execution governance framework.

14. The method of claim 1, wherein a structured memory system retrieves prior regulator feedback or prior incident resolutions through an anchor-based graph traversal and supplies the retrieved material to the classification module.

15. The system of claim 2, wherein specialist language model adapters are selected by a deterministic routing classifier to analyze incident subquestions without requiring the independent classification method to depend on any particular model architecture.

---

## Abstract

A self-classifying AI incident evidence engine ingests artificial intelligence telemetry, ICT telemetry, customer-impact metrics, and third-party provider notices for a financial entity. The engine generates a regulatory incident evidence object binding AI system state, ICT service state, impact metrics, DORA classification criteria, third-party causality, and reporting deadline clocks. The engine classifies reportability, starts staged reporting clocks, generates initial, intermediate, and final report packages, and preserves tamper-evident evidence showing what was known at detection, classification, and reporting. Optional embodiments integrate pre-execution governance, risk drift state machines, structured regulatory memory, specialist model routing, and append-only audit logs.

---

*AUMARA LLC · Peter Michael Viviani · AUMARA-C-PROV-001 · Provisional filed 2026*  
*Contact: peter@aumara.xyz*
