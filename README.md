# TrustEval

TrustEval is an evidence-based evaluation framework for AI systems.
It evaluates model quality, grounding, and trust signals strictly based on the
artifacts supplied at evaluation time.

TrustEval does not assume system maturity.
Evaluation depth increases automatically as instrumentation improves.

---

## What TrustEval Does

TrustEval evaluates AI systems across three evidence domains:

- **Quality** — output correctness, consistency, and calibration
- **Grounding** — alignment between outputs and retrieved context
- **Provenance** — verifiable linkage between outputs and underlying artifacts

All metrics are computed deterministically from supplied inputs.
No scores are inferred or estimated when evidence is missing.

---

## What TrustEval Does NOT Do

- TrustEval does not certify models
- TrustEval does not assert regulatory compliance
- TrustEval does not infer trust, grounding, or provenance without evidence
- TrustEval does not penalize systems for missing instrumentation

---

## Evidence-Driven Evaluation Model

TrustEval uses a single evaluation framework.
Metrics activate conditionally based on available evidence.

- Quality metrics are always computed
- Grounding metrics compute only when retrieval artifacts are provided
- Provenance metrics compute only when verifiable proofs are supplied

Missing evidence is treated as **Not Provided**, not as failure.

---

## Provenance in TrustEval

In TrustEval, provenance refers to verifiable linkage between:

- Model outputs
- Retrieved artifacts
- Cryptographic identifiers (hashes, manifests, Merkle roots, proofs)

Provenance metrics are computed only when such artifacts are explicitly supplied.
TrustEval does not estimate or approximate provenance.

---

## Coverage and Maturity

TrustEval reports both scores and coverage.

Coverage indicates which portions of the evaluation surface area were supported
by supplied evidence.

As systems mature and supply richer artifacts, TrustEval automatically produces
deeper and more complete evaluations.
