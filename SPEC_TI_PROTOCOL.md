# SPEC_TI_PROTOCOL.md: Infrastructure Token (IT) Protocol Design

## Summary
The Infrastructure Token (IT) is the project's cryptocurrency. Its issuance is directly tied to the value generated for the common good through the Proof of Benefit (PoB).

## 1. Mechanism: Proof of Benefit (PoB)

PoB replaces Proof-of-Work. Miners compete by dedicating compute power to governance-approved tasks.

### PoB Eligible Tasks (Public Goods)
IT rewards are only issued for the following computational contributions:
1.  **Open Model Training:** Compute dedicated to training open-source AI models (e.g., language models for the PSA, medical diagnostic models).
2.  **Data Curation:** Processing and cleaning large, public datasets (e.g., bias removal, source verification).
3.  **Protocol Auditing:** Running extensive simulations to test the security and stability of the **PoH** and the **IBC Protocol**.

### Decentralized Validation Process
1.  **Submission:** The miner submits the task output (e.g., the trained model binary) along with a verification hash.
2.  **Validator Consortium:** A randomized group of IT holders is selected for Decentralized Auditing.
3.  **Verification:** Validators approve that the output is **functional**, **open-source** (per license), and **meets the common good standard**.
4.  **Issuance:** Upon consensus, the IT reward is issued to the miner.

## 2. IT Governance

IT holders are responsible for the long-term health of the ecosystem.

* **Voting Power:** Voting power is proportional to the amount of IT held.
* **Key Decisions:** The community votes on:
    * The inclusion or exclusion of new task types eligible for PoB.
    * Adjustments to the IBC emission algorithm (only to maintain stability).
    * Major upgrades to the PSA and IT core code.

## 3. Issuance and Distribution (Initial Parameters - Subject to Funding)

* **Max Supply:** [To Be Defined]
* **Emission Rate:** Initially high to incentivize infrastructure building, with a periodic reduction (similar to Bitcoin's halving).
* **Fund Allocation:** 15% of the total emission will be reserved for the **Governance Treasury** to fund security audits and core development.
