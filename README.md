# Tagalog-English LLM Evaluation Framework

An open-source quality assurance and benchmarking framework for evaluating Large Language Models (LLMs) on Tagalog-English localization, code-switching (Taglish), and instruction adherence.

## 🎯 Purpose & Scope
Evaluating regional languages and code-switched text requires structured, objective criteria. This framework establishes deterministic QA protocols, atomic pass/fail rubrics, and Chain-of-Thought (CoT) audit standards to minimize evaluator bias and improve model alignment.

## 🔑 Core Methodologies

### 1. Atomic Rubric Design
Subjective scoring (e.g., "natural tone") introduces reviewer drift. This framework breaks evaluations into single, independent pass/fail checks:
- **Lexical Constraints:** Strict adherence to target vocabulary without hallucinated terms.
- **Cultural & Contextual Fidelity:** Accurate localization of idioms and polite particles (*po/opo*).
- **Structural Integrity:** Deterministic output formatting (JSON schemas, exact key ordering).

### 2. CoT First-Break Audits
If a model reaches the correct final translation or output but uses faulty intermediate logic or grammar rules, the audit flags the failure at the exact point of divergence (*First-Break Identification*).

---

## 🛠️ Repository Content & Schemas

```text
├── rubrics/
│   └── atomic_qa_schema.json       # JSON Schema for deterministic evaluation
├── benchmarks/
│   └── cot_divergence_example.md   # Step-by-step logic audit showcase
└── README.md
