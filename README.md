# VERITAS — Self-Correcting, Evidence-First AI Research & Audit System

> **Research → Verify → Remember → Learn → Adapt → Research Better**

VERITAS is an AI research and auditing system designed to investigate an important problem in web-based AI research:

> **Can an AI research system use its own verification history to avoid repeating previously discovered mistakes?**

Instead of treating citations as the end of research, VERITAS introduces an independent **Auditor** whose findings become actionable feedback for future research.

---

## 🚀 Why VERITAS?

Modern AI research agents can:

- find information quickly
- summarize multiple web pages
- provide citations
- answer complex research questions

But a citation does not automatically mean that the cited source actually supports the claim.

A research agent may:

- cite a source that does not contain the claimed information
- misunderstand a source
- use outdated information
- rely too heavily on one source
- miss contradictions between sources
- repeat a previously discovered mistake

VERITAS addresses this with an independent verification loop.

```text
User Question
      │
      ▼
┌───────────────┐
│    ANALYST    │
│ Plan + Search │
│ + Synthesize  │
└───────┬───────┘
        │
        ▼
 Answer + Claims + Citations
        │
        ▼
┌───────────────┐
│    AUDITOR    │
│ Independent   │
│ Verification  │
└───────┬───────┘
        │
        ▼
SUPPORTED / UNSUPPORTED / CONTRADICTED
        │
        ▼
┌───────────────────────┐
│ Evidence-Aware Memory │
│ + Source History      │
└───────────┬───────────┘
            │
            ▼
   Better Future Research
