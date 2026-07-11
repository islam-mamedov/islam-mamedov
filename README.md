from pathlib import Path

readme = r'''<p align="center">
  <img src="./assets/header-banner.png" alt="Islam Mamedov — AI and LLM Engineer" width="100%" />
</p>

<h1 align="center">Islam Mamedov</h1>

<h3 align="center">
  Graduate AI & LLM Engineer · RAG · Computer Vision · Agentic Systems
</h3>

<p align="center">
  I build AI systems that retrieve useful evidence, reason through tasks, work with tools, and produce results people can actually use.
</p>

<p align="center">
  <a href="https://github.com/islam-mamedov">
    <img src="https://img.shields.io/badge/GitHub-islam--mamedov-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub profile" />
  </a>
  <a href="mailto:islammamedov132004@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Islam Mamedov" />
  </a>
  <a href="https://huggingface.co/islam-mamedov">
    <img src="https://img.shields.io/badge/Hugging_Face-Live_Demos-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face profile" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Open_to-AI_%26_LLM_Roles-2EA44F?style=flat-square" alt="Open to AI and LLM roles" />
  <img src="https://img.shields.io/badge/Open_to-Relocation-8A2BE2?style=flat-square" alt="Open to relocation" />
</p>

---

## About Me

I am a Computer Science graduate with a double major in **Artificial Intelligence and Cybersecurity**.

I enjoy building complete systems rather than isolated model demos. My projects usually combine an AI or LLM component with retrieval, evaluation, backend services, databases, testing, and a usable interface.

Recently, I have been working on:

- evaluation-driven RAG systems
- LLM agents that can plan and use tools
- multimodal applications combining computer vision and language models
- safe AI workflows with validation, refusal handling, and traceable evidence
- full-stack applications built with Python, FastAPI, PostgreSQL, Next.js, and React

I am currently looking for graduate opportunities in **AI Engineering, LLM Engineering, Machine Learning Engineering, and Software Engineering**.

---

# Featured Projects

## 1. FastAPI Codebase Q&A

<p>
  <img src="https://img.shields.io/badge/Status-Deployed_Demo-2EA44F?style=flat-square" alt="Deployed demo" />
  <img src="https://img.shields.io/badge/Focus-LLM_%26_RAG-6F42C1?style=flat-square" alt="LLM and RAG" />
  <img src="https://img.shields.io/badge/Refusal_Accuracy-7%2F7-2EA44F?style=flat-square" alt="7 out of 7 refusal accuracy" />
</p>

An evaluation-driven RAG application for asking technical questions about the FastAPI codebase.

Instead of answering from the LLM's general knowledge, the system searches FastAPI source code, documentation, and resolved GitHub issues before generating a response. Every answer includes references to the files, symbols, and line ranges that support it.

<p align="center">
  <a href="https://huggingface.co/spaces/islam-mamedov/fastapi-codebase-qa">
    <img src="https://raw.githubusercontent.com/islam-mamedov/codebase-rag/main/assets/codebase-rag-demo.gif" alt="FastAPI Codebase Q&A demo" width="100%" />
  </a>
</p>

### What I worked on

- Built separate chunking strategies for source code, Markdown documentation, and GitHub issues
- Used Tree-sitter to preserve classes, methods, functions, symbols, and line ranges
- Compared dense retrieval, BM25 hybrid search, reranking, and LLM query rewriting
- Selected the final retriever based on measured performance rather than assumptions
- Added grounded citations and refusal behaviour for questions that cannot be supported
- Created a labelled benchmark to evaluate retrieval and answer quality
- Added resumable ingestion, caching, retries, and regression tests

### Results

| Metric | Result |
|---|---:|
| Indexed source files | 46 |
| Documentation files | 161 |
| Closed GitHub issues | 175 |
| Total chunks | 1,352 |
| Evaluation questions | 42 |
| Recall@5 | 0.91 |
| Mean Reciprocal Rank | 0.71 |
| Faithfulness | 0.89 |
| Correctness | 0.91 |
| Refusal accuracy | 7 / 7 |

**Stack:** Python · LLMs · RAG · Streamlit · ChromaDB · BGE Embeddings · Tree-sitter · PyGithub · Pytest

<p>
  <a href="https://github.com/islam-mamedov/codebase-rag"><strong>Source Code</strong></a>
  ·
  <a href="https://huggingface.co/spaces/islam-mamedov/fastapi-codebase-qa"><strong>Live Demo</strong></a>
</p>

---

## 2. InsightForge

<p>
  <img src="https://img.shields.io/badge/Status-Active_Development-F59E0B?style=flat-square" alt="Active development" />
  <img src="https://img.shields.io/badge/Focus-LLM_Data_Agent-6F42C1?style=flat-square" alt="LLM data agent" />
  <img src="https://img.shields.io/badge/Tests-103_Passing-2EA44F?style=flat-square" alt="103 passing tests" />
</p>

InsightForge is an LLM-powered data analyst that investigates business questions against a PostgreSQL database.

The goal was not simply to generate SQL. I wanted the system to plan an investigation, inspect the relevant schema, execute queries safely, repair failed SQL, validate the returned data, and explain how it reached its conclusion.

<p align="center">
  <a href="https://github.com/islam-mamedov/insightforge">
    <img src="https://raw.githubusercontent.com/islam-mamedov/insightforge/main/docs/demo.png" alt="InsightForge investigation interface" width="100%" />
  </a>
</p>

### What I worked on

- Designed an eight-stage investigation workflow from question interpretation to final explanation
- Limited schema context so the LLM only sees tables relevant to the current question
- Used SQLGlot to parse and inspect generated SQL
- Blocked write operations, unsafe functions, restricted tables, and sensitive columns
- Executed queries inside read-only database transactions
- Added automatic SQL repair with a controlled retry limit
- Checked results for empty outputs, null-only columns, and duplicated rows caused by joins
- Separated direct findings from model-generated interpretations
- Added audit logs for token use, latency, cost, and execution history

### Project Snapshot

| Area | Result |
|---|---:|
| Investigation stages | 8 |
| Automated tests | 103 |
| Synthetic database | ~650,000 rows |
| Planted benchmark anomalies | 6 |
| SQL repair attempts | Maximum of 3 |
| Query protection | AST inspection + read-only execution |

**Stack:** Python · LLM Tool Calling · FastAPI · PostgreSQL · SQLAlchemy · SQLGlot · Docker · Pydantic

<p>
  <a href="https://github.com/islam-mamedov/insightforge"><strong>Source Code</strong></a>
</p>

---

## 3. Concrete Inspection Agent

<p>
  <img src="https://img.shields.io/badge/Status-Deployed_Demo-2EA44F?style=flat-square" alt="Deployed demo" />
  <img src="https://img.shields.io/badge/Focus-Multimodal_AI-6F42C1?style=flat-square" alt="Multimodal AI" />
  <img src="https://img.shields.io/badge/License-MIT-007EC6?style=flat-square" alt="MIT License" />
</p>

A multimodal inspection system that combines computer vision with an evidence-grounded LLM workflow.

The vision model detects concrete defects in an uploaded image. The agent then retrieves relevant information from an engineering manual and uses that evidence to explain the finding and provide grounded repair guidance.

<p align="center">
  <a href="https://huggingface.co/spaces/islam-mamedov/inspection-agent">
    <img src="https://raw.githubusercontent.com/islam-mamedov/inspection-agent/main/assets/inspection-agent-demo.png" alt="Concrete Inspection Agent interface" width="100%" />
  </a>
</p>

### What I worked on

- Fine-tuned YOLOv8 to detect cracks, corrosion, and spalling
- Connected visual detections to a conditional LangGraph workflow
- Built a ChromaDB knowledge base from USACE engineering guidance
- Preserved section metadata so answers could cite the supporting manual sections
- Added retrieval grading and query rewriting when the first search was weak
- Added refusal behaviour for questions that the manual could not support
- Evaluated retrieval quality, citation validity, faithfulness, and refusals

### Results

| Metric | Result |
|---|---:|
| Training images | 1,770 |
| Annotated objects | 5,897 |
| Defect classes | 3 |
| Knowledge-base chunks | 292 |
| Evaluation questions | 35 |
| Retrieval hit rate | 28 / 28 |
| Citation validity | 33 / 33 |
| Faithfulness | 31 / 32 |
| Refusal correctness | 33 / 35 |

**Stack:** Python · YOLOv8 · LLMs · LangGraph · LangChain · ChromaDB · Gradio · Hugging Face Spaces

<p>
  <a href="https://github.com/islam-mamedov/inspection-agent"><strong>Source Code</strong></a>
  ·
  <a href="https://huggingface.co/spaces/islam-mamedov/inspection-agent"><strong>Live Demo</strong></a>
</p>

---

## 4. Java Multi-Agent Vehicle Routing System

<p>
  <img src="https://img.shields.io/badge/Status-Completed_Project-2EA44F?style=flat-square" alt="Completed project" />
  <img src="https://img.shields.io/badge/Focus-Multi--Agent_Systems-6F42C1?style=flat-square" alt="Multi-agent systems" />
  <img src="https://img.shields.io/badge/Language-Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" alt="Java" />
</p>

A Java multi-agent system for solving the Vehicle Routing Problem using the JADE agent framework.

The project models route planning as a cooperative agent problem. A master routing agent coordinates delivery agents, while several optimisation methods are used to build and improve vehicle routes.

### What I worked on

- Built the system with Java and JADE
- Created separate `MasterRoutingAgent` and `DeliveryAgent` components
- Implemented route generation and improvement strategies
- Added genetic algorithm and simulated annealing solvers
- Added nearest-neighbour and local-search optimisation
- Created route logging and visualisation components
- Organised the code into agent, core, and launcher layers

**Algorithms:** Genetic Algorithm · Simulated Annealing · Nearest Neighbour · Inter-route Local Search · Intra-route Local Search

**Stack:** Java · JADE · Multi-Agent Systems · Optimisation Algorithms · Route Visualisation

<p>
  <a href="https://github.com/islam-mamedov/vrp-mas-intelligent-system"><strong>View Repository</strong></a>
</p>

---

## Other Engineering Work

### Swinburne Campus App

A mobile-first campus platform that brings navigation, safety information, student support, events, and administration into one application.

I worked mainly on the admin console, emergency and exit-management features, support workflows, full-stack integration, and team coordination.

**Stack:** Next.js · React · TypeScript · Supabase · Tailwind CSS

[View repository](https://github.com/islam-mamedov/swinburne-app-group13)

---

## Technical Skills

### AI, LLMs and Machine Learning

<p>
  <img src="https://skillicons.dev/icons?i=py,pytorch,opencv,sklearn&perline=8" alt="AI and machine learning technologies" />
</p>

`Large Language Models` · `RAG` · `LLM Tool Calling` · `LangGraph` · `Agentic Workflows` · `Embeddings` · `Vector Search` · `Prompt Engineering` · `Computer Vision` · `Object Detection` · `Model Evaluation`

### Backend and Data

<p>
  <img src="https://skillicons.dev/icons?i=fastapi,postgres,supabase,docker&perline=8" alt="Backend and data technologies" />
</p>

`REST APIs` · `PostgreSQL` · `SQLAlchemy` · `ChromaDB` · `Pydantic` · `SQL Safety` · `Observability`

### Software Engineering

<p>
  <img src="https://skillicons.dev/icons?i=java,ts,nextjs,react,tailwind,git,github,linux&perline=8" alt="Software engineering technologies" />
</p>

`Java` · `Python` · `TypeScript` · `Next.js` · `React` · `Testing` · `Git` · `CI/CD` · `Linux` · `Clean Architecture`

---

## How I Work

I try to keep my AI projects practical and honest.

That means testing retrieval instead of assuming it works, checking whether an answer is actually supported, designing safe boundaries around tools and databases, and documenting the cases where a system can fail.

I care about building applications that are not only impressive in a demo, but also understandable, measurable, and useful.

---

## Open to Opportunities

I am interested in graduate roles across AI engineering, LLM applications, machine learning, computer vision, agentic systems, and backend or full-stack AI development.

<p align="center">
  <a href="mailto:islammamedov132004@gmail.com">
    <img src="https://img.shields.io/badge/Let's_Talk-Contact_Me-2EA44F?style=for-the-badge" alt="Contact Islam Mamedov" />
  </a>
</p>

<p align="center">
  <strong>Building AI systems that move from raw data to evidence, reasoning, and useful action.</strong>
</p>
'''

path = Path("/mnt/data/README_human_updated.md")
path.write_text(readme, encoding="utf-8")
print(f"Created {path} with {len(readme.splitlines())} lines.")
