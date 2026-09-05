<div align="center">

# Hi there, I'm Sri Priyan D 👋
### 🎓 Computer Science & Engineering @ VIT Chennai

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=1000&color=38BDF8&center=true&vCenter=true&width=650&lines=AI+%26+Information+Retrieval+Systems;Machine+Learning+%26+Deep+Learning;Full-Stack+Software+Architecture;Evidence-Grounded+AI+Pipelines)](https://git.io/typing-svg)

<p align="center">
  <a href="https://www.linkedin.com/in/sripriyandandayuthapani">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://github.com/SriPriyanD07">
    <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub" />
  </a>
  <a href="https://sripriyand-portfolio.vercel.app/">
    <img src="https://img.shields.io/badge/Portfolio-2563EB?style=flat-square&logo=google-chrome&logoColor=white" alt="Portfolio" />
  </a>
  <a href="https://rubric-one.vercel.app">
    <img src="https://img.shields.io/badge/Rubric_App-7C3AED?style=flat-square&logo=vercel&logoColor=white" alt="Rubric" />
  </a>
</p>

---

</div>

## 📌 About Me

I am a Computer Science student at **Vellore Institute of Technology (VIT Chennai)** building AI/ML systems, information retrieval pipelines, and full-stack applications.

My work bridges statistical machine learning and reliable software engineering—designing retrieval architectures with verifiable evidence, deep learning computer vision models, and responsive web platforms.

- 🔨 **Currently Building**: **[JurisLens](https://github.com/SriPriyanD07/jurislens)** — an evidence-grounded judicial precedent discovery and analysis system powered by hybrid retrieval and cross-encoder reranking.
- 🔬 **Currently Exploring**: Multi-stage ranking pipelines, targeted contrastive loss for medical vision (**MVCRNet**), and automated application verification workflows.
- 🎯 **Areas of Interest**: Information Retrieval · Machine Learning · AI Systems · Backend Architecture · Computer Vision.

---

## 🚀 Featured Flagship Project

### ⚖️ [JurisLens — Evidence-Grounded Judicial Precedent Discovery](https://github.com/SriPriyanD07/jurislens)

> **AI-powered precedent discovery and analysis system designed for Indian jurisprudence, replacing ungrounded generative search with an auditable, multi-stage retrieval and citation pipeline.**

*Traditional RAG architectures frequently introduce hallucinated citations and topical drift. JurisLens addresses this with deterministic guardrails, verified source indexing, and safe abstention.*

- **Dual-Path Hybrid Retrieval**: Blends Okapi BM25 lexical search with dense vector embeddings (`all-MiniLM-L6-v2`) via Reciprocal Rank Fusion (RRF, $k=60$) to capture statutory terminology and conceptual semantics.
- **Joint Cross-Encoder Reranking**: Re-scores candidates using deep cross-attention (`ms-marco-MiniLM-L-6-v2`) with an optimal candidate pool ($N=10$) that prevents attention dilution.
- **Deterministic Relevance Gating**: Multi-signal token overlap and score thresholding rejects off-topic distractors and issues explicit abstention (`REFUSED_INSUFFICIENT_EVIDENCE`) when evidence is insufficient.
- **Cryptographic Provenance**: 6-tier immutable chain ($\text{Case} \rightarrow \text{RawDoc} \rightarrow \text{Chunk} \rightarrow \text{Span}$) verified with SHA-256 content addressing and exact character byte-offsets.

```text
🧪 193 / 193 Tests Passing (100% Green)  │  📈 0.9118 Held-Out MRR  │  🎯 82.35% Rank-1 Accuracy  │  ⚡ 2.8x Speedup
```

*Stack: Python · FastAPI · PyTorch · Sentence Transformers · CrossEncoder · SQLite · TypeScript · Next.js · React · Three.js*  
👉 **[Explore the JurisLens Repository ↗](https://github.com/SriPriyanD07/jurislens)**

---

## 🛠️ Strong Engineering & Research Projects

- 🛡️ **[Predictive Maintenance for Military Systems](https://github.com/SriPriyanD07/Predictive-Maintenance-for-Military-Equipment-SIH26)**  
  *AI-driven Remaining Useful Life (RUL) estimation & telemetry simulation for defense machinery.*  
  Asynchronous FastAPI telemetry backend simulating sensor degradation across a fleet of 6 military turbofan engines. Implemented Remaining Useful Life (RUL) regression modeling trained on NASA's C-MAPSS FD001 dataset, verified with an automated 9-endpoint testing harness.  
  *Stack: Python · FastAPI · XGBoost · Scikit-Learn · NumPy · TypeScript · React*

- 📊 **[Rubric Platform](https://github.com/SriPriyanD07/rubric)** • [**Live App ↗**](https://rubric-one.vercel.app/)  
  *Automated evaluation pipeline auditing hackathon claims against live deployed artifacts.*  
  Automates project verification by extracting checkable factual claims from project decks and cross-checking them against deployed web apps. Uses headless Chromium (Playwright) to capture live screenshots and runs visual consistency scoring (*supported / contradicted / unverifiable*).  
  *Stack: TypeScript · Next.js · React · Playwright · Tailwind CSS · Vercel*

- 🚚 **[Fleet AI](https://github.com/SriPriyanD07/Fleet_AI)**  
  *Geospatial fleet logistics platform and routing telemetry engine.*  
  Interactive GIS mapping application built with OpenLayers and OpenRouteService (ORS) APIs. Features road-network waypoint interpolation, dynamic polyline geometry rendering, and vehicle routing simulation.  
  *Stack: JavaScript · React · Vite · Node.js · OpenLayers · REST APIs*

- 🔬 **[MVCRNet — Multi-View Medical Vision](https://github.com/SriPriyanD07)**  
  *Deep learning architecture for endoscopic gastrointestinal disease classification.*  
  Addresses clinical confusion between visually similar endoscopic findings (e.g. esophagitis vs. z-line) by training a targeted pairwise supervised contrastive loss (SupCon) on multi-view feature representations, achieving ~94% classification accuracy.  
  *Stack: Python · PyTorch · Computer Vision · Contrastive Learning · Scikit-Learn*

- 📈 **[Data Analysis Engine](https://github.com/SriPriyanD07/Data_Analysis)**  
  *Exploratory data analysis, statistical modeling, and visualization workflows.*  
  Multi-domain exploratory data analysis pipelines, feature engineering, and automated visualization dashboards for high-dimensional datasets.  
  *Stack: Python · Pandas · NumPy · Seaborn · Matplotlib · Scikit-Learn*

- 🌐 **[Developer Portfolio](https://github.com/SriPriyanD07/portfolio)** • [**Live Site ↗**](https://sripriyand-portfolio.vercel.app/)  
  *Personal developer website showcasing software projects, research, and technical stack.*  
  Responsive, modern portfolio application featuring interactive component demos, clean UI/UX, and fast client-side navigation.  
  *Stack: TypeScript · React · Tailwind CSS · Vercel*

---

## 💥 Tech Stack

<details open>
<summary><b>🧠 AI, Machine Learning & NLP</b></summary>
<br>

<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/Sentence_Transformers-FFA500?style=flat-square&logo=huggingface&logoColor=white" alt="Sentence Transformers" />
  <img src="https://img.shields.io/badge/Cross--Encoder-6366F1?style=flat-square" alt="Cross-Encoder" />
  <img src="https://img.shields.io/badge/BM25-4B5563?style=flat-square" alt="BM25" />
  <img src="https://img.shields.io/badge/XGBoost-EB392E?style=flat-square&logo=xgboost&logoColor=white" alt="XGBoost" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white" alt="Scikit-Learn" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="Pandas" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV" />
</p>
</details>

<details open>
<summary><b>⚙️ Backend & Systems</b></summary>
<br>

<p align="left">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white" alt="Express.js" />
  <img src="https://img.shields.io/badge/REST_APIs-005571?style=flat-square" alt="REST APIs" />
  <img src="https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white" alt="Pydantic" />
</p>
</details>

<details open>
<summary><b>🌐 Frontend & Web Development</b></summary>
<br>

<p align="left">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white" alt="Three.js" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3" />
</p>
</details>

<details open>
<summary><b>🗄️ Databases & Developer Tooling</b></summary>
<br>

<p align="left">
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" alt="SQL" />
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" alt="Playwright" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub" />
  <img src="https://img.shields.io/badge/Linux%2FWSL-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux/WSL" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white" alt="Vercel" />
  <img src="https://img.shields.io/badge/Render-46E3B7?style=flat-square&logo=render&logoColor=white" alt="Render" />
  <img src="https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white" alt="Postman" />
</p>
</details>

---

## 📊 GitHub Analytics

<div align="center">
  <img src="https://github-readme-stats-fast.vercel.app/api?username=SriPriyanD07&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=38BDF8&text_color=C9D1D9" alt="GitHub Stats" />
  <img src="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=SriPriyanD07&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=58A6FF&text_color=C9D1D9" alt="Top Languages" />
  <br><br>
  <img src="https://streak-stats.demolab.com/?user=SriPriyanD07&theme=tokyonight&hide_border=true&background=0D1117&ring=38BDF8&fire=38BDF8&currStreakLabel=38BDF8" alt="GitHub Streak Stats" />
  <br><br>
  <img src="https://ghchart.rshah.org/38BDF8/SriPriyanD07" alt="SriPriyanD07's Contribution Chart" />
</div>

---

<div align="center">
  <p><i>💡 "Turning complex problems into elegant, intelligent software."</i></p>
  <img src="https://komarev.com/ghpvc/?username=SriPriyanD07&label=Profile%20Views&color=0e75b6&style=flat-square" alt="Profile Views" />
</div>
