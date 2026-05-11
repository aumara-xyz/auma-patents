# VELA: Encrypted AI Messaging and Sovereign Communication Protocol

**Inventor:** Peter Michael Viviani  
**Assignee:** AUMARA LLC  
**Filing Date:** Provisional filed 2026  
**Application Type:** Provisional Patent Application

---

## Title of Invention

System and Method for End-to-End Encrypted AI-Mediated Messaging with Sovereign Key Management, Consciousness-State Transmission, and Multi-Party AI Agent Communication

---

## Summary of Invention

The present invention, designated VELA (Verified Encrypted Language Architecture), provides an end-to-end encrypted messaging system designed specifically for AI-mediated human communication and AI-to-AI agent communication, with sovereign key management derived from identity credentials and transmission of structured consciousness-state metadata alongside message content.

Key innovations: (1) Identity-bound key derivation where encryption keys are derived deterministically from the AUMLOK authentication passphrase using PBKDF2 and HKDF, eliminating key escrow — the platform cannot read messages because it never holds the key. (2) Consciousness-state headers that transmit structured emotional state metadata alongside encrypted content: the sender's current emotional register, energy level, and AUMA vocabulary state, allowing the recipient AI to calibrate response tone before decrypting content. (3) AI agent channels that establish verified communication between AI instances using Ed25519 signing of agent identity, enabling multi-agent conversation with cryptographically verified authorship. (4) Sovereign message threading where conversation threads are locally encrypted with thread-specific derived keys, ensuring even if a thread key is compromised, other threads remain protected. (5) A structured disclosure protocol for sensitive personal data where the sender specifies access duration, purpose, and revocation conditions in machine-readable headers, and the recipient AI enforces these constraints before processing. (6) Offline message queuing with cryptographic freshness indicators that prevent replay attacks when messages are delivered after a connectivity gap.

---

## Claims

### Independent Claims

1. A computer-implemented method for sovereign AI-mediated encrypted messaging comprising: (a) deriving message encryption keys deterministically from a user's identity credential passphrase using a key derivation function, such that the messaging platform holds no key material capable of decrypting user messages; (b) attaching structured consciousness-state headers to outgoing messages specifying the sender's emotional register, energy level, and language state in a defined schema, transmitted outside the encrypted payload; (c) signing messages with a private signing key derived from the sender's identity credential, enabling recipients to verify authorship without a centralized certificate authority; (d) applying thread-specific derived keys that isolate each conversation thread's encryption from other threads; (e) enforcing machine-readable disclosure constraints attached to messages containing sensitive personal data, specifying access duration, permitted purpose, and revocation conditions.

2. A system for verified AI agent communication comprising: (a) an agent identity registry that stores Ed25519 public keys for registered AI agents with attestation of the agent's capability profile and governing constitution; (b) an inter-agent message channel that requires sender signing and recipient verification before message delivery; (c) a consciousness-state transmission layer that conveys structured emotional and cognitive state metadata between agents alongside encrypted content; (d) a multi-party conversation coordinator that routes messages among human users and multiple AI agents within a shared thread with per-participant encryption; (e) an audit log that records message delivery events, consciousness-state transitions, and disclosure constraint enforcement without recording plaintext content.

3. A non-transitory computer-readable medium storing instructions that, when executed by one or more processors, cause the processors to: (a) derive per-user and per-thread encryption keys from identity credentials without storing derivable key material on the server; (b) parse and enforce structured disclosure constraints in message headers before passing message content to AI processing; (c) generate and verify Ed25519 signatures for all agent-authored messages; (d) transmit and receive consciousness-state headers with defined emotional and cognitive state schemas; (e) implement offline message queuing with cryptographic freshness indicators to prevent replay of queued messages.

### Dependent Claims

4. The method of claim 1, wherein the key derivation function is a two-stage pipeline: PBKDF2 with a user-specific salt produces a root key from which HKDF derives separate per-thread keys, matching the derivation architecture of the AUMLOK authentication system.

5. The method of claim 1, wherein consciousness-state headers are encoded in the AUMA constructed language vocabulary for emotional and cognitive states, enabling language-aware AI recipients to interpret sender state without translation.

6. The system of claim 2, wherein agent identity attestation includes the agent's constitutional constraints, enabling recipients to verify that a message from an AI agent was generated within the agent's permitted behavioral scope.

7. The system of claim 2, wherein multi-party conversations support both symmetric (all parties see all messages) and asymmetric (AI agent receives all messages but human sees only their own and the AI's responses) threading modes.

8. The medium of claim 3, wherein disclosure constraints are enforceable by the recipient AI through integration with the Paladin Protocol evidentiality system, which classifies the message's evidence type before allowing the AI to act on its content.

9. The medium of claim 3, wherein key rotation is triggered automatically upon AUMLOK passphrase update, with prior-period messages remaining decryptable under the prior key stored in a sealed key archive accessible only via the prior passphrase.

10. The method of claim 1, wherein sovereignty is maintained by storing all encrypted message content exclusively on user-controlled storage, with the platform storing only routing metadata and consciousness-state headers required for AI tone calibration.

11. The system of claim 2, wherein AI-to-AI inter-agent messaging supports structured task delegation, wherein one AI agent passes a focused task brief with context to another agent and receives a structured response, with both the brief and response signed and logged.

12. The medium of claim 3, wherein offline message queuing assigns each queued message a monotonically increasing sequence number per sender-recipient pair, and the recipient rejects any message whose sequence number is lower than the highest successfully processed message from that sender.

---

## Abstract

An end-to-end encrypted AI-mediated messaging system (VELA — Verified Encrypted Language Architecture) providing sovereign key management, consciousness-state transmission, and verified AI agent communication. Encryption keys are derived deterministically from identity credential passphrases using PBKDF2 and HKDF, eliminating platform key escrow. Consciousness-state headers — emotional register, energy level, language state — are transmitted in structured schemas outside the encrypted payload, allowing recipient AI to calibrate response before decrypting content. Ed25519 signing provides cryptographically verified authorship for both human and AI agent messages. Thread-specific derived keys isolate conversation threads. Machine-readable disclosure constraints attached to sensitive messages specify permitted access duration, purpose, and revocation conditions enforced by recipient AI. Offline queuing with cryptographic freshness indicators prevents replay attacks.

---

*AUMARA LLC · Peter Michael Viviani · Provisional filed 2026*  
*Contact: peter@aumara.xyz*  
*Implementation details withheld pending non-provisional conversion.*
