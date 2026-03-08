# Laviq Trust Matrix

> **Audit our math.** This repository defines the scoring methodology and risk definitions used by Laviq.io to evaluate cryptographic posture in Linux environments.

## The Problem
Most security tools treat risk scores as a "black box." For Post-Quantum Cryptography (PQC) readiness, this isn't enough. Auditors need to know *why* an algorithm was flagged and which standard was used for the verdict.

## The Logic
The Trust Matrix maps observed **Execution Physics**—the runtime parameters captured by the Laviq agent—against established global standards, including:
- **NSA CNSA 2.0**
- **CCCS ITSM.40.001 (Canada)**
- **NIST PQC Standards**

## What's Inside
- **Algorithm Mapping:** How we categorize classical vs. quantum-resistant algorithms.
- **Parameter Sensitivity:** Why a 1024-bit key triggers a "Critical" verdict while 3072-bit is "Transitional."
- **Negotiation Verdicts:** Logic for flagging TLS/SSH protocol fallbacks.

## Why Open Source?
We provide this logic openly so that:
- **Security Engineers** can validate our findings against their own internal risk appetites.
- **Auditors** can cite the specific methodology used in a Laviq report.
- **The Community** can contribute new definitions as PQC standards evolve.

## Integration
The Trust Matrix is used by the `laviq-html-reporter` to color-code findings and suggest remediation timelines.

## License
Apache-2.0
