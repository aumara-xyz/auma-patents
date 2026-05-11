# Paladin Protocol: Dual-Mode Evidentiality Enforcement System for AI Agent Safety

**Inventor:** Peter Michael Viviani  
**Assignee:** AUMARA LLC  
**Filing Date:** February 9, 2026  
**U.S. Provisional Application No.:** 63/978,890  
**Application Type:** Provisional Patent Application

---

## Title of Invention

System and Method for Dual-Mode Evidentiality Enforcement in AI Agent Systems Using Grammatical Evidence Classification, Typed Schema Validation at Execution Boundaries, Non-Forgeable Reference Resolution, and Constitutional Default Safe State

---

## Summary of Invention

The present invention, designated the Paladin Protocol, provides a dual-mode evidentiality enforcement system for AI agent safety. A constructed language (AUMA) whose grammatical particles simultaneously serve as natural language markers for human communication and as typed schema validators for AI agent execution forms the foundation.

Key innovations: (1) A grammar-to-schema-to-validator architecture where every knowledge claim justifying an action must declare its evidence type as a typed data structure. (2) Four evidence types with distinct validation requirements: direct evidence (server-resolvable proof references required), reported evidence (source attribution required), inferred evidence (traceable inference chains with cumulative confidence decay required), and intuited evidence (hard confidence ceiling enforced). (3) Negative evidentiality that distinguishes active search with coverage proof from absence of investigation. (4) A dual-gate authorization system requiring both capability and permission for every action, with opaque authorization references that are never output as raw tokens. (5) A constitutional default safe state that halts execution on any validation failure with no auto-resume, requiring human clearance. (6) A typed error taxonomy replacing vague failure modes with named, parseable violations. (7) An append-only, hash-chained audit log against which all proof references are resolved server-side.

Two modes: Agent Mode binds the grammar to typed validators with mandatory evidence requirements at execution boundaries. Conversation Mode operates the grammar as natural language with optional evidentiality. A single mode flag determines enforcement level, and the system operates only at the execution boundary, preserving natural conversation.

---

## Claims

### Independent Claims

1. A computer-implemented method for AI agent safety through dual-mode evidentiality enforcement comprising: (a) parsing AI agent output to identify grammatical evidentiality particles that declare the epistemic source type for each knowledge claim justifying an agent action; (b) resolving each evidence claim against typed data structure requirements specific to the declared evidence type; (c) validating proof references associated with each claim against an append-only, hash-chained audit log, wherein validation occurs server-side and proof references are never exposed as raw tokens; (d) applying type-specific requirements including: mandatory server-resolvable proof references for direct evidence, mandatory inference chains with cumulative confidence decay for inferred evidence, and hard confidence ceilings for intuited evidence; (e) requiring dual-gate authorization comprising both capability verification and permission verification for every agent action request; (f) enforcing a constitutional default safe state that halts all execution upon any validation failure, with no automatic resumption; (g) activating a constitutional default safe state that halts execution and requires human clearance upon any validation failure.

2. A system for AI agent safety through dual-mode evidentiality enforcement, comprising: (a) a grammar layer comprising a constructed language specification defining evidentiality particles that classify knowledge claims by epistemic source type; (b) a schema layer comprising typed data structures to which each evidentiality particle resolves, wherein each data structure specifies required proof fields based on evidence type; (c) an enforcement layer comprising server-side validation functions operating at an execution boundary, wherein a first function validates all evidence claims and authorization gates and a second function executes the requested action only upon successful validation; (d) an immutable audit log with hash-chained entries against which all proof references are resolved server-side; (e) a mode flag determining enforcement level, wherein a first mode operates the grammar as natural language with optional evidentiality and a second mode binds the grammar to typed validators with mandatory evidence requirements at the execution boundary; (f) a constitutional default safe state that activates on any validation failure, halting all execution and requiring human clearance to resume.

3. A non-transitory computer-readable medium storing instructions that, when executed by one or more processors, cause the one or more processors to: (a) parse AI agent output to identify grammatical evidentiality particles declaring epistemic source types for knowledge claims; (b) resolve proof references associated with each claim against an append-only, hash-chained audit log; (c) validate that evidence type declarations match the proof structures actually provided, applying type-specific requirements including confidence ceilings for intuited evidence and mandatory inference chains with cumulative confidence decay for inferred evidence; (d) enforce dual-gate authorization requiring both capability and permission for each action request; (e) block execution and activate a constitutional safe state upon any validation failure; and (f) record all validation decisions and safe state activations to the append-only audit log with hash chaining.

### Dependent Claims

4. The method of claim 1, wherein the inferred evidence type requires an inference chain comprising: premise identifiers referencing existing validated claims, natural language reasoning, and a confidence decay factor for each inference step, wherein total chain confidence equals the product of (1 minus decay) across all steps.

5. The method of claim 1, further comprising negative evidentiality classification, wherein the system distinguishes between: active negative evidence requiring proof of search scope, search method, and coverage metric with a server-resolvable search proof reference; and absence of evidence declaring that no investigation was conducted.

6. The method of claim 1, wherein evidence freshness is tracked using configurable validity windows for each evidence type, and evidence exceeding its validity window triggers a stale evidence warning requiring the agent to refresh evidence or mark claims as historical.

7. The system of claim 2, wherein the enforcement layer implements a Judge-Soldier pattern: the first function (submitIntent) operates as an atomic database mutation that validates all claims and authorization; the second function (executeIntent) operates as a database action that fires only upon successful validation; and the database runtime enforces that validation failure in the first function makes the second function unreachable within the same transaction scope.

8. The system of claim 2, wherein the typed error taxonomy comprises named errors with defined severity levels and prescribed agent actions, including: evidence species mismatch, broken inference chain, intuition overclaim, missing authorization gate, stale evidence, unauthorized action, and safety boundary violation.

9. The system of claim 2, wherein the opaque authorization reference is a server-side pointer that is never output as a raw token, key, or secret, and wherein raw token output by the agent constitutes a typed security violation distinct from a grammar error.

10. The system of claim 2, wherein authorization references include replay protection through scoping, time-bounding, and optional single-use constraints.

11. The medium of claim 3, wherein the constructed language serves simultaneously as a natural language for human communication and as a typed policy domain-specific language for AI agent execution, with a single grammar serving both purposes and a mode flag determining enforcement level.

12. The medium of claim 3, wherein the append-only audit log records tool outputs with tool_output_id and payload_hash, search operations with search_id and parameters_hash and result_hash, and all safe state activations, enabling complete auditability of agent decisions.

---

## Abstract

A dual-mode evidentiality enforcement system for AI agent safety uses a constructed language whose grammatical particles simultaneously serve as natural language markers for human communication and as typed schema validators for AI agent execution. In agent mode, every knowledge claim justifying an action must declare its evidence type (direct, reported, inferred, or intuited) as a typed data structure validated at an execution boundary against non-forgeable references in an append-only, hash-chained audit log. Direct evidence requires server-resolvable proof references. Inferred evidence requires traceable inference chains with mandatory cumulative confidence decay. Intuited evidence carries a hard confidence ceiling. Negative evidence distinguishes between active search with coverage proof and absence of investigation. A dual-gate authorization system requires both capability and permission for every action. A constitutional default safe state halts execution on any validation failure, with no auto-resume, requiring human clearance. The system operates only at the execution boundary, preserving natural conversation while making all side-effects formally verified. A typed error taxonomy replaces vague failure modes with named, parseable violations that enable automated error handling and escalation.

---

*AUMARA LLC · Peter Michael Viviani · U.S. Provisional No. 63/978,890 · Filed February 9, 2026*  
*Contact: peter@aumara.xyz*  
*Implementation details withheld pending non-provisional conversion.*
