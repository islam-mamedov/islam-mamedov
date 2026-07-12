<p align="center">
  <img src="./assets/banner.png" alt="Islam Mamedov — AI and LLM Engineer" width="100%" />
</p>

<p align="center">
  <strong>Computer Science graduate building practical AI, LLM, RAG, computer-vision, and software-engineering systems.</strong>
</p>

<p align="center">
  <a href="https://github.com/islam-mamedov">GitHub</a>
  ·
  <a href="https://huggingface.co/islam-mamedov">Hugging Face</a>
  ·
  <a href="mailto:islammamedov132004@gmail.com">Email</a>
</p>

---

## About

I am a Computer Science graduate from **Swinburne University of Technology Sarawak**, with a double major in **Artificial Intelligence and Cybersecurity**.

I enjoy building complete systems rather than isolated model demonstrations. My work combines LLMs, retrieval, computer vision, backend services, databases, evaluation, testing, and usable interfaces.

I am currently open to graduate opportunities in **AI Engineering, LLM Engineering, Machine Learning, and Software Engineering**.

---

## Selected Projects

### 1. FastAPI Codebase Q&A

An evaluation-driven RAG system for asking technical questions about the FastAPI codebase.

The system searches source code, documentation, and resolved GitHub issues before generating an answer. It returns file, symbol, and line-level references so the response can be checked against the original source.

**Key engineering work**

- Built AST-aware code chunking with Tree-sitter
- Compared dense retrieval, BM25, reranking, and LLM query rewriting
- Added grounded citations and evidence-aware refusal
- Created a labelled benchmark for retrieval and answer quality
- Added resumable ingestion, caching, retries, and regression tests

**Results:** Recall@5 `0.91` · MRR `0.71` · Faithfulness `0.89` · Correctness `0.91` · Refusal accuracy `7/7`

**Stack:** Python · LLMs · RAG · Streamlit · ChromaDB · BGE Embeddings · Tree-sitter · Pytest

[Source Code](https://github.com/islam-mamedov/codebase-rag) · [Live Demo](https://huggingface.co/spaces/islam-mamedov/fastapi-codebase-qa)

---

### 2. InsightForge

An LLM-powered data analyst that investigates business questions against a PostgreSQL database.

The system plans an investigation, discovers the relevant schema, generates SQL, checks it for safety, executes it in a read-only transaction, validates the result, and explains the final findings.

<p align="center">
  <a href="https://github.com/islam-mamedov/insightforge">
    <img src="https://raw.githubusercontent.com/islam-mamedov/insightforge/main/docs/demo.png" alt="InsightForge interface" width="88%" />
  </a>
</p>

**Key engineering work**

- Designed an eight-stage investigation workflow
- Added SQL inspection with SQLGlot
- Enforced read-only execution and restricted-table protection
- Added automatic SQL repair with controlled retries
- Validated empty outputs, null-only columns, and join duplication
- Tracked token use, latency, cost, and execution history

**Project snapshot:** `103 tests` · `~650,000 database rows` · `6 planted anomalies` · `3 repair attempts maximum`

**Stack:** Python · LLM Tool Calling · FastAPI · PostgreSQL · SQLAlchemy · SQLGlot · Docker · Pydantic

[Source Code](https://github.com/islam-mamedov/insightforge)

---

### 3. Concrete Inspection Agent

A multimodal AI system that combines concrete-defect detection with evidence-grounded repair guidance.

The vision model detects cracks, corrosion, and spalling. A LangGraph workflow then retrieves relevant information from USACE engineering guidance and uses the evidence to produce a cited response.

<p align="center">
  <a href="https://huggingface.co/spaces/islam-mamedov/inspection-agent">
    <img src="https://raw.githubusercontent.com/islam-mamedov/inspection-agent/main/assets/inspection-agent-demo.png" alt="Concrete Inspection Agent interface" width="88%" />
  </a>
</p>

**Key engineering work**

- Fine-tuned YOLOv8 for crack, corrosion, and spalling detection
- Built a LangGraph workflow with retrieval grading and query rewriting
- Created a ChromaDB knowledge base with section-level metadata
- Added cited answers and unsupported-question refusal
- Evaluated retrieval, citations, faithfulness, and refusal behaviour

**Results:** `1,770 images` · `5,897 objects` · Retrieval `28/28` · Citation validity `33/33` · Faithfulness `31/32`

**Stack:** Python · YOLOv8 · LLMs · LangGraph · LangChain · ChromaDB · Gradio

[Source Code](https://github.com/islam-mamedov/inspection-agent) · [Live Demo](https://huggingface.co/spaces/islam-mamedov/inspection-agent)

---

## Additional Work

| Project | What I built | Stack |
|---|---|---|
| [Java Multi-Agent Vehicle Routing System](https://github.com/islam-mamedov/vrp-mas-intelligent-system) | A JADE-based routing system using master and delivery agents, genetic algorithms, simulated annealing, nearest-neighbour search, and local optimisation | Java · JADE · Multi-Agent Systems |
| [Swinburne Campus App](https://github.com/islam-mamedov/swinburne-app-group13) | A mobile-first campus platform for navigation, safety, support, events, and administration | Next.js · React · TypeScript · Supabase |

---

## Technical Skills

**AI & LLMs:** Large Language Models, RAG, LangGraph, tool calling, embeddings, vector search, prompt engineering, computer vision, object detection, model evaluation

**Backend & Data:** Python, FastAPI, PostgreSQL, SQLAlchemy, ChromaDB, Pydantic, REST APIs, Docker

**Software Engineering:** Java, TypeScript, Next.js, React, Git, Linux, testing, CI/CD

---

## Education

**Bachelor of Computer Science**  
Swinburne University of Technology Sarawak  
Double Major: **Artificial Intelligence and Cybersecurity**

---

<p align="center">
  <strong>Building AI systems that move from raw data to evidence, reasoning, and useful action.</strong>
</p>

<p align="center">
  <a href="mailto:islammamedov132004@gmail.com">Contact me</a>
</p>
