<div align="center">

<img src="./assets/github-banner.png" alt="Islam Mamedov — Graduate AI Engineer" width="100%">

# Islam Mamedov

### Graduate AI Engineer focused on Computer Vision, RAG and Agentic AI

I build domain-specific AI systems that combine trained vision models, technical knowledge retrieval and LLM-based reasoning.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/YOUR-LINKEDIN)
[![Hugging Face](https://img.shields.io/badge/Hugging_Face-Live_Demos-FFD21E?style=for-the-badge\&logo=huggingface\&logoColor=black)](https://huggingface.co/Pace200413)
[![Email](https://img.shields.io/badge/Email-Contact_Me-EA4335?style=for-the-badge\&logo=gmail\&logoColor=white)](mailto:YOUR-EMAIL)

</div>

---

## About Me

I am a Computer Science graduate with a double major in **Artificial Intelligence and Cybersecurity** from Swinburne University of Technology.

My work focuses on applied AI systems that solve domain-specific problems rather than isolated model experiments. I have experience building complete workflows covering dataset preparation, model training, evaluation, retrieval, agent orchestration, user interfaces and deployment.

Currently, I am developing multimodal inspection systems that detect structural defects from images and generate repair recommendations grounded in engineering documentation.

* Based in Malaysia and open to relocation
* Targeting graduate and junior AI engineering roles
* Particularly interested in opportunities in the UAE and Abu Dhabi
* Languages: English and Russian

---

# Featured Project

## Agentic Multimodal Inspection Intelligence System

An end-to-end AI inspection platform that detects structural defects from images and uses a knowledge-grounded agent to explain the findings and recommend suitable repair actions.

<div align="center">

[![Live Demo](https://img.shields.io/badge/Launch_Live_Demo-FF4B4B?style=for-the-badge\&logo=huggingface\&logoColor=white)](https://huggingface.co/spaces/Pace200413/inspection-agent)
[![Repository](https://img.shields.io/badge/View_Repository-181717?style=for-the-badge\&logo=github\&logoColor=white)](https://github.com/islam-mamedov/inspection-agent)

</div>

<br>

<div align="center">
  <img src="./assets/inspection-demo.gif" alt="Inspection system demonstration" width="850">
</div>

### The problem

Structural inspection normally requires a combination of visual assessment and technical engineering knowledge. A detection model can identify visible damage, but it cannot independently explain the appropriate repair process or provide evidence for its recommendation.

This project combines computer vision, retrieval and agentic reasoning into one workflow.

### System workflow

```text
Structural Image
       ↓
YOLOv8 Defect Detection
       ↓
Defect Type, Confidence and Location
       ↓
LangGraph Agent
       ↓
Relevant Manual Sections Retrieved
       ↓
Grounded Inspection and Repair Recommendation
```

### Computer vision

* Trained a **YOLOv8s object-detection model** for crack, corrosion and spalling detection
* Prepared a custom dataset containing **1,770 images**
* Worked with approximately **5,897 labelled defect instances**
* Performed annotation checking, dataset cleaning, class validation and model evaluation
* Compared YOLO-based detection with RT-DETR experiments
* Generated annotated outputs containing bounding boxes, labels and confidence scores

### Agentic reasoning

* Built a stateful reasoning workflow using **LangGraph**
* Connected visual detections to a retrieval-augmented generation pipeline
* Grounded responses in the **USACE EM 1110-2-2002 concrete repair manual**
* Retrieved relevant technical passages before generating recommendations
* Designed the system to separate visual detection, retrieval and response generation
* Included supporting source context to reduce unsupported recommendations

### Product and deployment

* Developed an interactive interface for image upload and inspection
* Displayed detected defect types, confidence scores and annotated results
* Added structured inspection summaries and suggested actions
* Deployed the application publicly using **Hugging Face Spaces**
* Documented installation, architecture and system limitations in the repository

### Technology

`Python` · `PyTorch` · `Ultralytics YOLOv8` · `LangGraph` · `ChromaDB` · `OpenCV` · `Gradio` · `Hugging Face Spaces`

### Architecture

<div align="center">
  <img src="./assets/inspection-architecture.png" alt="Inspection system architecture" width="850">
</div>

---

# Selected Projects

<table>
<tr>
<td width="50%" valign="top">

### Structural Defect Detection

Computer-vision system for detecting cracks, corrosion and spalling from structural imagery.

**Highlights**

* Custom object-detection dataset
* YOLOv8 and RT-DETR experiments
* Bounding-box annotation validation
* Detection confidence and severity analysis
* Interactive model interface

**Stack**

`Python` `PyTorch` `YOLOv8` `RT-DETR` `OpenCV` `Gradio`

[View project →](YOUR-PROJECT-LINK)

</td>
<td width="50%" valign="top">

### Codebase RAG Assistant

Retrieval system designed to answer technical questions using information extracted from source code, documentation and project files.

**Highlights**

* Code-aware document ingestion
* Semantic chunking
* Vector retrieval
* Context-grounded answer generation
* Source references

**Stack**

`Python` `Embeddings` `ChromaDB` `LLMs` `RAG`

[View project →](YOUR-PROJECT-LINK)

</td>
</tr>

<tr>
<td width="50%" valign="top">

### Swinburne Campus Platform

A mobile-first campus system combining indoor navigation, student support, emergency tools, events and administrative content management.

**Highlights**

* Full-stack application architecture
* Campus and 360-degree navigation
* Emergency and support functionality
* Role-based administrative tools
* Supabase data management

**Stack**

`Next.js` `TypeScript` `React` `Supabase` `REST APIs`

[View project →](YOUR-PROJECT-LINK)

</td>
<td width="50%" valign="top">

### Published iOS Application

A production mobile application designed, developed and released through the Apple App Store.

**Highlights**

* Native iOS development
* Application lifecycle management
* Interface and feature implementation
* Production release experience

**Stack**

`Swift` `SwiftUI` `Xcode`

[View on the App Store →](YOUR-APP-STORE-LINK)

</td>
</tr>
</table>

---

# Technical Skills

### Artificial Intelligence

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square\&logo=python\&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square\&logo=pytorch\&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square\&logo=opencv\&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging_Face-FFD21E?style=flat-square\&logo=huggingface\&logoColor=black)

Computer Vision · Object Detection · Model Training · Dataset Preparation · Model Evaluation · Multimodal AI

### LLM Systems

![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square\&logo=langchain\&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square\&logo=langchain\&logoColor=white)

Retrieval-Augmented Generation · Agentic Workflows · Embeddings · Vector Databases · Document Processing · Grounded Generation

### Software Development

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square\&logo=typescript\&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square\&logo=nextdotjs\&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-F05138?style=flat-square\&logo=swift\&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square\&logo=git\&logoColor=white)

REST APIs · Full-Stack Development · Mobile Development · Supabase · Git · Linux

---

# Education

**Bachelor of Computer Science**
Double Major in Artificial Intelligence and Cybersecurity
**Swinburne University of Technology**

---

# Current Focus

I am currently expanding my portfolio with systems that demonstrate:

* Reliable agent orchestration
* Evaluation of RAG and agent outputs
* Multimodal AI workflows
* Database-operating AI agents
* Production-focused model deployment
* AI system observability and error handling

---

<div align="center">

## Let’s Connect

I am open to graduate and junior opportunities in AI engineering, computer vision, RAG and applied machine learning.

[![LinkedIn](https://img.shields.io/badge/Connect_on_LinkedIn-0A66C2?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/YOUR-LINKEDIN)
[![Email](https://img.shields.io/badge/Send_an_Email-EA4335?style=for-the-badge\&logo=gmail\&logoColor=white)](mailto:YOUR-EMAIL)

</div>
