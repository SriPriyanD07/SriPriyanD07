# Sri Priyan D

**AI Systems Engineer** · Machine Learning · Information Retrieval · Evidence-Grounded AI  
Chennai, India · [Portfolio](https://sripriyand-portfolio.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/sripriyandandayuthapani) · [GitHub](https://github.com/SriPriyanD07) · [Email](mailto:sripriyand@gmail.com)

---

### Overview

I build **evidence-grounded AI systems**, **information retrieval pipelines**, and **backend software**.

My work focuses on the reliability gap in applied machine learning: replacing unconstrained, speculative generation with verifiable architectures combining **hybrid lexical and dense retrieval (BM25 + vector search)**, **Cross-Encoder reranking**, **deterministic relevance gating**, and **cryptographic provenance tracing**.

Rather than treating AI as an external API wrapper, I design systems where statistical models operate within strict deterministic boundaries, backed by automated evaluation harnesses, empirical benchmarks, and explicit abstention when evidence is insufficient.

---

## Flagship System: JurisLens

### Evidence-Grounded Judicial Precedent Discovery & Analysis
**Repository:** [github.com/SriPriyanD07/jurislens](https://github.com/SriPriyanD07/jurislens)  
**Status:** Backend Architecture Frozen (`v1.0.0`) · **193 / 193 Passing Tests (100% Green)**  
**Governing Axiom:** *The LLM is never the source of legal authority.*

JurisLens is an AI-powered legal precedent discovery and analysis system designed for Indian jurisprudence. Standard RAG implementations frequently introduce hallucinated citations, topical drift, and spurious authority synthesis. JurisLens addresses these failure modes through an auditable, multi-stage retrieval and evidence-binding pipeline.

```
                    User Legal Scenario
                             │
                             ▼
┌─────────────────────────────────────────────────────────┐
│ 1. Scenario & Query Understanding                       │
│    • Deterministic normalization & legal abbreviation mapping│
│    • Controlled legal concept expansion                 │
└────────────────────────────┬────────────────────────────┘
                             │ Normalized Query
                             ▼
┌─────────────────────────────────────────────────────────┐
│ 2. First-Stage Hybrid Retrieval                         │
│    • Lexical Search: BM25Okapi over tokenized chunks    │
│    • Dense Semantic Search: all-MiniLM-L6-v2 embeddings │
│    • Fusion: Reciprocal Rank Fusion (RRF, k=60)         │
└────────────────────────────┬────────────────────────────┘
                             │ Top N=10 Candidates
                             ▼
┌─────────────────────────────────────────────────────────┐
│ 3. Second-Stage Joint Reranking                         │
│    • cross-encoder/ms-marco-MiniLM-L-6-v2               │
│    • Full cross-attention between scenario & text       │
└────────────────────────────┬────────────────────────────┘
                             │ Reordered Candidates
                             ▼
┌─────────────────────────────────────────────────────────┐
│ 4. Deterministic Relevance Gating & Safe Abstention      │
│    • Multi-signal decision boundary (Overlap + Score)   │
│    • Rejection of spurious single-token distractors     │
│    • Hard floor rejection (S_CE < -6.0)                 │
│    • Explicit abstention if no precedent qualifies      │
└────────────────────────────┬────────────────────────────┘
                             │ Qualified Candidates
                             ▼
┌─────────────────────────────────────────────────────────┐
│ 5. Evidence Extraction & Discourse Classification       │
│    • Exact byte-offset extraction (start_offset, end)   │
│    • Rule-based discourse tagger (HOLDING, FACTUAL)     │
└────────────────────────────┬────────────────────────────┘
                             │ Typed Evidence Spans
                             ▼
┌─────────────────────────────────────────────────────────┐
│ 6. Cryptographic Provenance Chain                       │
│    • 6-Tier Immutable Hierarchy with SHA-256 Digests    │
│    • Case ──► RawDoc ──► Revision ──► Chunk ──► Span    │
└────────────────────────────┬────────────────────────────┘
                             │ Verified Context Packet
                             ▼
┌─────────────────────────────────────────────────────────┐
│ 7. Closed-World Grounded Analysis                       │
│    • Strict prompt isolation (verified evidence only)   │
│    • Verbatim quotation verification & citation audit   │
│    • Explicit disclaimer: no outcome prediction / advice│
└─────────────────────────────────────────────────────────┘
```

### Engineering & Research Decisions
- **Hybrid Lexical-Semantic Fusion**: Combines BM25Okapi with dense vector embeddings via Reciprocal Rank Fusion ($k=60$), ensuring both exact statutory terminology and conceptual legal phrasing are represented in candidate selection.
- **Candidate Pool Optimization**: Empirically demonstrated that an $N=10$ candidate pool outperforms larger pools by preventing cross-attention dilution, improving held-out MRR from **0.8824 to 0.9118** and speeding up inference by **2.8x**.
- **Deterministic Relevance Gating**: Multi-signal token overlap and score thresholding rejects off-topic lexical matches before prompt assembly, preventing unrelated cases from appearing as supporting authorities.
- **Cryptographic Provenance**: Every extracted proposition carries immutable `(start_offset, end_offset)` coordinates tied to the raw judgment text, verified through SHA-256 content addressing.
- **Safe Abstention**: When retrieved evidence falls below empirical thresholds, the system issues an explicit refusal (`REFUSED_INSUFFICIENT_EVIDENCE`) and suppresses case cards, preventing ungrounded generation.

### Empirical Evaluation & Benchmark Metrics
| Component / Evaluation | Metric | Benchmark Scope / Notes |
| :--- | :--- | :--- |
| **Test Suite Coverage** | **193 / 193 Passing** | Full unit, integration, and regression coverage |
| **Held-Out Retrieval MRR** | **0.9118** | Evaluated on held-out judicial scenarios (+3.33% over baseline) |
| **Rank-1 Precedent Accuracy** | **82.35%** | First-rank retrieval accuracy (improved from 76.47%) |
| **Inference Latency** | **2.8x speedup** | Achieved through candidate pool optimization ($N=10$) |
| **Factual Proposition Classification** | **F1 = 1.0000** | 100% precision and recall on held-out factual spans |
| **Holding Proposition Classification** | **F1 = 0.9545** | 1.0000 precision, 0.9130 recall on legal holdings |
| **Relevance Gating Accuracy** | **100%** | Accurate refusal on out-of-corpus and irrelevant scenarios |

*Stack: Python · FastAPI · PyTorch · Sentence Transformers · CrossEncoder · SQLite · TypeScript · Next.js · React · Three.js*

---

## Selected Systems & Engineering Projects

### Predictive Maintenance for Military Systems
**Repository:** [github.com/SriPriyanD07/Predictive-Maintenance-for-Military-Equipment-SIH26](https://github.com/SriPriyanD07/Predictive-Maintenance-for-Military-Equipment-SIH26)  
*AI-driven telemetry analysis and Remaining Useful Life (RUL) estimation for defense machinery.*
- Built an asynchronous FastAPI telemetry service simulating sensor degradation across a fleet of 6 military turbofan engines.
- Implemented Remaining Useful Life (RUL) regression modeling trained on NASA's C-MAPSS FD001 dataset.
- Engineered automated test harness (`verify.py`) validating 9 system endpoints, telemetry replay buffers, and health diagnostics.  
*Stack: Python · FastAPI · XGBoost · Scikit-Learn · NumPy · TypeScript · React*

### Rubric Platform
**Repository:** [github.com/SriPriyanD07/rubric](https://github.com/SriPriyanD07/rubric) · **Live App:** [rubric-one.vercel.app](https://rubric-one.vercel.app/)  
*Automated evaluation pipeline auditing hackathon claims against live deployed artifacts.*
- Automates the project evaluation workflow: extracts checkable factual claims from project decks and cross-checks them against deployed web apps.
- Integrates headless Chromium (Playwright) to capture live application screenshots and runs automated visual consistency checks.
- Produces structured evidence scoring across a three-state verification schema: *supported*, *contradicted*, or *unverifiable*.  
*Stack: TypeScript · Next.js · React · Playwright · Tailwind CSS · Vercel*

### Fleet AI
**Repository:** [github.com/SriPriyanD07/Fleet_AI](https://github.com/SriPriyanD07/Fleet_AI)  
*Geospatial logistics platform and routing telemetry engine.*
- Engineered an interactive GIS mapping application leveraging OpenLayers and OpenRouteService (ORS) APIs.
- Implemented real-time waypoint interpolation, polyline route geometry generation, and fleet status monitoring.  
*Stack: JavaScript · React · Vite · Node.js · OpenLayers · REST APIs*

---

## Technical Capabilities

- **AI & Machine Learning**: Python · PyTorch · Scikit-Learn · XGBoost · OpenCV · Model Evaluation
- **Information Retrieval & NLP**: Okapi BM25 · Dense Semantic Retrieval · Sentence Transformers · Cross-Encoder Reranking · Reciprocal Rank Fusion (RRF) · Query Normalization
- **Backend & Systems**: FastAPI · Node.js · Express.js · RESTful APIs · Uvicorn · Pydantic · Asynchronous Architecture
- **Frontend & Visualization**: TypeScript · React · Next.js (App Router) · Three.js · OpenLayers · Tailwind CSS · HTML5 · CSS3
- **Data & Storage**: SQLite · MongoDB · SQL · Content-Addressed Storage (SHA-256)
- **Testing & Tooling**: Pytest · Vitest · Playwright · Git · GitHub · Linux / WSL · Postman · Vercel · Render

---

## Research Interests

- **Information Retrieval & Multi-Stage Ranking**: Studying interaction dynamics between sparse lexical scoring (BM25) and dense embeddings, optimizing late-stage cross-attention rerankers, and candidate pool sizing.
- **Evidence-Grounded AI & Safety**: Developing deterministic verification pipelines, exact character-level citation mapping, and explicit abstention mechanisms to ensure language models remain anchored in verified source corpora.
- **Reliable ML Systems**: Building architectures that treat machine learning models as probabilistic components within deterministic software guardrails.

---

## Engineering Philosophy

I don't simply consume external LLM APIs; I build the retrieval, ranking, validation, and evaluation systems around them. Reliable applied AI requires software engineering fundamentals: strict type validation, reproducible database schemas, empirical benchmark suites, deterministic guardrails, and automated regression testing.

---

## Education

- **B.Tech in Computer Science and Engineering** — Vellore Institute of Technology (VIT Chennai)
- **Core Coursework**: Data Structures & Algorithms, Operating Systems, Database Management Systems, Computer Networks, Machine Learning.
