# Human-like Memory Reconstruction LLM Architecture

This repository proposes a hallucination-resistant memory reconstruction architecture for Large Language Models (LLMs).

## Core Idea

Instead of:

generation → answer

this architecture prioritizes:

question → retrieval → verification → reconstruction → generation

---

## Main Concepts

- Question Budget System
- Human-AI Collaborative Recall
- Memory Compression Hierarchy
- Source Log Revalidation
- Uncertainty-aware Retrieval
- Flow-based Memory Conflict Resolution

---

## Key Philosophy

Questions are treated as limited-cost resources for hallucination reduction.

The system shifts from:

"generate if uncertain"

to:

"ask, retrieve, verify, then generate"

---

## Included Documents

- Korean design document PDF
- Korean design document DOCX

---

## Current Status

Concept architecture / early-stage research design.

---

## Related Topics

- Hallucination Mitigation
- Agent Memory
- Interactive Retrieval
- Episodic Memory
- Persistent AI Systems

# Known Limitations

## 1. Model Dependency

The protocol does not behave identically across models.

Some models ask clarification questions.
Other models directly infer and answer.

## 2. Prompt-only Limitation

Prompt rules cannot reliably force question behavior.

A stronger implementation may require an external policy gate.

## 3. Narrative Completion Bias

LLMs often complete plausible narratives from partial evidence.

This can cause unsupported memory reconstruction.

## 4. Uncertainty Wording Problem

Adding words like "possibly" or "likely" may still preserve a hallucinated narrative.

## 5. Context Contamination

A model may use current conversation context instead of only the provided memory log.

## 6. Need for External Demo

A robust version should separate:

- memory retrieval
- candidate scoring
- question gating
- verification
- response generation
