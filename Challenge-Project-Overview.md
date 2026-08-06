---

> ## Challenge Advisor: Update & Finalize Your Project Overview
>
> > 💡 **These grey text instructions are just for you, the team's Challenge Advisor; please delete them once you have completed the steps below.**
>
> We've pre-populated this Challenge Project Overview page — which is what will be shared with your Break Through Tech student team in August — using the details from your submission form. You should have received an email inviting you to join this repo as a Collaborator, enabling you to add files and make edits.
> 
> In order for your project to be finalized and assigned to a team, please:
> 1. **Review all sections below** and update or expand any content as needed, making sure to address the SME Feedback in the section immediately below. Look for square brackets to find the places below that require additional inputs from you (e.g., "About [Company / Org Name]").
> 2. **Add your dataset** to the [data folder](data) in this repo.
> 3. **Close the Issue assigned to you in this repo** to let us know that you have made your edits and the overview page is ready for final review. You can do this by going to the _Issues_ tab in the top left section of the menu above, add a comment that says "CA review complete", and click the button to Close the Issue. 
>
> If you're unfamiliar with how to edit a page like this in GitHub, check out [this tutorial](https://ubc-lib-geo.github.io/gis-workshop-waml-template/content/handson/edit-readme.html) for a quick overview (start with step 2 and only edit this page), and [this guide](https://ubc-lib-geo.github.io/gis-workshop-waml-template/content/markdown.html) on how to use Markdown to compose text.
>
>
> ❌ Remember that this is a public repo. Do NOT include: Proprietary data, PII, API keys, credentials, or anything confidential.

---

## 📋 BTT Internal Evaluation Notes
*(This section is for BTT staff and CAs only — remove before sharing with students)*

### Technical Vetting
| Check | Status | Notes |
| :--- | :--- | :--- |
| Python Compatibility | 🟢 | Project relies on LangChain/LlamaIndex stack, which is standard Python. However, managing agentic flows often drifts into complex orchestrations that may overcomplicate for the student base. |
| Data Readiness | 🟡 | Unstructured enterprise documents (PDF/Word) inherently require intensive OCR and chunking logic. Without pre-cleaned, ingested data, students risk spending the bulk of the 12 weeks on pipeline engineering rather than RAG optimization. |
| Resource Check | 🟢 | Resource requirements are low (embedding models are small/local), provided students stick to Hugging Face local models rather than paid OpenAI APIs. |

### Internal Scores
- **Student Fit Score:** 6/10
- **Technical Depth Score:** 8/10
- **Overall Recommendation:** REVISE

### Advisor Feedback Draft
The proposal offers a strong, high-visibility outcome in RAG. To ensure success, first, explicitly mandate the use of Ragas or TruLens for systematic evaluation to avoid subjective testing. Second, replace the 'Agentic' requirement with a focus on a robust Retrieval-Augmented Generation pipeline. Reserve Agentic AI for the stretch goals, as agents introduce unpredictable execution loops that can be particularly difficult to debug given the AI Studio program's timeframe and resource constraints.

---

# Document Intelligence Agent Harness

**Company / Org:** Microsoft  
**Challenge Advisor:** Vikas Goyal, goyal3vikas@gmail.com  
**AI Coach:** Alexandra Ladyzhensky, alexandra.ladyzhensky@breakthroughtech.org

**Program:** Break Through Tech AI Studio - Fall 2026  

---

## 🏢 About Microsoft
Microsoft is a global technology leader dedicated to empowering every person and organization on the planet to achieve more through innovation in software, cloud computing, and AI services. This project aligns with Microsoft’s objective to modernize enterprise information retrieval, specifically focusing on helping organizations derive actionable insights from massive, unstructured data repositories.

---

## 🎯 The Challenge
### Project Summary
This project challenges students to develop an enterprise-ready document intelligence solution that ingests, indexes, and retrieves information from complex organizational documents. By leveraging RAG frameworks and document parsing, the team will transform static files like PDFs and Word documents into a highly discoverable and trustworthy knowledge base.

### Success Criteria
Functional completeness, Answer quality (factual grounding), Citation accuracy, Trustworthiness, User experience, System performance, Enterprise readiness.

### Project Milestones
Use these milestones to guide your work. Your team will create a GitHub Projects board to track tasks within each milestone.

| Month | Milestone | Key Activities |
| :--- | :--- | :--- |
| September | Harness Architecture, Ingestion & Baseline Evaluation | • Define standard agent interfaces and contract schemas for document processing tasks.<br>• Set up document ingestion pipelines for synthetic and public PDF corpora.<br>• Establish baseline benchmarking suite to measure tool-calling accuracy, retrieval precision, and task execution times.<br>• Implement basic single-agent document parsing workflows. |
| October | Multi-Agent Orchestration & Evaluation Framework | • Construct an agent evaluation harness capable of orchestrating multi-agent interactions.<br>• Implement tool integration testing for document analysis, entity extraction, and table parsing.<br>• Evaluate multi-agent orchestration frameworks (e.g., AutoGen, CrewAI, or LangGraph) on complex document sets.<br>• Conduct benchmark stress-tests on agent reasoning and failure recovery loops. |
| November / December | System Optimization, Interactive UI & Capstone Deliverables | • Optimize agent harness efficiency, reduce tool-calling latency, and mitigate error propagation.<br>• Build an interactive Streamlit dashboard to monitor live agent execution traces, tool calls, and document evaluation metrics.<br>• Finalize clean, reproducible GitHub repository with full harness code, documentation, and stakeholder presentation deck. |

### Stretch Goals
* **Autonomous Error-Recovery Middleware:** Build an intelligent interception layer that detects failed tool executions or ungrounded responses and automatically re-routes queries with corrected tool arguments.
* **Cross-Agent Memory Pipeline:** Implement shared context memory across specialized document agents to maintain state during multi-step reasoning over large multi-page document collections.
* **Plug-and-Play Agent Evaluation Benchmark Suite:** Package the evaluation harness into a modular Python package enabling developers to benchmark custom document agent architectures against standard test cases.
> **Note for the team:** Please create a GitHub Projects board in this repository to break these milestones into weekly tasks. Go to the **Projects** tab → **New project** → Choose **Board** → Add columns for each month.

---

## 📊 Dataset
**Name and Source:** Enterprise Document Suite (Synthetic/Public Open Source)  
**Format:** PDF, DOCX, TXT  
**Size:** under 1gb  
**Location:** To be initialized in the repository data folder.

### Key Details
- Enterprise documents (PDFs, Word documents, and other unstructured content). The team will generate synthetic data or use a publicly available one.
- Focus on consistent metadata extraction and normalization across varying document structures to ensure high-quality retrieval accuracy.

---

## 🛠️ Suggested Approach
**ML Problem Type:** NLP & RAG / Multi-Agent Systems  
**Recommended Libraries:**
- Vector embeddings (Sentence-Transformers)
- Semantic search (FAISS / ChromaDB)
- Retrieval-augmented generation (LangChain / LlamaIndex)
- AI agents (LangGraph or equivalent orchestration)
**Evaluation Metrics:** Ragas (Faithfulness, Answer Relevance, Context Precision), Latency, and Factual Grounding rate.

---

## 📚 Resources to Get Started
The following resources will help your team understand the problem space and potential technical approaches for this project:
**Background Reading:**
- Microsoft Research Blog: Advances in Document Intelligence and Large Language Models.
**Technical Tutorials:**
- LangChain Documentation: "RAG from Scratch" video series and documentation.
**Code Examples:**
- Sample GitHub repositories showcasing LlamaIndex ingestion pipelines for PDF documents.

---

## 🤝 How We'll Work Together
**Check-ins:** During our biweekly 60-min AI Studio Lab Section meeting block (2nd and 4th week of every month)  
**Communication:** Microsoft Teams or Slack  
**Response time:** 24-48 hours during business days  
**Recommended Tools:**
- **Coding:** Google Colab Free Tier  
- **Collaboration:** GitHub, Notion  
- **Virtual Meetings:** Zoom, Google Meet  

---

## 🚀 Getting Started
1. **Review this overview document** and note any questions for our first meeting.
2. **Begin reviewing the dataset** using the link provided in the Dataset section.
3. **Read the GitHub Projects documentation** [here](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects).

I'm excited to work with you!

---

## ❓ Questions?
Please bring any questions to our first meeting during the week of August 24th (Break Through Tech's Bridge to Studio - Session B).
