# SPEC_ISP_POH.md: Personal Sovereign AI (PSA) Proof of Humanity (PoH) Module Specification

## Summary
This document outlines the preliminary design for the Proof of Humanity (PoH) module, the key component that mitigates Sybil Attacks and ensures user privacy within the Capital of Capacity (CC) protocol.

## 1. Cryptographic Decision: Using zk-STARKs
The PoH module will utilize **Zero-Knowledge Proofs (ZKP)**, prioritizing **zk-STARKs**.

* **Justification:** zk-STARKs eliminate the need for a "Trusted Setup." Relying on a trusted setup is unacceptable for a system guaranteeing human sovereignty and dignity. Transparency and auditable security are the highest priority.

## 2. Phases of the Proof of Humanity (PoH)

### Phase A: Uniqueness Certification (PoH-S)
The goal is to verify that the user is a unique person.

* **Mechanism:** The PSA generates a unique private/public key pair on the user’s device. For *initial registration*, a **low-friction biometric validation** (e.g., iris scan) **is executed and verified exclusively on the local device**.
* **Outcome:** The verification result (an encrypted hash derived from the biometric data) is used as the **immutable cryptographic identifier** for the user’s IBC wallet. **The biometric data never leaves the device.**

### Phase B: Encrypted Activity Receipt Generation (PoH-A)
The goal is to verify active human engagement for IBC issuance without surveillance.

* **Mechanism:** When the user interacts with a Universal AI module (e.g., completes a 30-minute study session), the PSA runs a program to:
    1.  Verify the interaction locally.
    2.  Generate a zk-STARK proof asserting: **"Unique User X completed a valid activity of type 'Education' for a duration > T."**
* **Critical Constraint:** The content or nature of the activity (e.g., medical query keywords, lesson answers) **must never be part of the ZKP or leave the device**.

## 3. Technical Challenges

Initial development efforts must focus on:
1.  Optimizing zk-STARK proof generation for low-power mobile devices.
2.  Ensuring no hidden channel exists for data exfiltration during the certification process.
