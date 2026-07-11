<p align="center">
  <img src="./assets/header-banner.png" alt="Islam Mamedov — AI Engineer" width="100%" />
</p>

<h1 align="center">Islam Mamedov</h1>

<h3 align="center">
  Graduate AI Engineer · Computer Vision · Agentic Systems · RAG
</h3>

<p align="center">
  I build practical AI systems that combine perception, retrieval, reasoning, evaluation, and software engineering.
</p>

<p align="center">
  <a href="https://github.com/islam-mamedov">
    <img src="https://img.shields.io/badge/GitHub-islam--mamedov-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub profile" />
  </a>
  <a href="mailto:islammamedov132004@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email Islam Mamedov" />
  </a>
  <a href="https://huggingface.co/islam-mamedov">
    <img src="https://img.shields.io/badge/Hugging_Face-Live_AI_Demos-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face profile" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Based_in-Malaysia-0A66C2?style=flat-square" alt="Based in Malaysia" />
  <img src="https://img.shields.io/badge/Open_to-AI_%26_ML_Roles-2EA44F?style=flat-square" alt="Open to AI and machine learning roles" />
  <img src="https://img.shields.io/badge/Open_to-Relocation-8A2BE2?style=flat-square" alt="Open to relocation" />
</p>

---

## About Me

I am a Computer Science graduate specialising in **Artificial Intelligence and Cybersecurity**. I focus on building complete AI applications rather than isolated notebooks or simple chatbot wrappers.

My projects combine:

* computer vision and object detection
* retrieval-augmented generation
* agentic planning and tool use
* evaluation and failure analysis
* backend APIs, databases, and user interfaces
* testing, security controls, and reproducible workflows

I am currently seeking graduate opportunities in **AI Engineering, Machine Learning Engineering, and Software Engineering**.

---

## Engineering Highlights

* Built multimodal systems that connect visual detection with evidence-grounded language generation
* Implemented conditional agent workflows with retrieval grading, query rewriting, validation, and refusal handling
* Evaluated RAG systems with labelled benchmarks instead of relying only on demonstration examples
* Designed safe SQL-agent workflows with AST-based query inspection, read-only execution, and self-repair
* Developed full-stack applications using Python, FastAPI, PostgreSQL, Next.js, React, TypeScript, and Supabase
* Documented limitations, failure cases, and engineering trade-offs alongside successful results

---

# Featured Projects

## 1. Concrete Inspection Agent

<p>
  <a href="https://github.com/islam-mamedov/inspection-agent">
    <img src="https://img.shields.io/badge/Status-Deployed_Demo-2EA44F?style=flat-square" alt="Deployed demo" />
  </a>
  <img src="https://img.shields.io/badge/Type-Multimodal_AI-6F42C1?style=flat-square" alt="Multimodal AI" />
  <img src="https://img.shields.io/badge/License-MIT-007EC6?style=flat-square" alt="MIT License" />
</p>

A multimodal AI agent for concrete-defect detection and evidence-grounded repair guidance.

<p align="center">
  <a href="https://huggingface.co/spaces/islam-mamedov/inspection-agent">
    <img src="https://raw.githubusercontent.com/islam-mamedov/inspection-agent/main/assets/inspection-agent-demo.png" alt="Concrete Inspection Agent interface" width="100%" />
  </a>
</p>

### What I engineered

* Fine-tuned a YOLOv8 detector for **crack, corrosion, and spalling**
* Connected image findings to a conditional **LangGraph** reasoning workflow
* Built a ChromaDB knowledge base from **USACE EM 1110-2-2002**
* Preserved section metadata for evidence-grounded citations
* Added passage grading and query rewriting for weak retrieval results
* Implemented unsupported-question refusal rather than forcing an answer
* Evaluated retrieval, citations, faithfulness, and refusal behaviour

### Verified project evidence

| Area                  |  Result |
| --------------------- | ------: |
| Training images       |   1,770 |
| Annotated objects     |   5,897 |
| Defect classes        |       3 |
| Knowledge-base chunks |     292 |
| Evaluation questions  |      35 |
| Retrieval hit rate    | 28 / 28 |
| Citation validity     | 33 / 33 |
| Faithfulness          | 31 / 32 |
| Refusal correctness   | 33 / 35 |

**Stack:** Python · YOLOv8 · LangGraph · LangChain · ChromaDB · Gradio · Hugging Face Spaces

<p>
  <a href="https://github.com/islam-mamedov/inspection-agent"><strong>Source Code</strong></a>
  ·
  <a href="https://huggingface.co/spaces/islam-mamedov/inspection-agent"><strong>Live Demo</strong></a>
</p>

---

## 2. InsightForge

<p>
  <a href="https://github.com/islam-mamedov/insightforge">
    <img src="https://img.shields.io/badge/Status-Active_Development-F59E0B?style=flat-square" alt="Active development" />
  </a>
  <img src="https://img.shields.io/badge/Type-Agentic_Data_Analysis-6F42C1?style=flat-square" alt="Agentic data analysis" />
  <img src="https://img.shields.io/badge/Tests-103_Passing-2EA44F?style=flat-square" alt="103 tests" />
</p>

An autonomous AI data analyst that investigates business questions against a PostgreSQL database.

<p align="center">
  <a href="https://github.com/islam-mamedov/insightforge">
    <img src="https://raw.githubusercontent.com/islam-mamedov/insightforge/main/docs/demo.png" alt="InsightForge investigation interface" width="100%" />
  </a>
</p>

### What I engineered

* Built an eight-stage investigation pipeline:
  **interpret → plan → discover schema → generate SQL → inspect → execute → validate → explain**
* Used a deterministic planner rather than delegating every decision to an LLM
* Added schema discovery so the model sees only relevant tables
* Parsed generated SQL with **SQLGlot** instead of relying on regex filters
* Blocked writes, DDL, unsafe functions, disallowed tables, and PII columns
* Executed queries inside read-only database transactions
* Added automatic query repair for failed SQL, with a maximum of three attempts
* Validated results for empty outputs, null-only columns, and join fan-out
* Separated observed facts from inferences in the final explanation
* Added token, latency, cost, and audit tracking

### Verified project evidence

| Area                        |                               Result |
| --------------------------- | -----------------------------------: |
| Pipeline stages             |                                    8 |
| Automated tests             |                                  103 |
| Synthetic database size     |                        ~650,000 rows |
| Planted benchmark anomalies |                                    6 |
| Maximum SQL repair attempts |                                    3 |
| Database protection         | AST inspection + read-only execution |

**Stack:** Python · FastAPI · PostgreSQL · SQLAlchemy · SQLGlot · Docker · Pydantic · LLM Tool Calling

<p>
  <a href="https://github.com/islam-mamedov/insightforge"><strong>Source Code</strong></a>
</p>

---

## 3. FastAPI Codebase Q&A

<p>
  <a href="https://github.com/islam-mamedov/codebase-rag">
    <img src="https://img.shields.io/badge/Status-Deployed_Demo-2EA44F?style=flat-square" alt="Deployed demo" />
  </a>
  <img src="https://img.shields.io/badge/Type-Evaluation--Driven_RAG-6F42C1?style=flat-square" alt="Evaluation-driven RAG" />
  <img src="https://img.shields.io/badge/Refusal_Accuracy-7%2F7-2EA44F?style=flat-square" alt="7 out of 7 refusal accuracy" />
</p>

An evaluation-driven RAG system for exploring FastAPI source code, documentation, and resolved GitHub issues.

<p align="center">
  <a href="https://huggingface.co/spaces/islam-mamedov/fastapi-codebase-qa">
    <img src="https://raw.githubusercontent.com/islam-mamedov/codebase-rag/main/assets/codebase-rag-demo.gif" alt="FastAPI Codebase Q&A demo" width="100%" />
  </a>
</p>

### What I engineered

* Ingested source code, English documentation, and closed GitHub issues
* Created AST-aware code chunks using Tree-sitter
* Preserved symbols, file paths, line ranges, and content-type metadata
* Compared dense retrieval, BM25 hybrid search, reranking, and query rewriting
* Selected the simplest production retriever based on measured performance
* Generated answers with file, symbol, and line-level evidence
* Added evidence-aware refusal behaviour for unsupported questions
* Built resumable ingestion, evaluation caching, retry logic, and regression tests

### Verified project evidence

| Area                          | Result |
| ----------------------------- | -----: |
| Indexed source files          |     46 |
| Documentation files           |    161 |
| Closed GitHub issues          |    175 |
| Total chunks                  |  1,352 |
| Labelled evaluation questions |     42 |
| Recall@5                      |   0.91 |
| Mean Reciprocal Rank          |   0.71 |
| Faithfulness                  |   0.89 |
| Correctness                   |   0.91 |
| Refusal accuracy              |  7 / 7 |

**Stack:** Python · Streamlit · ChromaDB · BGE Embeddings · Tree-sitter · PyGithub · Pytest · Hugging Face Spaces

<p>
  <a href="https://github.com/islam-mamedov/codebase-rag"><strong>Source Code</strong></a>
  ·
  <a href="https://huggingface.co/spaces/islam-mamedov/fastapi-codebase-qa"><strong>Live Demo</strong></a>
</p>

---

## Other Engineering Work

### Swinburne Campus App

A mobile-first campus platform covering navigation, emergency support, student services, events, and administration.

**My focus:** admin console, safety and exit-management workflows, support features, full-stack integration, and team leadership.

**Stack:** Next.js · React · TypeScript · Supabase · Tailwind CSS

[View repository](https://github.com/islam-mamedov/swinburne-app-group13)

---

## Technical Stack

### AI and Machine Learning

<p>
  <img src="https://skillicons.dev/icons?i=py,pytorch,opencv,sklearn&perline=8" alt="AI and machine learning technologies" />
</p>

`Computer Vision` · `Object Detection` · `RAG` · `Embeddings` · `Vector Search` · `Agentic Workflows` · `Model Evaluation` · `LLM Tool Use`

### Backend and Data

<p>
  <img src="https://skillicons.dev/icons?i=fastapi,postgres,supabase,docker&perline=8" alt="Backend and data technologies" />
</p>

`REST APIs` · `PostgreSQL` · `SQLAlchemy` · `ChromaDB` · `Pydantic` · `SQL Safety` · `Observability`

### Frontend and Software Engineering

<p>
  <img src="https://skillicons.dev/icons?i=ts,nextjs,react,tailwind,git,github,linux&perline=8" alt="Frontend and software engineering technologies" />
</p>

`TypeScript` · `Next.js` · `React` · `Testing` · `Git` · `CI/CD` · `Linux` · `Clean Architecture`

---

## GitHub Contributions

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=islam-mamedov&theme=github_dark" alt="Islam Mamedov GitHub contribution summary" width="100%" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=islam-mamedov&theme=github-compact&hide_border=true&area=true&custom_title=Contribution%20Activity" alt="Islam Mamedov GitHub contribution activity graph" width="100%" />
</p>

---

## How I Approach AI Engineering

```python
class AIEngineeringPrinciples:
    build_complete_systems = True

    priorities = [
        "ground outputs in evidence",
        "measure retrieval and model quality",
        "design for failure and refusal",
        "protect data and execution boundaries",
        "make results inspectable",
        "document limitations honestly",
    ]

    goal = "Build AI systems that are useful, testable, secure, and explainable."
```

---

## Open to Opportunities

I am interested in graduate roles involving:

* AI and machine learning engineering
* computer vision
* RAG and LLM applications
* agentic systems
* backend and full-stack AI development

<p align="center">
  <a href="mailto:islammamedov132004@gmail.com">
    <img src="https://img.shields.io/badge/Let's_Build_Something-Contact_Me-2EA44F?style=for-the-badge" alt="Contact Islam Mamedov" />
  </a>
</p>

<p align="center">
  <strong>Building AI systems that move from perception to evidence, reasoning, and action.</strong>
</p>
* Grades retrieved evidence and rewrites weak searches
* Produces section-level citations and avoids unsupported recommendations

**Stack:** Python · YOLOv8 · LangGraph · RAG · Gradio

[Source Code](https://github.com/islam-mamedov/inspection-agent) · [Live Demo](https://huggingface.co/spaces/islam-mamedov/inspection-agent)

</td>
<td width="50%" valign="top">

### [InsightForge](https://github.com/islam-mamedov/insightforge)

An autonomous AI data analyst that investigates business questions against a SQL database.

**What it does**

* Plans multi-step analytical investigations
* Generates and self-repairs SQL queries
* Validates calculations before presenting conclusions
* Shows the evidence behind each answer
* Separates planning, execution, validation, and reporting

**Stack:** Python · FastAPI · PostgreSQL · LLM Agents · SQL

[Source Code](https://github.com/islam-mamedov/insightforge)

</td>
</tr>

<tr>
<td width="50%" valign="top">

### [Codebase RAG](https://github.com/islam-mamedov/codebase-rag)

An evaluation-driven RAG system for exploring source code, documentation, and GitHub issues.

**What it does**

* Parses code-aware chunks instead of splitting files blindly
* Retrieves across code, documentation, and issue discussions
* Produces grounded answers with source citations
* Includes retrieval and answer-quality evaluation
* Provides an interactive Streamlit interface

**Stack:** Python · FastAPI · Semantic Search · RAG · Streamlit

[Source Code](https://github.com/islam-mamedov/codebase-rag)

</td>
<td width="50%" valign="top">

### [Swinburne Campus App](https://github.com/islam-mamedov/swinburne-app-group13)

A mobile-first campus platform combining navigation, safety, support, events, and administration.

**What it includes**

* Campus navigation and location discovery
* Emergency and safety workflows
* Support directory, service status, and FAQs
* Event management and admin CRUD tools
* Role-based access and Supabase-backed data

**Stack:** Next.js · React · TypeScript · Supabase · Tailwind CSS

[Source Code](https://github.com/islam-mamedov/swinburne-app-group13)

</td>
</tr>
</table>

---

## Technical Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=py,pytorch,opencv,sklearn,fastapi,postgres,docker,git,github,linux,ts,nextjs,react,supabase,tailwind&perline=8" alt="Technical skills" />
</p>

<p align="center">
  <strong>AI:</strong> Computer Vision · Object Detection · RAG · Agentic Workflows · Embeddings · Model Evaluation<br/>
  <strong>Engineering:</strong> REST APIs · PostgreSQL · Vector Search · Full-Stack Development · Git · Docker
</p>

---

## GitHub Contributions

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=islam-mamedov&theme=github_dark" alt="Islam Mamedov GitHub contribution summary" width="100%" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=islam-mamedov&theme=github-dark-blue&hide_border=true" alt="Islam Mamedov GitHub contribution streak" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=islam-mamedov&theme=github-compact&hide_border=true&area=true&custom_title=Contribution%20Activity" alt="Islam Mamedov contribution activity graph" width="100%" />
</p>

---

## Current Focus

```python
class CurrentFocus:
    building = [
        "multimodal AI agents",
        "evaluation-driven RAG systems",
        "autonomous data-analysis workflows",
        "production-ready AI applications",
    ]

    principle = "Build systems that are useful, grounded, testable, and explainable."
```

---

<p align="center">
  <strong>Building AI systems that move from perception to evidence, reasoning, and action.</strong>
</p>

<p align="center">
  <a href="https://github.com/islam-mamedov?tab=repositories">Explore my repositories</a>
</p>
