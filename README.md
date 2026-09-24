## Core Idea

VERITAS is an AI-powered research and auditing system designed to answer complex research questions using **live web sources** and an **independent AI Auditor** that verifies the claims and citations produced by the research agent.

Unlike a research system that simply generates an answer and stops, VERITAS introduces a verification and feedback loop:

```text
Research
   ↓
Verify
   ↓
Remember
   ↓
Learn
   ↓
Adapt
   ↓
Research Better

The central research question is:

> **Can an AI research system use its own verification history to avoid repeating previously discovered evidence failures?**

---

# 🌟 Why VERITAS?

Modern AI research systems can produce answers that *look correct* while containing:

* ❌ Incorrect factual claims
* ⚠️ Unsupported statements
* 🕒 Outdated information
* 🔗 Citation mismatches
* 📄 Over-reliance on a single source
* ⚔️ Conflicting information between sources
* 🔁 Repeated mistakes across different questions

A citation alone does not guarantee that the cited source actually supports the claim.

VERITAS addresses this through an independent verification and feedback loop.

```text
                 🤔 USER QUESTION
                        │
                        ▼
                 🧠 RESEARCH ANALYST
                        │
                        ▼
                 🌐 LIVE WEB RESEARCH
                        │
                        ▼
                 📚 EVIDENCE COLLECTION
                        │
                        ▼
                 📝 ANSWER + CITATIONS
                        │
                        ▼
                🛡️ INDEPENDENT AUDITOR
                        │
             ┌──────────┼──────────┐
             ▼          ▼          ▼
        🟢 SUPPORTED 🟡 UNSUPPORTED 🔴 CONTRADICTED
             │          │          │
             └──────────┼──────────┘
                        ▼
                🧠 EVIDENCE-AWARE
                     MEMORY
                        │
                        ▼
             📊 SOURCE HISTORY SIGNAL
                        │
                        ▼
             🔄 FUTURE RESEARCH
                        │
                        └──────────────► Better Research
```

---

# 🎯 Core Idea

VERITAS separates **research generation** from **evidence verification**.

```text
                    ┌─────────────────┐
                    │   USER QUERY    │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │     ANALYST     │
                    │                 │
                    │ Plan            │
                    │ Search          │
                    │ Retrieve        │
                    │ Analyze         │
                    │ Cross-check     │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │ Claims +        │
                    │ Evidence +      │
                    │ Citations       │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │     AUDITOR     │
                    │                 │
                    │ Independent     │
                    │ Verification    │
                    └────────┬────────┘
                             │
                ┌────────────┼────────────┐
                ▼            ▼            ▼
           SUPPORTED    UNSUPPORTED   CONTRADICTED
                │            │            │
                └────────────┼────────────┘
                             ▼
                    ┌─────────────────┐
                    │ Evidence-Aware  │
                    │ Memory          │
                    └────────┬────────┘
                             │
                             ▼
                    Future Research
```

The key idea is not simply having two agents.

The important part is:

```text
Audit Finding
     ↓
Memory Update
     ↓
Research Strategy Update
     ↓
Future Research
```

This feedback loop is what VERITAS is designed to investigate and measure.

---

# 👤 The Analyst

The **Analyst** performs the actual research.

It is responsible for:

1. Understanding the user's question
2. Identifying entities and required information
3. Creating a research plan before searching
4. Searching the live web
5. Retrieving relevant pages
6. Extracting evidence
7. Cross-checking important information
8. Identifying conflicts
9. Generating a cited answer

## Analyst Workflow

```text
User Question
      ↓
Question Understanding
      ↓
Research Planning
      ↓
Identify Sub-Questions
      ↓
Search Strategy
      ↓
Parallel Web Search
      ↓
Page Retrieval
      ↓
Evidence Extraction
      ↓
Cross-Checking
      ↓
Conflict Detection
      ↓
Answer Generation
      ↓
Citations
```

---

# 🛡️ The Auditor

The **Auditor** is an independent verification component.

It does not simply trust the Analyst's answer.

Its core question is:

> **"Does the cited evidence actually support this claim?"**

The Auditor independently opens the cited source and compares the source evidence with the claim.

For each important claim, it produces a verification status.

| Status                 | Meaning                                                   |
| ---------------------- | --------------------------------------------------------- |
| 🟢 **SUPPORTED**       | The cited evidence supports the claim                     |
| 🟡 **UNSUPPORTED**     | The cited evidence is insufficient to establish the claim |
| 🔴 **CONTRADICTED**    | The cited evidence conflicts with the claim               |
| ⚪ **MISSING CITATION** | An important claim has no suitable citation               |

---

# 🔎 Claim-Level Verification

### Example — Supported

```text
CLAIM

Company X opened 42 stores during the specified period.

SOURCE

Company X annual report.

AUDITOR

🟢 SUPPORTED
```

### Example — Contradicted

```text
CLAIM

Company X opened 42 stores.

SOURCE

Company X annual report → 31 stores.

AUDITOR

🔴 CONTRADICTED
```

### Example — Unsupported

```text
CLAIM

Company X opened 42 stores.

SOURCE

The cited article discusses Company X but
does not provide the number of stores opened.

AUDITOR

🟡 UNSUPPORTED
```

### Example — Missing Citation

```text
CLAIM

Company X became the market leader.

SOURCE

No suitable citation provided.

AUDITOR

⚪ MISSING CITATION
```

---

# 🚀 What Makes VERITAS Different?

The main innovation is **not simply Analyst + Auditor**.

The important part is what happens **after the audit**.

```text
             🔎 RESEARCH
                  │
                  ▼
             🛡️ VERIFY
                  │
                  ▼
          ⚠️ EVIDENCE FAILURE
                  │
                  ▼
            🧠 REMEMBER
                  │
                  ▼
       📊 UPDATE EVIDENCE HISTORY
                  │
                  ▼
       🔄 CHANGE FUTURE RESEARCH
                  │
                  ▼
       🎯 MEASURE THE DIFFERENCE
```

The system is designed so that an audit finding can become actionable information for later research.

This creates a feedback loop:

```text
Research
   ↓
Verification
   ↓
Audit Finding
   ↓
Memory Update
   ↓
Research Strategy Update
   ↓
Future Research
```

---

# 👤 Concrete User Workflow

A user simply enters a research question.

### Example

> **"Which Indian jewellery retailers opened the most stores in the last two years?"**

---

## Step 1 — 💬 User Input

```text
User Question
      ↓
Question Understanding
```

VERITAS identifies:

* Entities
* Time period
* Required facts
* Comparisons
* Potential ambiguities

---

# Step 2 — 🧠 Research Planning

The Analyst creates a research plan **before searching**.

```text
Question
   ↓
Break into sub-questions
   ↓
Identify required evidence
   ↓
Select search strategy
   ↓
Select source types
```

The plan can determine:

* Which entities need research
* Which facts need verification
* Which claims require multiple sources
* Which sources are likely to be primary
* Which searches can run in parallel

---

# Step 3 — 🌐 Parallel Web Research

Where appropriate, independent searches can run simultaneously.

```text
                 Research Plan
                      │
       ┌──────────────┼──────────────┐
       ▼              ▼              ▼
   🔎 Search A    🔎 Search B    🔎 Search C
       │              │              │
       ▼              ▼              ▼
   📄 Page A       📄 Page B       📄 Page C
       └──────────────┼──────────────┘
                      ▼
               Evidence Pool
```

Parallelism is used where the research tasks are independent.

This can reduce unnecessary sequential search time.

---

# Step 4 — 📚 Evidence Collection

VERITAS maintains the relationship between a claim and its evidence.

```text
Fact
 ↓
Source
 ↓
URL
 ↓
Source Metadata
 ↓
Evidence
 ↓
Claim
```

Relevant metadata can include:

* Source URL
* Source type
* Publication date
* Retrieved timestamp
* Evidence snippet
* Claim
* Audit status

---

# Step 5 — ✍️ Analyst Generates Answer

The Analyst produces:

```text
Answer
├── Claims
├── Evidence
├── Citations
└── Sources
```

Example:

> Company X opened 42 new stores during the specified period.

The claim is then passed to the Auditor for independent verification.

---

# Step 6 — 🛡️ Independent Audit

The Auditor receives the claims and citations.

```text
Claim
  ↓
Find cited source
  ↓
Open source
  ↓
Read relevant evidence
  ↓
Compare claim vs evidence
  ↓
Classify
```

The Auditor should independently inspect the source rather than simply accepting the Analyst's reasoning.

---

# Step 7 — ⚖️ Verification

Example:

```text
CLAIM

Company X opened 42 stores.

SOURCE

Company annual report.

AUDITOR

🟢 SUPPORTED
```

If the source instead says 31:

```text
CLAIM

Company X opened 42 stores.

SOURCE

Company annual report → 31 stores.

AUDITOR

🔴 CONTRADICTED
```

---

# ⚔️ Source Conflict Resolution

Real-world information can disagree.

Example:

```text
Source A → $50M
Source B → $55M
Source C → $50M
```

VERITAS does **not silently choose one value**.

Instead:

```text
⚠️ CONFLICT DETECTED
        ↓
Identify conflicting claims
        ↓
Compare sources
        ↓
Check dates
        ↓
Check source type
        ↓
Check context
        ↓
Check primary vs secondary evidence
        ↓
Resolve if possible
        ↓
Otherwise report uncertainty
```

Potential factors include:

* Source type
* Publication date
* Update date
* Primary vs secondary source
* Geographic applicability
* Product or version applicability
* Time period
* Customer segment
* Context of the claim

If the evidence cannot establish a clear answer, VERITAS reports the uncertainty instead of inventing certainty.

---

# 🧠 Evidence-Aware Memory

Traditional memory might store:

```text
Company X → CEO = Person Y
```

VERITAS stores the claim together with its evidence history.

```text
┌──────────────────────────────┐
│ CLAIM                        │
│ Company X → CEO → Person Y   │
├──────────────────────────────┤
│ SOURCE                       │
│ company.com                  │
├──────────────────────────────┤
│ SOURCE TYPE                  │
│ Primary                      │
├──────────────────────────────┤
│ AUDIT STATUS                 │
│ 🟢 SUPPORTED                 │
├──────────────────────────────┤
│ VERIFIED                     │
│ 2026-09-24                   │
├──────────────────────────────┤
│ AUDIT HISTORY                │
│ Previous verification        │
└──────────────────────────────┘
```

This means:

```text
Memory ≠ Truth
```

Instead:

```text
Memory
   =
Claim
+
Evidence
+
Source
+
Audit Status
+
Timestamp
+
History
```

This makes memory **evidence-aware** rather than simply fact-aware.

---

# 🔄 Memory Behavior

Different audit results can influence future research differently.

### 🟢 SUPPORTED

Previously supported evidence can be reused where appropriate, while considering freshness and context.

### 🟡 UNSUPPORTED

Previously unsupported evidence should not automatically be trusted.

The system can:

* Re-check the source
* Request corroboration
* Lower its research priority
* Avoid using it as sole evidence

### 🔴 CONTRADICTED

Previously contradicted evidence should not automatically be reused.

The system should seek fresh or stronger evidence.

### ⚪ MISSING CITATION

The system knows that the claim requires appropriate sourcing.

---

# 🔄 Self-Correction Example

## Question 1

> Who is the CEO of Company X?

The Analyst produces:

```text
Person A
```

The Auditor independently checks the evidence.

Result:

```text
🔴 CONTRADICTED
```

VERITAS stores:

```text
Company X → Person A
Status → CONTRADICTED
```

---

## Question 2

> What was Company X's CEO's previous role?

Instead of blindly reusing Person A:

```text
Memory Lookup
      ↓
Previous Information = CONTRADICTED
      ↓
❌ Do Not Blindly Reuse
      ↓
🌐 Fresh Research
      ↓
New Evidence
      ↓
Updated Answer
```

This is the intended **self-correction mechanism**.

The evaluation should verify whether this behavior actually occurs rather than assuming it does.

---

# 📊 Historical Source Reliability Signal

VERITAS can maintain a historical signal based on previous audit results.

Example:

```text
Source A
────────────────────────
Audited claims:       20
Supported:            17
Unsupported:           2
Contradicted:          1
```

This produces a:

> **Historical Source Reliability Signal**

This signal is **not treated as absolute truth**.

Instead, it can influence future research decisions.

```text
Research
   ↓
Audit
   ↓
Source Evidence History
   ↓
Historical Reliability Signal
   ↓
Future Source Prioritization
```

For example:

```text
Previously strong evidence
        ↓
Candidate for early inspection

Previous unsupported evidence
        ↓
Requires additional scrutiny

Previous contradictions
        ↓
Seek corroboration / fresh evidence
```

### Important Principle

```text
Historical reliability ≠ Truth
```

A source that has historically provided useful evidence can still publish incorrect or outdated information.

---

# 🧪 Auditor Canary Test

VERITAS also tests whether the Auditor can detect deliberately manipulated evidence.

This addresses an important failure mode:

> **What if the Auditor simply agrees with the Analyst?**

---

## Test 1 — Supported Evidence

```text
CLAIM:

Company X raised $50M.

EVIDENCE:

Company X announced a $50M funding round.

EXPECTED:

🟢 SUPPORTED
```

---

## Test 2 — Contradictory Evidence

Change only the evidence:

```text
CLAIM:

Company X raised $50M.

EVIDENCE:

Company X announced a $30M funding round.

EXPECTED:

🔴 CONTRADICTED
```

If the Auditor still returns:

```text
SUPPORTED
```

VERITAS identifies a weakness in the verification component.

---

# 🎯 Purpose of the Canary Test

The canary test checks whether the Auditor is actually verifying evidence rather than simply agreeing with the Analyst.

Desired behavior:

```text
Analyst says X
       ↓
Auditor opens source
       ↓
Auditor reads evidence
       ↓
Auditor compares evidence
       ↓
Auditor independently decides
```

Not:

```text
Analyst says X
       ↓
Auditor agrees with X
```

---

# 🔁 Self-Correction Feedback Loop

The central idea of VERITAS is that auditing is not the end of the pipeline.

```text
                 ┌─────────────────┐
                 │   USER QUERY    │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │     ANALYST     │
                 │ Plan + Research │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Claims +        │
                 │ Citations       │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │     AUDITOR     │
                 │ Independent     │
                 │ Verification    │
                 └────────┬────────┘
                          │
             ┌────────────┼────────────┐
             ▼            ▼            ▼
        SUPPORTED    UNSUPPORTED   CONTRADICTED
             │            │            │
             └────────────┼────────────┘
                          ▼
                 ┌─────────────────┐
                 │ Evidence-Aware  │
                 │ Memory          │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Research        │
                 │ Strategy Update │
                 └────────┬────────┘
                          │
                          ▼
                    Future Query
```

---

# 📈 Progressive Research Evaluation

VERITAS will be evaluated using **at least 8 progressively difficult research questions**.

Example progression:

```text
🟢 Q1 → Simple factual lookup
       ↓
🟢 Q2 → Multi-source factual question
       ↓
🟡 Q3 → Current information requiring live search
       ↓
🟡 Q4 → Reuse an entity from a previous question
       ↓
🟠 Q5 → Conflicting sources
       ↓
🟠 Q6 → Multi-step research
       ↓
🔴 Q7 → Deep evidence verification
       ↓
🔥 Q8 → Complex research requiring memory + adaptation
```

At least two questions should intentionally reuse previously researched entities.

This allows the evaluation to test whether research history actually affects later behavior.

---

# 📊 Evaluation Metrics

VERITAS measures more than just whether the final answer looks good.

---

## 🎯 Accuracy

Measure:

* Total claims
* Supported claims
* Unsupported claims
* Contradicted claims
* Citation coverage

### Claim Support Rate

```text
Supported Claims
──────────────────────── × 100
Total Audited Claims
```

---

## ⚠️ Unsupported Claim Rate

```text
Unsupported Claims
──────────────────────── × 100
Total Audited Claims
```

---

## 🔴 Contradiction Detection

Measure how often the Auditor correctly identifies claims contradicted by the cited evidence.

---

## 🔗 Citation Coverage

Measure how many important claims have suitable citations.

---

## 📚 Citation Correctness

Measure how often the cited source actually supports the claim.

---

## ⚪ Missing Citation Rate

Measure how many important claims lack suitable citations.

---

## 🧠 Memory Reuse

Measure how often previously researched entities or evidence are reused in later questions.

---

## 🔄 Adaptation

Measure whether Auditor findings actually change later research behavior.

Example:

```text
Before Audit:
Use Source B directly

Audit:
Source B unsupported

Memory:
Unsupported evidence recorded

Later Question:
Source B encountered again

Changed Behavior:
Request additional corroboration
```

---

## 💰 Cost

Track:

* Input tokens
* Output tokens
* Total tokens
* Estimated API cost
* Estimated cost in INR
* Cost per question
* Cumulative cost

---

## ⚡ Latency

Track:

```text
Total Research Time
Analyst Time
Auditor Time
Web Search Time
Page Retrieval Time
```

---

## 🧪 Auditor Canary Accuracy

Measure whether the Auditor catches deliberately modified evidence.

---

# 💰 Cost Tracking

Every research run should record:

```text
Question ID
Analyst Tokens
Auditor Tokens
Total Tokens
Estimated Cost
Latency
Number of Sources
Number of Claims
Supported Claims
Unsupported Claims
Contradicted Claims
Missing Citations
Memory Reuse
Adaptation Event
```

Example:

```text
Question 1
────────────────────────────

Analyst tokens:        2,140
Auditor tokens:        1,020
Total tokens:          3,160

Estimated cost:        ₹X.XX
Latency:               XX sec

Claims:                10

Supported:             8
Unsupported:           1
Contradicted:          0
Missing citation:      1
```

> The numbers above are an example format, not claimed experimental results.

---

# 📊 Example Evaluation Table

```text
| Q | Difficulty | Claims | Supported | Unsupported | Contradicted | Tokens | Cost | Latency |
|---|------------|--------|-----------|-------------|--------------|--------|------|---------|
| 1 | Low        | 8      | 7         | 1           | 0            | XXXX   | ₹X    | XXs     |
| 2 | Low        | 9      | 8         | 1           | 0            | XXXX   | ₹X    | XXs     |
| 3 | Medium     | 10     | 8         | 1           | 1            | XXXX   | ₹X    | XXs     |
| 4 | Medium     | 9      | 8         | 1           | 0            | XXXX   | ₹X    | XXs     |
| 5 | Medium     | 12     | 8         | 2           | 2            | XXXX   | ₹X    | XXs     |
| 6 | High       | 13     | 10        | 2           | 1            | XXXX   | ₹X    | XXs     |
| 7 | High       | 15     | 11        | 2           | 2            | XXXX   | ₹X    | XXs     |
| 8 | Very High  | 17     | 13        | 2           | 2            | XXXX   | ₹X    | XXs     |
```

> These are example placeholders for the evaluation format.

---

# 🏗️ Complete System Architecture

```text
                         👤 USER
                           │
                           ▼
                 ┌───────────────────┐
                 │   USER QUESTION   │
                 └─────────┬─────────┘
                           │
                           ▼
                 ┌───────────────────┐
                 │ QUESTION ANALYZER │
                 └─────────┬─────────┘
                           │
                           ▼
                 ┌───────────────────┐
                 │ RESEARCH PLANNER  │
                 └─────────┬─────────┘
                           │
              ┌────────────┼────────────┐
              ▼            ▼            ▼
        🌐 Web Search  📄 Page Fetch  🔎 Search 2
              │            │            │
              └────────────┼────────────┘
                           ▼
                 ┌───────────────────┐
                 │ EVIDENCE COLLECTOR│
                 └─────────┬─────────┘
                           │
                           ▼
                 ┌───────────────────┐
                 │   ANALYST AGENT   │
                 └─────────┬─────────┘
                           │
                           ▼
                  📝 ANSWER + CLAIMS
                           │
                           ▼
                 ┌───────────────────┐
                 │   AUDITOR AGENT   │
                 └─────────┬─────────┘
                           │
                ┌──────────┼──────────┐
                ▼          ▼          ▼
             🟢 PASS    🟡 WARN    🔴 FAIL
                │          │          │
                └──────────┼──────────┘
                           ▼
                 ┌───────────────────┐
                 │  CONFLICT ENGINE  │
                 └─────────┬─────────┘
                           │
                           ▼
                🧠 EVIDENCE MEMORY
                           │
              ┌────────────┴────────────┐
              ▼                         ▼
       📚 CLAIM MEMORY           📊 SOURCE HISTORY
              │                         │
              └────────────┬────────────┘
                           ▼
                  🔄 FEEDBACK ENGINE
                           │
                           ▼
                  FUTURE RESEARCH
                           │
                           └──────────► 🔁
```

---

# 🖥️ High-Level Technology Architecture

```text
┌─────────────────────────────────────────────┐
│              🎨 FRONTEND                   │
│                                             │
│ React + TypeScript + Material UI            │
│                                             │
│ • Research Dashboard                        │
│ • Research History                          │
│ • Evidence Viewer                           │
│ • Audit Results                             │
│ • Memory Explorer                           │
│ • Analytics                                 │
└──────────────────────┬──────────────────────┘
                       │ REST API
                       ▼
┌─────────────────────────────────────────────┐
│              ⚡ BACKEND                    │
│                                             │
│ Python + FastAPI + Pydantic                 │
│                                             │
│ • Research API                              │
│ • Analyst Orchestration                     │
│ • Auditor Orchestration                     │
│ • Evidence Processing                       │
│ • Memory Management                         │
│ • Conflict Resolution                       │
└──────────────┬──────────────────┬───────────┘
               │                  │
               ▼                  ▼
       ┌──────────────┐   ┌──────────────┐
       │ PostgreSQL   │   │    Redis     │
       │              │   │              │
       │ Claims       │   │ Cache        │
       │ Sources      │   │ Sessions     │
       │ Audits       │   │ Short State  │
       │ Research     │   │              │
       └──────────────┘   └──────────────┘
               │
               ▼
┌─────────────────────────────────────────────┐
│              🤖 AI LAYER                   │
│                                             │
│ • Analyst LLM                               │
│ • Auditor LLM                               │
│ • Structured Outputs                        │
│ • Tool Calling                              │
│ • Research Planning                         │
│ • Claim Verification                        │
└──────────────────────┬──────────────────────┘
                       │
                       ▼
┌─────────────────────────────────────────────┐
│              🌐 WEB LAYER                  │
│                                             │
│ • Search                                    │
│ • Page Retrieval                            │
│ • Content Extraction                        │
│ • Source Metadata                           │
└─────────────────────────────────────────────┘
```

---

# 📁 Suggested GitHub Repository Structure

```text
VERITAS/
│
├── 📁 backend/
│   ├── 📁 api/
│   │   ├── routes.py
│   │   └── schemas.py
│   │
│   ├── 📁 agents/
│   │   ├── analyst.py
│   │   ├── auditor.py
│   │   └── prompts.py
│   │
│   ├── 📁 research/
│   │   ├── planner.py
│   │   ├── search.py
│   │   ├── fetcher.py
│   │   └── extractor.py
│   │
│   ├── 📁 memory/
│   │   ├── evidence_memory.py
│   │   ├── claim_memory.py
│   │   └── source_history.py
│   │
│   ├── 📁 verification/
│   │   ├── claim_checker.py
│   │   ├── conflict_resolver.py
│   │   └── canary.py
│   │
│   ├── 📁 database/
│   │   ├── models.py
│   │   └── database.py
│   │
│   └── main.py
│
├── 📁 frontend/
│   ├── 📁 src/
│   │   ├── 📁 components/
│   │   ├── 📁 pages/
│   │   ├── 📁 services/
│   │   ├── 📁 types/
│   │   └── App.tsx
│   │
│   ├── package.json
│   └── tsconfig.json
│
├── 📁 evaluation/
│   ├── questions.json
│   ├── run_evaluation.py
│   ├── metrics.py
│   └── results/
│
├── 📁 tests/
│   ├── test_analyst.py
│   ├── test_auditor.py
│   ├── test_memory.py
│   ├── test_conflicts.py
│   └── test_canary.py
│
├── 📁 logs/
│   └── ai-session-logs/
│
├── 📁 docs/
│   ├── architecture.md
│   ├── evaluation.md
│   └── decisions.md
│
├── .env.example
├── .gitignore
├── docker-compose.yml
├── requirements.txt
├── README.md
└── DECISIONS.md
```

---

# 📈 Evaluation Strategy

VERITAS will be evaluated using **at least eight progressively difficult questions**.

```text
🟢 Q1 → Basic factual research
       ↓
🟢 Q2 → Multi-source research
       ↓
🟡 Q3 → Current/live information
       ↓
🟡 Q4 → Entity reuse from previous question
       ↓
🟠 Q5 → Source conflict
       ↓
🟠 Q6 → Multi-step research
       ↓
🔴 Q7 → Deep evidence verification
       ↓
🔥 Q8 → Full-system challenge
```

At least two questions should intentionally reuse entities or information from previous questions.

This allows the evaluation to test whether research history actually affects later behavior.

---

# 🎯 Evaluation Dimensions

## Accuracy

* Claim support
* Citation correctness
* Contradiction detection
* Missing citation detection

## Research Quality

* Research planning
* Source diversity
* Primary-source usage
* Cross-checking
* Conflict handling

## Memory

* Entity reuse
* Evidence reuse
* Audit history reuse
* Source history

## Adaptation

* Re-verification behavior
* Source prioritization changes
* Search strategy changes
* Response to previous audit failures

## Performance

* Search count
* Pages retrieved
* Latency
* Parallelism

## Cost

* Analyst tokens
* Auditor tokens
* Total tokens
* Estimated cost
* Cost per question

---

# 📊 Example Evaluation Dashboard

```text
╔════════════════════════════════════════════╗
║             VERITAS ANALYTICS              ║
╠═══════════╦═══════════╦══════════╦═════════╣
║ Questions ║  Claims   ║ Verified ║  Cost   ║
║     8     ║    XX     ║    XX    ║  ₹XX    ║
╠═══════════╩═══════════╩══════════╩═════════╣
║                                            ║
║  🟢 Supported        XX                    ║
║  🟡 Unsupported       X                    ║
║  🔴 Contradicted      X                    ║
║  ⚪ Missing Citation  X                    ║
║                                            ║
║  Citation Coverage: XX%                    ║
║  Average Latency:   XX sec                 ║
║  Total Tokens:      XX,XXX                 ║
║                                            ║
║  Memory Reuse:      XX%                    ║
║  Adaptation Events: XX                     ║
║  Canary Test:       PASS / FAIL            ║
║                                            ║
╚════════════════════════════════════════════╝
```

> Values shown above are placeholders for actual evaluation results.

---

# 🧪 Example End-to-End Run

## 👤 User

> "How much funding did Company X raise in 2025?"

---

## 🔎 Analyst

Searches:

```text
Source A → $50M
Source B → $50M
Source C → $45M
```

---

## 📝 Analyst Answer

> Company X raised $50M in 2025.

---

## 🛡️ Auditor

```text
Source A → 🟢 Supports
Source B → 🟢 Supports
Source C → ⚠️ Conflicting
```

---

## ⚖️ Conflict Engine

The system compares:

* dates
* source type
* source context
* primary vs secondary evidence

If applicable primary evidence establishes the value, the system can use it while preserving the conflict information.

---

## 🧠 Memory

```text
Company X
Funding 2025
Value → $50M

Audit Status:
SUPPORTED

Conflict:
Yes

Supporting Source:
Source A
```

---

## 🔄 Future Question

A later question about Company X retrieves this information but also knows:

```text
⚠️ Previous source conflict existed.
```

The system can therefore decide whether fresh verification is appropriate.

---

# 🧪 Failure Modes to Investigate

VERITAS should explicitly test where the system can fail.

## Analyst Failure

The Analyst produces an unsupported claim.

## Citation Failure

The citation exists but does not support the claim.

## Source Failure

A source contains outdated or incorrect information.

## Auditor Failure

The Auditor incorrectly marks unsupported evidence as supported.

## Memory Failure

The system stores an incorrect or poorly contextualized conclusion.

## Adaptation Failure

The Auditor detects an error, but future research does not change.

## Conflict Failure

The system encounters conflicting sources and resolves them incorrectly.

## Freshness Failure

Previously correct information is no longer current.

---

# 🔬 The Most Important Experiment

The strongest experiment in VERITAS is:

> **Can the system learn from its own audit history?**

The experiment:

```text
             FIRST RESEARCH
                   │
                   ▼
             Analyst Answer
                   │
                   ▼
                Auditor
                   │
                   ▼
             Error Detected
                   │
                   ▼
             Memory Update
                   │
                   ▼
             SECOND RESEARCH
                   │
                   ▼
        Does behavior change?
                   │
             ┌─────┴─────┐
             ▼           ▼
            YES          NO
             │           │
             ▼           ▼
       Adaptation     No Adaptation
       Demonstrated
```

This directly tests the central idea of VERITAS.

---

# 📈 Measuring Adaptation

For each adaptation event, record:

```text
Previous Behavior
       ↓
Auditor Finding
       ↓
Memory Update
       ↓
New Research Behavior
       ↓
Observed Outcome
```

Example:

```text
BEFORE

Analyst:
Uses Source B as primary evidence.

AUDIT

Auditor:
Source B does not support the claim.

MEMORY UPDATE

Source B:
Unsupported evidence recorded.

LATER QUESTION

Analyst encounters Source B again.

CHANGED BEHAVIOR

Analyst:
Requests additional corroboration.
```

This provides a measurable definition of self-correction.

---

# 📝 Decision Log

Important architecture decisions should be recorded in:

```text
DECISIONS.md
```

Example:

```text
Decision:
Use an independent Auditor rather than relying on
a single verification prompt.

Reason:
The system should separate research generation
from evidence verification.
```

```text
Decision:
Store audit history with claims.

Reason:
Future research should know not only what was
previously found, but how the evidence performed
when it was checked.
```

```text
Decision:
Use historical source performance as a signal,
not absolute truth.

Reason:
Past source performance does not guarantee
future correctness.
```

---

# 🧪 Testing Strategy

## Analyst Tests

Test whether the Analyst can:

* Create a research plan
* Perform live searches
* Retrieve relevant pages
* Extract evidence
* Generate citations
* Cross-check important claims
* Identify potential conflicts

---

## Auditor Tests

Test whether the Auditor can:

* Verify supported claims
* Detect unsupported evidence
* Detect contradictions
* Identify missing citations
* Independently inspect cited pages

---

## Memory Tests

Test whether:

* Audit results are stored
* Source history is updated
* Unsupported evidence is recognized later
* Contradicted evidence is not blindly reused
* Memory affects future research

---

## Conflict Tests

Test whether:

* Conflicting values are detected
* Dates are compared
* Source context is considered
* Primary evidence is identified
* Uncertainty is preserved when necessary

---

## Canary Tests

Test whether the Auditor can detect deliberately modified evidence.

---

# 🛠️ Technology Stack

## Frontend

* React
* TypeScript
* Material UI

## Backend

* Python
* FastAPI
* Pydantic

## Database

* PostgreSQL

## Caching / Short-Term State

* Redis

## AI

* LLM-based Analyst
* Independent Auditor
* Structured Outputs
* Tool Calling
* Research Planning
* Claim Verification

## Web Research

* Live Web Search
* Page Retrieval
* Content Extraction
* Source Metadata

## Infrastructure

* Docker
* Git
* Pytest
* Structured Logging

---

# 🚀 Quick Start

## 1️⃣ Clone

```bash
git clone https://github.com/<your-username>/VERITAS.git
cd VERITAS
```

---

## 2️⃣ Configure Environment

```bash
cp .env.example .env
```

Add the required API keys and database configuration.

Example:

```env
LLM_API_KEY=your_api_key
SEARCH_API_KEY=your_search_key
DATABASE_URL=your_database_url
REDIS_URL=your_redis_url
```

---

## 3️⃣ Install Backend Dependencies

```bash
pip install -r requirements.txt
```

---

## 4️⃣ Start Services

```bash
docker compose up --build
```

---

## 5️⃣ Start Backend

```bash
uvicorn backend.main:app --reload
```

---

## 6️⃣ Start Frontend

```bash
cd frontend
npm install
npm run dev
```

---

# 🧪 Run Tests

Run the complete test suite:

```bash
pytest
```

Run the evaluation:

```bash
python evaluation/run_evaluation.py
```

---

# 📜 Complete Project Workflow

```text
👤 USER
  │
  ▼
💬 Research Question
  │
  ▼
🧠 Question Understanding
  │
  ▼
📋 Research Planning
  │
  ▼
🌐 Parallel Web Search
  │
  ▼
📄 Page Retrieval
  │
  ▼
📚 Evidence Extraction
  │
  ▼
🤖 Analyst
  │
  ▼
📝 Answer + Claims + Citations
  │
  ▼
🛡️ Independent Auditor
  │
  ├──── 🟢 SUPPORTED
  │
  ├──── 🟡 UNSUPPORTED
  │
  ├──── 🔴 CONTRADICTED
  │
  └──── ⚪ MISSING CITATION
  │
  ▼
⚔️ Conflict Resolution
  │
  ▼
🧠 Evidence-Aware Memory
  │
  ├──── 📚 Claim History
  │
  ├──── 📊 Source History
  │
  └──── 🔄 Research Strategy
  │
  ▼
📤 Verified Answer
  │
  ▼
🔁 Future Research
```

---

# 📌 Project Status

## Core Research Pipeline

* [ ] Analyst research planning
* [ ] Live web search
* [ ] Page retrieval
* [ ] Evidence extraction
* [ ] Citation generation
* [ ] Independent Auditor
* [ ] Supported / Unsupported / Contradicted classification
* [ ] Missing-citation detection

## Memory & Adaptation

* [ ] Evidence-Aware Memory
* [ ] Claim History
* [ ] Source History
* [ ] Research History
* [ ] Memory reuse
* [ ] Future research adaptation

## Advanced Features

* [ ] Conflict Detection
* [ ] Conflict Resolution
* [ ] Auditor Canary Test
* [ ] Historical Source Reliability Signal

## Evaluation

* [ ] 8 progressive research questions
* [ ] Entity reuse
* [ ] Token tracking
* [ ] Cost tracking
* [ ] INR cost estimation
* [ ] Latency tracking
* [ ] Citation correctness
* [ ] Audit accuracy
* [ ] Adaptation measurement
* [ ] Evaluation dashboard

---

# 🔮 Future Improvements

Potential future extensions include:

* 🔄 Automatic auditor feedback into future research planning
* ⚡ Improved parallel research optimization
* 🌐 Broader source coverage
* 🧠 Improved evidence retrieval
* 📊 Advanced research analytics
* 🧪 Automated adversarial research cases
* 💰 Cost optimization
* ⏱️ Research execution optimization
* 🔍 Improved source conflict resolution
* 🕒 Automatic freshness detection
* 📈 More advanced source-history modeling
* 👥 Human review workflows
* 🤖 Multiple independent auditors
* 🧪 Larger research benchmarks

---

# 🎯 Success Criteria

VERITAS should demonstrate that it can:

```text
1. Perform live web research.

2. Create a research plan before searching.

3. Produce claims with citations.

4. Independently verify cited sources.

5. Classify evidence as:
   SUPPORTED
   UNSUPPORTED
   CONTRADICTED
   MISSING CITATION

6. Store audit findings in memory.

7. Reuse previously researched entities.

8. Detect conflicting evidence.

9. Test Auditor reliability using a canary test.

10. Track tokens and estimated cost.

11. Track latency and research behavior.

12. Evaluate at least eight progressively difficult
    research questions.

13. Measure whether audit findings influence
    future research behavior.
```

---

# 🏆 Key Differentiators

| Capability                             | VERITAS |
| -------------------------------------- | ------: |
| Live web research                      |       ✅ |
| Research planning                      |       ✅ |
| Parallel research                      |       ✅ |
| Evidence collection                    |       ✅ |
| Citations                              |       ✅ |
| Independent auditing                   |       ✅ |
| Claim-level verification               |       ✅ |
| Supported / Unsupported / Contradicted |       ✅ |
| Missing citation detection             |       ✅ |
| Conflict detection                     |       ✅ |
| Evidence-aware memory                  |       ✅ |
| Source history                         |       ✅ |
| Future research adaptation             |       ✅ |
| Auditor canary testing                 |       ✅ |
| Progressive evaluation                 |       ✅ |
| Token tracking                         |       ✅ |
| Cost tracking                          |       ✅ |
| Latency tracking                       |       ✅ |

---

# 🔐 Design Principles

### 1. Evidence Before Trust

> An AI-generated statement is not automatically a trusted fact.

### 2. Independent Verification

> Important claims should be independently checked against their cited evidence.

### 3. Memory Is Not Truth

> Stored information retains its evidence and verification history.

### 4. Failures Should Teach the System

> Audit findings should be available to influence future research.

### 5. Uncertainty Should Be Visible

> When evidence cannot establish an answer, VERITAS should preserve and communicate the uncertainty.

### 6. Historical Signals Are Not Guarantees

> A source's previous performance should inform research, not replace verification.

### 7. Measure Before Claiming Improvement

> The system should demonstrate adaptation through evaluation rather than assuming it.

---

# 💡 Core Philosophy

> ## **"No important fact should become trusted merely because an AI generated it."**

VERITAS follows:

```text
       🔎 EVIDENCE
            ↓
       🛡️ VERIFICATION
            ↓
       🧠 MEMORY
            ↓
       📚 LEARNING
            ↓
       🔄 ADAPTATION
            ↓
       🎯 BETTER RESEARCH
```

---

# 🌟 Final Summary

VERITAS is an evidence-first AI research and auditing system combining:

* 🌐 Live web research
* 🧠 Structured research planning
* 🛡️ Independent auditing
* 🔎 Claim-level evidence verification
* 🔗 Citation correctness checking
* 🧠 Evidence-Aware Memory
* 📊 Historical Source Reliability Signals
* ⚔️ Source Conflict Detection
* 🧪 Auditor Canary Testing
* 📈 Progressive research evaluation
* 💰 Token and cost tracking
* ⚡ Latency measurement
* 🔄 Future research adaptation

The central idea is:

> **An AI research system should not only remember what it found. It should remember how well the evidence survived verification — and use that history to guide future research.**

---

# 👨‍💻 Project

## VERITAS

### **Self-Correcting, Evidence-First AI Research & Audit System**

> **Research → Verify → Remember → Learn → Adapt → Research Better**

Built for **Problem 3 — Analyst & Auditor**, with a focus on:

* Agent design
* Live web research
* Research planning
* Independent verification
* Evidence-aware memory
* Source history
* Conflict resolution
* Auditor reliability
* Progressive evaluation
* Cost and latency measurement
* Measurable adaptation

---

# 📜 License

This project is intended for educational, research, and hackathon purposes.

Add the appropriate license here if the project is released publicly.

---

# ⭐ VERITAS

> **Research. Verify. Remember. Learn. Adapt. Research Better.**

```

**Yes, this is suitable for your `README.md`.** One thing to remember: before submission, change the `[ ]` project-status items to `[x]` **only for features you have actually implemented**, and replace the placeholder evaluation numbers (`XX`, `₹X`, `XXXX`) with your real results.
```
