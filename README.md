# 🔎 VERITAS

### **Self-Correcting, Evidence-First AI Research & Audit System**

> **Research → Verify → Remember → Learn → Adapt → Research Better**

VERITAS is an AI-powered research system that answers complex questions using **live web sources** and an **independent AI Auditor** that verifies the claims and citations produced by the research agent.

Unlike a traditional research chatbot that simply generates an answer, VERITAS remembers previous verification failures, tracks evidence quality, identifies conflicting sources, and uses previous audit results to improve future research.

---

## 🌟 Why VERITAS?

Modern AI research systems can produce answers that *look correct* while containing:

* ❌ Incorrect factual claims
* ⚠️ Unsupported statements
* 🕒 Outdated information
* 🔗 Citation mismatches
* 📄 Over-reliance on a single source
* ⚔️ Conflicting information between sources
* 🔁 Repeated mistakes across different questions

VERITAS addresses this through an independent verification and learning loop.

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
       🟢 PASS     🟡 WARN     🔴 FAIL
      Supported   Unsupported  Contradicted
          └──────────┼──────────┘
                     ▼
             🧠 EVIDENCE MEMORY
                     │
                     ▼
             📊 SOURCE REPUTATION
                     │
                     ▼
             🔄 FUTURE RESEARCH
                     │
                     └──────────────► Better Research
```

---

# 🎯 Core Idea

VERITAS consists of two independent AI roles:

### 🧠 Analyst

The Analyst performs the actual research.

It:

1. Understands the user's question
2. Identifies entities and required information
3. Creates a research plan
4. Searches the live web
5. Retrieves relevant pages
6. Extracts evidence
7. Cross-checks important information
8. Generates a cited answer

### 🛡️ Auditor

The Auditor does **not simply trust the Analyst**.

It independently checks:

> **"Does the cited evidence actually support this claim?"**

Each claim receives a status:

| Status                 | Meaning                                  |
| ---------------------- | ---------------------------------------- |
| 🟢 **SUPPORTED**       | Evidence supports the claim              |
| 🟡 **UNSUPPORTED**     | Evidence is insufficient                 |
| 🔴 **CONTRADICTED**    | Evidence conflicts with the claim        |
| ⚪ **MISSING CITATION** | Important claim has no suitable citation |

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
       ⚠️ FAILURE FOUND
             │
             ▼
       🧠 REMEMBER WHY
             │
             ▼
       📊 UPDATE SOURCE
          REPUTATION
             │
             ▼
       🔄 CHANGE FUTURE
        RESEARCH STRATEGY
             │
             ▼
       🎯 BETTER ANSWER
```

The system therefore turns previous failures into actionable knowledge.

---

# 👤 Concrete User Workflow

A user simply enters a research question.

### Example

> **"Which Indian jewellery retailers opened the most stores in the last two years?"**

### Step 1 — 💬 User Input

The user submits the question.

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

### Step 2 — 🧠 Research Planning

The Analyst creates a research plan.

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

---

### Step 3 — 🌐 Parallel Web Research

Independent searches can run simultaneously.

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

This reduces unnecessary sequential searching.

---

### Step 4 — 📚 Evidence Collection

VERITAS extracts relevant information from the retrieved pages.

For every important piece of information:

```text
Fact
 ↓
Source
 ↓
URL
 ↓
Publication Date
 ↓
Evidence
 ↓
Claim
```

---

### Step 5 — ✍️ Analyst Generates Answer

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

---

### Step 6 — 🛡️ Independent Audit

The Auditor receives the claims and independently opens the cited sources.

```text
Claim
  ↓
Find cited source
  ↓
Open source
  ↓
Read evidence
  ↓
Compare claim vs evidence
  ↓
Classify
```

---

### Step 7 — ⚖️ Verification

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
Company annual report → 31 stores

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
Prefer applicable primary evidence
        ↓
Resolve or report uncertainty
```

If the evidence cannot establish a clear answer, VERITAS explicitly reports the uncertainty.

---

# 🧠 Evidence-Aware Memory

Traditional memory might store:

```text
Company X → CEO = Person Y
```

VERITAS stores:

```text
┌─────────────────────────────┐
│ FACT                        │
│ Company X → CEO → Person Y  │
├─────────────────────────────┤
│ SOURCE                      │
│ company.com                 │
├─────────────────────────────┤
│ SOURCE TYPE                 │
│ Primary                     │
├─────────────────────────────┤
│ AUDIT STATUS                │
│ 🟢 SUPPORTED                │
├─────────────────────────────┤
│ VERIFIED                    │
│ 2026-09-23                  │
├─────────────────────────────┤
│ AUDIT HISTORY               │
│ 2 successful checks         │
└─────────────────────────────┘
```

This prevents an unverified fact from becoming permanent system knowledge.

---

# 🔄 Self-Correction Example

### Question 1

> Who is the CEO of Company X?

Analyst:

```text
Person A
```

Auditor:

```text
🔴 CONTRADICTED
```

VERITAS stores:

```text
Company X → Person A
Status → CONTRADICTED
```

---

### Question 2

> What was Company X's CEO's previous role?

Instead of blindly reusing Person A:

```text
Memory lookup
      ↓
Previous information = CONTRADICTED
      ↓
❌ Do not blindly reuse
      ↓
🌐 Fresh research
      ↓
New evidence
```

This is the **self-correction mechanism**.

---

# 📊 Source Reputation

VERITAS maintains a historical signal based on previous audit results.

```text
Source                         Signal

🏢 Official company website    HIGH
🏛️ Government / regulator      HIGH
📰 Reputable news              HIGH
🌐 Industry database           MEDIUM
📝 Unknown website              LOW
```

This is **not treated as absolute truth**.

It simply influences future source prioritization.

```text
Research
   ↓
Audit
   ↓
Source performance
   ↓
Reputation update
   ↓
Future source prioritization
```

A source that repeatedly produces unsupported information can receive lower priority in future research.

---

# 🧪 Auditor Canary Test

VERITAS also tests whether its own Auditor can detect manipulated evidence.

### Test 1

```text
CLAIM:
Company X raised $50M.

EVIDENCE:
Company X announced a $50M funding round.

EXPECTED:
🟢 SUPPORTED
```

### Test 2

Change only the evidence:

```text
CLAIM:
Company X raised $50M.

EVIDENCE:
Company X announced a $30M funding round.

EXPECTED:
🔴 CONTRADICTED
```

If the Auditor still returns `SUPPORTED`, VERITAS identifies a weakness in its own verification system.

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
                 │  QUESTION ANALYZER│
                 └─────────┬─────────┘
                           │
                           ▼
                 ┌───────────────────┐
                 │ RESEARCH PLANNER  │
                 └─────────┬─────────┘
                           │
              ┌────────────┼────────────┐
              ▼            ▼            ▼
        🌐 Web Search  📄 Fetcher  🔎 Search 2
              │            │            │
              └────────────┼────────────┘
                           ▼
                 ┌───────────────────┐
                 │ EVIDENCE COLLECTOR│
                 └─────────┬─────────┘
                           │
                           ▼
                 ┌───────────────────┐
                 │  ANALYST AGENT    │
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
       📚 FACT MEMORY            📊 SOURCE TRUST
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
       │ Facts        │   │ Cache        │
       │ Sources      │   │ Sessions     │
       │ Audits       │   │ Short state  │
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
│   ├── 📁 agents/
│   │   ├── analyst.py
│   │   └── auditor.py
│   │
│   ├── 📁 research/
│   │   ├── planner.py
│   │   ├── search.py
│   │   ├── fetcher.py
│   │   └── extractor.py
│   │
│   ├── 📁 memory/
│   │   ├── evidence_memory.py
│   │   └── source_reputation.py
│   │
│   ├── 📁 verification/
│   │   ├── claim_checker.py
│   │   └── conflict_resolver.py
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
│   │   └── App.tsx
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
│   └── test_conflicts.py
│
├── 📁 logs/
│   └── ai-session-logs/
│
├── 📁 docs/
│   ├── architecture.md
│   └── evaluation.md
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

VERITAS will be tested using **at least eight progressively difficult questions**.

```text
🟢 Q1 → Basic factual research
       ↓
🟢 Q2 → Multi-source research
       ↓
🟡 Q3 → Entity research
       ↓
🟡 Q4 → Memory reuse
       ↓
🟠 Q5 → Entity comparison
       ↓
🟠 Q6 → Complex evidence
       ↓
🔴 Q7 → Conflicting sources
       ↓
🔥 Q8 → Full-system challenge
```

The evaluation measures:

### 🎯 Accuracy

* Total claims
* Supported claims
* Unsupported claims
* Contradicted claims
* Citation coverage

### ⚡ Performance

* Research latency
* Number of searches
* Pages retrieved
* Memory reuse

### 💰 Cost

* Input tokens
* Output tokens
* Estimated cost/question

### 🧠 Adaptation

* Source reputation changes
* Re-verification events
* Memory decisions
* Auditor failures

---

# 📊 Example Evaluation Dashboard

```text
╔════════════════════════════════════════════╗
║             VERITAS ANALYTICS              ║
╠═══════════╦═══════════╦══════════╦═════════╣
║ Questions ║  Claims   ║ Verified ║  Cost   ║
║     8     ║    73     ║   61     ║  ₹X.XX  ║
╠═══════════╩═══════════╩══════════╩═════════╣
║                                            ║
║  🟢 Supported       61                     ║
║  🟡 Unsupported      7                     ║
║  🔴 Contradicted     5                     ║
║                                            ║
║  Citation Coverage: 100%                   ║
║  Average Latency:   XX seconds             ║
║                                            ║
║  Source Reliability     ↑                  ║
║  Unsupported Claims    ↓                   ║
║  Research Cost         ↓                   ║
║                                            ║
╚════════════════════════════════════════════╝
```

---

# 🧪 Example End-to-End Run

### 👤 User

> "How much funding did Company X raise in 2025?"

### 🔎 Analyst

Searches:

```text
Source A → $50M
Source B → $50M
Source C → $45M
```

### 📝 Analyst Answer

> Company X raised $50M in 2025.

### 🛡️ Auditor

```text
Source A → 🟢 Supports
Source B → 🟢 Supports
Source C → ⚠️ Conflicting
```

### ⚖️ Conflict Engine

Determines that Source A is the applicable primary source.

### 🧠 Memory

Stores:

```text
Company X
Funding 2025
Value → $50M
Status → SUPPORTED
Conflict → Yes
Primary Source → Source A
```

### 🔄 Future Question

A later question about Company X retrieves this information but also knows:

```text
⚠️ Previous source conflict existed.
```

The system can re-verify if necessary.

---

# 🏆 Key Differentiators

| Feature                    | Traditional Research AI | VERITAS |
| -------------------------- | ----------------------- | ------- |
| Web research               | ✅                       | ✅       |
| Citations                  | ✅                       | ✅       |
| Independent auditing       | ❌                       | ✅       |
| Claim-level verification   | Limited                 | ✅       |
| Conflict detection         | Limited                 | ✅       |
| Evidence-aware memory      | ❌                       | ✅       |
| Source reputation          | ❌                       | ✅       |
| Research-strategy learning | ❌                       | ✅       |
| Auditor stress testing     | ❌                       | ✅       |
| Failure feedback loop      | ❌                       | ✅       |
| Cost tracking              | Limited                 | ✅       |

---

# 🔐 Design Principles

### 1. Evidence before trust

> An AI-generated statement is not automatically a trusted fact.

### 2. Independent verification

> The Auditor should independently verify important claims.

### 3. Memory is not truth

> Stored information retains its evidence and verification status.

### 4. Failures should teach the system

> Audit failures should influence future research.

### 5. Uncertainty should be visible

> When evidence cannot establish an answer, VERITAS reports the uncertainty.

---

# 🛠️ Technology Stack

### Frontend

![React](https://img.shields.io/badge/React-2026-61DAFB?style=for-the-badge\&logo=react\&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-2026-3178C6?style=for-the-badge\&logo=typescript\&logoColor=white)
![Material UI](https://img.shields.io/badge/Material_UI-2026-007FFF?style=for-the-badge\&logo=mui\&logoColor=white)

### Backend

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge\&logo=python\&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?style=for-the-badge\&logo=fastapi\&logoColor=white)

### Data

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge\&logo=postgresql\&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-Cache-DC382D?style=for-the-badge\&logo=redis\&logoColor=white)

### AI

* 🤖 LLM-based Analyst
* 🛡️ Independent Auditor
* 🔧 Tool Calling
* 📋 Structured Outputs
* 🧠 Evidence-Aware Memory

### Infrastructure

* 🐳 Docker
* 🔀 Git
* 🧪 Pytest
* 📊 Structured Logging

---

# 🚀 Quick Start

## 1️⃣ Clone

```bash
git clone https://github.com/<your-username>/VERITAS.git
cd VERITAS
```

## 2️⃣ Configure environment

```bash
cp .env.example .env
```

Add the required API keys and database configuration.

## 3️⃣ Start services

```bash
docker compose up --build
```

## 4️⃣ Start backend

```bash
uvicorn backend.main:app --reload
```

## 5️⃣ Start frontend

```bash
cd frontend
npm install
npm run dev
```

---

# 🧪 Run Tests

```bash
pytest
```

Run the complete evaluation:

```bash
python evaluation/run_evaluation.py
```

---

# 📜 Project Workflow

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
📝 Answer + Citations
  │
  ▼
🛡️ Independent Auditor
  │
  ├──── 🟢 Supported
  ├──── 🟡 Unsupported
  └──── 🔴 Contradicted
  │
  ▼
⚖️ Conflict Resolution
  │
  ▼
🧠 Evidence-Aware Memory
  │
  ├──── 📚 Verified Facts
  ├──── 📊 Source Reputation
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

```text
🟢 Architecture       Planned
🟢 Analyst            Planned
🟢 Auditor            Planned
🟡 Evidence Memory    Planned
🟡 Source Reputation  Planned
🟡 Conflict Engine    Planned
🟡 Evaluation         Planned
🟡 Dashboard          Planned
```

---

# 🎯 Future Improvements

* 🔄 Automatic auditor feedback into future research planning
* ⚡ Parallel research optimization
* 🌐 Larger source coverage
* 🧠 Improved evidence retrieval
* 📊 Advanced research analytics
* 🧪 Automated adversarial research cases
* 💰 Cost optimization
* ⏱️ Two-minute maximum research execution
* 🔍 Better source conflict resolution

---

# 💡 Core Philosophy

> ### **"No important fact should become trusted merely because an AI generated it."**

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

# 👨‍💻 Project

**VERITAS — Self-Correcting, Evidence-First AI Research & Audit System**

Built as an implementation of **Problem 3 — Analyst & Auditor**, focusing on agent design, live web research, independent verification, evidence-aware memory, adaptive source selection, conflict resolution, and measurable evaluation.
