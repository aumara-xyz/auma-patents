# DAEMON: Continuous Subconscious AI Processing

**Inventor:** Peter Michael Viviani  
**Assignee:** AUMARA LLC  
**Filing Date:** February 10, 2026  
**Application Type:** Provisional Patent Application

---

## Title of Invention

System and Method for Continuous Subconscious AI Processing Using Separate Lightweight Model for Background Cognitive Analysis, Autonomous Knowledge Document Management with Importance-Gated Write Permissions, Watermark-Based Completeness Guarantees, Identity-Critical Safety Gates, and Three-Layer Cognitive Architecture Implementing Biologically-Inspired Hippocampal Tagging for Memory Consolidation

---

## Summary of Invention

The present invention, designated DAEMON (Dynamic Autonomous Executive for Memory Organization and Notation), provides a continuous subconscious AI processing system implementing a three-layer cognitive architecture inspired by biological neuroscience.

Key innovations: (1) A three-layer cognitive architecture: Layer 1 (Conscious) uses a frontier conversation model for real-time interaction; Layer 2 (Subconscious/DAEMON) uses a separate lightweight model (~100x cheaper) running continuously as a background process every 5 minutes; Layer 3 (Deep Sleep) executes periodic consolidation. (2) Post-hoc analysis from a persistent message store — the subconscious layer reads ALL messages after they occur, capturing information the conscious layer may have missed due to context window pressure or multi-turn complexity. (3) Importance-gated write permissions with three tiers: autonomous write for routine knowledge (importance 6-8), review queue for identity-critical knowledge (importance >=9, touchesCore=true), and discard for insignificant information (importance <6). (4) Watermark-based completeness guarantee — the timestamp watermark advances ONLY after successful processing completion, ensuring daemon failure results in reprocessing rather than permanent data loss. (5) Biologically-inspired hippocampal tagging where the DAEMON IS the hippocampal tagging system, running during waking hours to tag experiences for significance. (6) Domain-organized living knowledge document system with automatic vector embedding generation for immediate semantic search integration. (7) Review queue storing suggested knowledge modifications with full context for informed approval or rejection.

---

## Claims

### Independent Claims

1. A computer-implemented method for continuous AI background processing comprising: (a) storing all conversational messages exchanged in a persistent database before any processing occurs; (b) operating a separate, lightweight AI model as a background process at configurable intervals that reads all messages since a timestamp watermark, extracts information worth storing long-term using structured importance scoring, and creates or updates knowledge documents autonomously based on importance thresholds; (c) routing modifications to identity-critical knowledge to a review queue rather than applying them autonomously, based on importance score and domain classification; (d) advancing the timestamp watermark only after all processing for the current cycle completes successfully, ensuring that daemon failure results in reprocessing rather than data loss; (e) autonomously creating new knowledge documents or updating existing documents in a structured domain-organized system with automatic vector embedding generation for semantic search integration.

2. A system for continuous AI knowledge maintenance comprising: (a) a persistent conversation message store wherein all messages are stored before any processing occurs, providing a complete record that the background process can analyze post-hoc; (b) a daemon process executing at configurable intervals using a lightweight AI model separate from the primary conversation model, the lightweight model being selected for analytical capability and cost efficiency rather than conversational quality; (c) a structured knowledge document system organized by functional domains with hierarchical path-based addressing, importance scoring, confidence ratings, creation metadata, and automatic vector embedding generation on document creation and update; (d) an importance-gated write permission system with at least three tiers: autonomous write for routine knowledge, review queue for identity-critical knowledge, and discard for insignificant information; (e) a watermark-based completeness mechanism wherein the daemon maintains a timestamp watermark that advances only after successful processing completion, guaranteeing that no conversational information is permanently lost; (f) a review queue storing suggested knowledge modifications with full context including source messages, suggested action, target document, suggested content, importance score, and reasoning, enabling informed approval or rejection.

3. A non-transitory computer-readable medium storing instructions that, when executed, cause a processor to: (a) implement a biologically-inspired cognitive architecture separating conscious processing (real-time conversation via frontier model), subconscious processing (continuous background analysis via lightweight model), and deep sleep processing (periodic consolidation) into three independent layers with different AI models optimized for each layer's specific cognitive function; (b) continuously analyze conversation messages after they occur using a lightweight model approximately 100x less expensive than the primary conversation model, extracting facts, decisions, emotional milestones, corrections, and commitments while filtering routine exchanges and transient information; (c) autonomously maintain a living knowledge document system that evolves with new information, creating new documents for novel facts and updating existing documents with new information appended with timestamps, all organized by functional domains; (d) enforce safety gates preventing autonomous modification of identity-critical knowledge by routing high-importance modifications to a review queue with full contextual justification; (e) guarantee processing completeness through watermark-based post-hoc analysis of a persistent message store, ensuring no information is permanently lost regardless of conscious-layer processing failures.

### Dependent Claims

4. The method of claim 1, wherein the lightweight AI model is configured with low temperature (<=0.3) for consistent analytical output and structured JSON output format for reliable programmatic parsing, with the model being independently replaceable without modifying the daemon architecture.

5. The method of claim 1, wherein the importance scoring uses a defined scale: 6 for contextually useful information, 7 for useful factual context, 8 for important facts, 9 for critical knowledge, and 10 for identity-defining information, with scores below 6 automatically discarded.

6. The method of claim 1, wherein the daemon prompt instructs the lightweight model to create memories only from user-provided information and never from the AI's own responses, preventing self-referential knowledge loops.

7. The system of claim 2, wherein documents created by the daemon carry a lower default confidence score (e.g., 0.8) than human-verified information (1.0), and the confidence score informs retrieval weighting in subsequent conversations.

8. The system of claim 2, wherein the deep sleep consolidation layer (KIRA integration) processes daemon-created documents by promoting frequently-accessed documents to higher entrenchment tiers, demoting low-access documents, merging related entries, and generating abstract summaries from accumulated specifics.

9. The system of claim 2, further comprising integration with a recursive self-improvement system (DOLLY) wherein high-quality daemon memory extractions validated by subsequent user confirmation become candidate training examples for model fine-tuning.

10. The medium of claim 3, wherein the daemon operates on free or near-free inference tiers of the lightweight model provider, enabling continuous cognitive maintenance at effectively zero marginal cost, with the system degrading gracefully on rate limiting by skipping the current cycle and retrying on the next interval.

11. The medium of claim 3, wherein knowledge document modifications by the daemon are tracked through a version control system (Neural Git integration) enabling rollback of incorrect daemon writes and audit trails of knowledge evolution over time.

12. The medium of claim 3, wherein the review queue for identity-critical modifications integrates with an evidentiality enforcement system (Paladin Protocol) requiring confidence classification distinguishing direct evidence from user statements, inference from conversational context, and extrapolation from indirect signals.

---

## Abstract

A continuous subconscious AI processing system (DAEMON — Dynamic Autonomous Executive for Memory Organization and Notation) implementing a three-layer cognitive architecture inspired by biological neuroscience. The conscious layer (frontier AI model) handles real-time conversation. The subconscious layer (separate lightweight model, ~100x cheaper) runs continuously as a background cron process at configurable intervals (default: every 5 minutes), reading all new conversation messages from a persistent store since a timestamp watermark, analyzing them for long-term significance using structured importance scoring, and autonomously creating or updating living knowledge documents organized by functional domains with automatic vector embedding generation. The deep sleep layer (periodic consolidation) performs deeper restructuring. An importance-gated write permission system enables autonomous document management for routine knowledge (importance 6-8) while queuing identity-critical modifications (importance >=9) for human or senior AI review with full contextual justification. Watermark-based processing guarantees completeness: the watermark advances only after successful processing, ensuring daemon failure results in reprocessing rather than data loss. The system implements biologically-inspired hippocampal tagging where the subconscious daemon tags experiences for significance during waking hours while the deep sleep layer consolidates tagged memories into permanent knowledge structures.

---

*AUMARA LLC · Peter Michael Viviani · Provisional filed February 10, 2026*  
*Contact: peter@aumara.xyz*  
*Implementation details withheld pending non-provisional conversion.*
