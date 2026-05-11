# Risk Drift Sentinel: Automated Post-Market AI Compliance Monitoring

**Inventor:** Peter Viviani  
**Assignee:** AUMARA LLC  
**Application Docket:** AUMARA-RDS-PROV-001  
**Filing Date:** March 21, 2026  
**Application Type:** Provisional Patent Application

---

## Title of Invention

System and Method for Automated Post-Market Compliance Monitoring and Obligation-Triggered Risk Management of Artificial Intelligence Systems Using Multi-Source Regulatory Telemetry, Human Oversight Integrity Analysis, Formal Risk State Modeling, and Audit-Grade Evidence Provenance

---

## Summary of Invention

The present invention, designated the Risk Drift Sentinel, provides an automated post-market compliance monitoring system for deployed artificial intelligence systems. The system comprises five integrated subsystems:

(1) Multi-Source Telemetry Ingestion Layer ingesting operational data across seven signal categories each mapped to specific EU AI Act articles: human oversight interactions (Article 14), model performance and behavior (Articles 9 and 15), data pipeline telemetry (Article 10), infrastructure and security events (Article 15), documentation and configuration state (Articles 11 and 12), deployer transparency state (Article 13), and end-user transparency state (Article 50). Each event is tagged with a Regulatory Relevance Annotation.

(2) Human Oversight Monitor (HOM) — the most novel component — instruments review interfaces to detect ten oversight degradation signals: review velocity anomalies (rubber-stamping), override rate collapse, confidence-agreement divergence, justification degradation, session fatigue, reviewer concentration risk, automation complacency index, cumulative cross-session decision fatigue, anchoring effect from AI confidence displays, and explanation neglect.

(3) Regulatory Risk State Engine (RRSE) maintaining a formal state machine with thirteen defined compliance states: COMPLIANT_BASELINE, OVERSIGHT_DEGRADED, PERFORMANCE_DRIFTED, DATA_GOVERNANCE_BREACH, SECURITY_COMPROMISED, DOCUMENTATION_INVALID, TRANSPARENCY_FAILURE, CONFORMITY_EXPIRED, SCOPE_DRIFT, FUNDAMENTAL_RIGHTS_IMPACT, THIRD_PARTY_DEPENDENCY_FAILURE, COMPOUND_RISK, and SERIOUS_INCIDENT. Each state has defined entry conditions, mandatory obligation sets, and exit conditions.

(4) Obligation Trigger Engine (OTE) that upon state transitions automatically identifies applicable AI Act articles and paragraphs, generates structured obligation tickets with deadlines, initiates prescribed compliance workflows, and tracks completion lifecycle.

(5) Evidence Bundle Generator (EBG) producing audit-grade documentation with cryptographic provenance hash chains for tamper detection, formatted for EU AI Act Article 79 investigation readiness.

---

## Claims

### Independent Claims

1. A computer-implemented system for monitoring regulatory compliance of a deployed artificial intelligence system, comprising: (a) a telemetry ingestion layer configured to receive multi-source operational data across a plurality of signal categories including human oversight interactions, model performance and behavior, data pipeline telemetry, infrastructure and security events, documentation and configuration state, deployer transparency state, and end-user transparency state, and to annotate each telemetry event with a Regulatory Relevance Annotation comprising a mapping to one or more specific regulatory provisions at the article and paragraph level, a severity classification, and a correlation identifier linking related events across signal categories; (b) a human oversight monitor configured to instrument human review interfaces and detect oversight degradation patterns by analyzing at least review velocity anomalies, override rate collapse relative to measured system error rates, confidence-agreement divergence, justification quality degradation, within-session fatigue indicators, reviewer concentration risk, automation complacency index, cumulative cross-session decision fatigue, anchoring effect from AI confidence displays, and explanation neglect, wherein the detected degradation patterns are inputs to the risk state engine rather than standalone trust scores; (c) a risk state engine configured to maintain a formal regulatory compliance state model comprising a plurality of defined states including at least COMPLIANT_BASELINE, OVERSIGHT_DEGRADED, PERFORMANCE_DRIFTED, DATA_GOVERNANCE_BREACH, SECURITY_COMPROMISED, DOCUMENTATION_INVALID, TRANSPARENCY_FAILURE, CONFORMITY_EXPIRED, SCOPE_DRIFT, FUNDAMENTAL_RIGHTS_IMPACT, THIRD_PARTY_DEPENDENCY_FAILURE, COMPOUND_RISK, and SERIOUS_INCIDENT, wherein each state has defined entry conditions, mandatory obligation sets derived from specific regulatory provisions, and exit conditions requiring documented evidence of remediation; (d) an obligation trigger engine configured to, upon risk state transitions, automatically identify applicable regulatory obligations, generate structured obligation records with legally-mandated actions and deadlines, initiate prescribed compliance workflows, and track obligation completion through a defined lifecycle; and (e) an evidence bundle generator configured to produce audit-grade documentation linking triggering telemetry through risk state transitions through obligation activation through remediation actions, including cryptographic provenance metadata forming a hash chain enabling tamper detection.

2. A computer-implemented method for automated post-market compliance monitoring of a deployed artificial intelligence system, comprising the steps of: (a) continuously ingesting operational telemetry across a plurality of signal categories including human oversight interactions, model performance and behavior, data pipeline telemetry, infrastructure and security events, documentation and configuration state, deployer transparency state, and end-user transparency state; (b) annotating each ingested telemetry event with a Regulatory Relevance Annotation mapping the event to one or more specific regulatory provisions at the article and paragraph level; (c) analyzing human oversight interaction data to detect degradation by measuring at least review velocity anomalies, override rate collapse relative to expected system error rates, confidence-agreement divergence, justification quality changes, within-session fatigue indicators, reviewer concentration risk, automation complacency across confidence bins, cumulative cross-session decision fatigue, anchoring effects from AI confidence displays, and explanation neglect; (d) maintaining a regulatory compliance state model with defined states having entry conditions, mandatory obligation sets, and exit conditions, and computing state transitions when cross-signal fusion of analyzed telemetry breaches defined thresholds; (e) upon state transitions, automatically generating obligation records specifying legally-mandated actions with deadlines tiered by incident severity; and (f) producing evidence bundles with cryptographic provenance enabling tamper detection at any point in the chain.

3. A non-transitory computer-readable medium storing instructions that, when executed by one or more processors, cause the one or more processors to: (a) receive multi-source telemetry across seven signal categories and annotate each event with paragraph-level regulatory relevance metadata; (b) detect human oversight degradation through behavioral analysis of review interactions across at least ten measured signal categories; (c) maintain and update a formal regulatory compliance state machine with thirteen obligation-mapped states having defined entry conditions, mandatory obligation sets, and exit conditions; (d) automatically trigger compliance workflows responsive to state transitions, including tiered incident reporting deadlines; (e) generate tamper-evident evidence bundles with cryptographic provenance chains linking triggering telemetry through obligation activation through remediation; and (f) syndicate sanitized compliance alerts to authorized deployers when detected operational risks intersect with the system's documented instructions for use.

### Dependent Claims

4. The system of claim 1, wherein the human oversight monitor detects oversight degradation by comparing measured oversight metrics against baselines established during an initial calibration period specific to the monitored AI system, and wherein baselines are periodically recalibrated to account for legitimate operational changes.

5. The system of claim 1, wherein the risk state engine includes a compound risk state activated when two or more non-baseline risk states are simultaneously active, triggering elevated response obligations including incident assessment and potential system restriction or withdrawal.

6. The system of claim 1, wherein the obligation trigger engine generates incident report drafts conforming to regulatory reporting requirements, including pre-packaging information required for serious incident reports with applicable reporting timeframes.

7. The system of claim 1, wherein the evidence bundle includes provenance metadata comprising a cryptographic hash chain linking raw telemetry events through processing steps to generated obligation records and remediation evidence, enabling tamper detection at any point in the chain.

8. The method of claim 2, wherein annotating telemetry events uses a Regulatory Relevance Annotation schema that maps operational events to specific regulatory article and paragraph references, severity classifications, and correlation identifiers linking related events across signal categories.

9. The method of claim 2, wherein the compliance state model is parameterized by the AI system's risk classification category, intended purpose, and operating context, with default configurations for common high-risk categories including biometric identification, credit scoring, hiring systems, and critical infrastructure.

10. The method of claim 2, wherein the obligation trigger engine implements escalation logic that increases response urgency for unacknowledged obligations based on configurable time thresholds, and wherein unresolved serious incident obligations escalate to executive notification.

11. The method of claim 2, wherein the system monitors documentation validity by detecting model version changes, configuration mutations, or intended-use scope changes that render existing technical documentation non-representative of the current system state, triggering a DOCUMENTATION_INVALID risk state.

12. The medium of claim 3, wherein human oversight degradation detection comprises measuring the divergence between human reviewer override rates and the AI system's measured error rate, wherein a statistically significant gap between expected and actual override rates indicates oversight failure.

13. The system of claim 1, further comprising deployer transparency telemetry mapped to Article 13 and end-user transparency telemetry mapped to Article 50, wherein failure of transparency mechanisms triggers a TRANSPARENCY_FAILURE risk state with associated remediation obligations.

14. The system of claim 1, wherein the monitored AI system is a general-purpose AI model with systemic risk as defined under Article 55, and wherein the obligation trigger engine automatically generates structured incident reports for transmission to the AI Office upon detection of a systemic risk threshold breach.

15. The method of claim 2, wherein the obligation trigger engine implements tiered incident reporting deadlines: a maximum fifteen-day reporting window for standard serious incidents, a maximum ten-day reporting window for incidents resulting in death, and a maximum two-day reporting window for widespread infringements or serious disruption of critical infrastructure services, in accordance with Article 73(4).

16. The system of claim 1, further comprising a deployer-facing compliance interface configured to satisfy Article 26(5) obligations, wherein the obligation trigger engine syndicates sanitized, deployer-specific obligation tickets when detected operational risks intersect with the system's instructions for use.

17. The system of claim 1, wherein the risk state engine includes a SCOPE_DRIFT state triggered when runtime telemetry indicates the AI system is being used outside its intended purpose as defined in technical documentation.

18. The system of claim 1, wherein the risk state engine includes a THIRD_PARTY_DEPENDENCY_FAILURE state triggered when an upstream model provider fails to maintain compliance with applicable data governance, transparency, or systemic risk obligations.

19. The system of claim 1, wherein the risk state engine includes a downstream causal link analysis component that correlates AI system outputs with downstream operational metrics, and wherein statistical correlation between an AI output anomaly and a downstream critical failure triggers a SERIOUS_INCIDENT assessment workflow for indirectly caused incidents.

20. The system of claim 1, wherein the telemetry ingestion layer, risk state engine, and obligation trigger engine are further configured to map telemetry events and compliance states to regulatory obligations across a plurality of jurisdictions, enabling simultaneous compliance monitoring against multiple regulatory frameworks.

21. The system of claim 1, wherein a single system instance monitors a plurality of deployed AI systems, each maintaining an independent compliance state machine with system-specific parameterization.

22. The system of claim 1, wherein the evidence bundle generator employs Merkle tree structures for efficient integrity verification and selective disclosure of specific evidence paths, and wherein provenance chain timestamps are anchored to trusted timestamping authorities conforming to RFC 3161 for legally admissible temporal proof.

---

## Abstract

A system and method for automated post-market compliance monitoring of deployed artificial intelligence systems. The system ingests multi-source operational telemetry across seven signal categories (human oversight, model performance, data pipeline, infrastructure, documentation, deployer transparency, and end-user transparency), each annotated with paragraph-level regulatory relevance metadata. A Human Oversight Monitor instruments review interfaces to detect ten categories of oversight degradation including automation complacency, cumulative fatigue, and anchoring effects, feeding degradation signals into a formal compliance state engine rather than producing standalone trust scores. A Regulatory Risk State Engine maintains thirteen defined compliance states with mandatory obligation sets and exit conditions, including compound risk escalation and downstream causal link analysis for indirectly caused incidents. An Obligation Trigger Engine automatically identifies applicable regulatory requirements upon state transitions, initiates prescribed compliance workflows with tiered reporting deadlines, and syndicates sanitized alerts to deployers under Article 26(5). An Evidence Bundle Generator produces audit-grade documentation with Merkle tree provenance chains and RFC 3161 timestamp anchoring.

---

*AUMARA LLC · Peter Viviani · AUMARA-RDS-PROV-001 · Filed March 21, 2026*  
*Contact: peter@aumara.xyz*  
*Implementation details withheld pending non-provisional conversion.*
