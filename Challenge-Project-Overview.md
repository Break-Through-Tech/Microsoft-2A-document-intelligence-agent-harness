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
Microsoft is a global technology leader dedicated to empowering every person and organization on the planet to achieve more through innovation in software, cloud computing, and AI services. 

---

## 🎯 The Challenge
### Project Summary
In this project, you will use enterprise documents (PDFs, Word documents, and other unstructured content) and modern AI techniques including vector embeddings, semantic search, retrieval-augmented generation (RAG), and AI agents to build an enterprise-ready document intelligence solution that can ingest, index, retrieve, and answer questions grounded in organizational knowledge. This will help any company address the challenge of making large volumes of unstructured information easily discoverable, trustworthy, and actionable for employees.

### Success Criteria

Success will be evaluated across several dimensions:

- Functional completeness: Documents are automatically ingested, parsed, indexed, and searchable through a conversational interface.
- Answer quality: The system retrieves relevant information and generates responses that are factually grounded in the uploaded documents.
- Citation accuracy: Every response includes references to the source document and relevant section or page, allowing users to verify the answer.
- Trustworthiness: The system appropriately indicates when sufficient information is unavailable rather than generating unsupported responses.
- User experience: Users can easily upload documents, manage the knowledge base, and interact with the system using natural language.
- System performance: Responses are returned within an acceptable time, and new or updated documents are reflected in the knowledge base after ingestion.
- Enterprise readiness: The architecture is modular, well documented, and designed so local components (LLMs, vector databases, storage) can be replaced with enterprise services without major redesign.

### Stretch Goals

_Here are some ways solution can be extended:_

- Multi-document reasoning: Answer questions that require synthesizing information across multiple documents.
- Advanced document workflows: Support summarization, document comparison, key information extraction, and action item generation.
- Agentic capabilities: Enable the agent to plan and execute multi-step document tasks rather than responding to a single query.
- Access control: Implement role-based document permissions to ensure users can only retrieve information from authorized documents.
- Evaluation framework: Develop automated benchmarks to measure retrieval quality, answer accuracy, citation quality, and hallucination rates.
- Enterprise integrations: Replace local storage with cloud services or integrate with enterprise repositories such as SharePoint or OneDrive.
- Observability and governance: Add logging, performance metrics, prompt injection detection, content safety checks, and audit trails.
- Multimodal document support: Extend the solution to process tables, images, scanned PDFs (OCR), and diagrams.

### Project Milestones
Use these milestones to guide your work. Your team will create a GitHub Projects board to track tasks within each milestone.

| Month | Milestone | Key Activities |
|---|---|---|
| September | [Title] | Build the core document ingestion and retrieval pipeline. |
| October | [Title] | Transform retrieval into an intelligent document agent. |
| November | [Title] | Make the solution enterprise-ready and demonstrate its business value. |

> **Note for the team:** Please create a GitHub Projects board in this repository to break these milestones into weekly tasks. Go to the **Projects** tab → **New project** → Choose **Board** → Add columns for each month.

---

## 📊 Dataset
**Name and Source:** [TBD]
**Format:** PDF, DOCX, TXT  
**Size:** under 1gb  
**Location:** [TBD]


### Key Details
- [Brief description of what's in the data]
- [Any known limitations or preprocessing needed]
- [Link to data dictionary or documentation, if available]

---

## 🛠️ Suggested Approach

**ML Problem Type:** Natural Language Processing (NLP),Large Language Models (LLMs)/ Generative AI

**Recommended Libraries:**
- [e.g., pandas, scikit-learn, TensorFlow, Hugging Face]

**Evaluation Metrics:**
- [e.g., Accuracy, Precision/Recall, RMSE, BLEU score]
  
---
## 📚 Resources to Get Started

The following resources will help your team understand the problem space and potential technical approaches for this project:

**Background Reading:**
- [e.g., Link to an article or blog post about the problem domain]
- [e.g., Link to an industry report or case study]

**Technical Tutorials:**
- [e.g., Link to a free tutorial on the ML technique(s) involved]
- [e.g., Link to documentation for a key library or tool]

**Code Examples:**
- [e.g., Link to a relevant GitHub repo]
- [e.g., Link to a sample implementation or starter code]

**Other:**
- [Links to any additional resources — e.g., papers, videos, podcasts, etc.]

*Feel free to explore beyond these, and share anything interesting you find with me!*

---

## 🤝 How We'll Work Together

**Official check-ins:** During our biweekly 45-minute AI Studio Lab Section meeting block (2nd and 4th week of every month)

 **Other ways to reach out to me with questions:** 
* [e.g., Your team's channel within Break Through Tech’s Discord space]
* [e.g., Email; please copy your teammates and AI Studio Coach]
* [e.g., Request a team check-in on Zoom]
* [Note: I will aim to respond within 48 hours. Please reach out to your AI Studio Coach with urgent questions.]

> 💡 **Challenge Advisor: Please update the above based on your availability and preference. If you are not able to answer questions or meet with fellows outside of the biweekly Lab Section check-ins, simply write in "N/A (only available during the official check-in times)"**

**Recommended free coding / collaboration tools**
* […]
* […]

---

## 🚀 Getting Started

1. **Review this overview document** and note any questions for our first meeting
2. **Begin reviewing the dataset** using the link above
3. **Read the GitHub Projects documentation** [here](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects)

I’m excited to work with you!

---

## ❓ Questions?

Please bring any questions to our first meeting during the week of August 24th (Break Through Tech’s Bridge to Studio - Session C). 
