

# Document Intelligence Agent Harness

**Company / Org:** Microsoft  
**Challenge Advisor:** Vikas Goyal, goyal3vikas@gmail.com  
**AI Coach:** Alexandra Ladyzhensky, alexandra.ladyzhensky@breakthroughtech.org  
**Program Manager:** Tyla Daniels, tyla.daniels@breakthroughtech.org

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
| September | Ingestion | Ingestion and indexing pipeline. Extract PDF/DOCX content, chunk it, retain metadata, generate embeddings, persist ChromaDB indexes, and verify repeatable indexing without duplicates. |
| October | Retrieval | Retrieval and grounded-answer pipeline. Implement top-k retrieval, evidence inspection, answer generation, citations, and refusal for insufficient evidence. Run early retrieval tests and a small Ragas baseline. |
| November | Integration | Integrated UI and final evaluation. Connect both pipelines in Streamlit, expose citations and intermediate results, compare configurations, run the complete evaluation set, fix weaknesses, and prepare the final demonstration and documentation. |

> **Note for the team:** Please create a GitHub Projects board in this repository to break these milestones into weekly tasks. Go to the **Projects** tab → **New project** → Choose **Board** → Add columns for each month.

---

## 📊 Dataset
**Name and Source:** Northstar University Knowledge Base  
**Format:** PDF, DOCX, TXT  
**Size:** under 1gb  
**Location:** data folder  

Team will use the Northstar University Knowledge Base, a fully synthetic collection of university policies and student-service documents created specifically for this project. All institutions, people, programs, contact details, and policies in the dataset are fictional; the corpus contains no personal or confidential information.

**The dataset contains**   
10 documents totaling 50 pages   
7 searchable PDF files and 3 DOCX files   
Approximately 5,200 words of extracted text   
9 current documents and 1 superseded policy   

**The documents cover**  
Academic integrity and use of generative AI  
Examinations, grading, and academic standing  
Admissions and enrollment  
Attendance and course participation  
Scholarships and financial aid  
Internships  
Library services  
Laboratory safety  
Student and campus services  

---

## 🛠️ Suggested Approach

**Recommended Technical Stack:**
- Python 3.11  
- `venv` and `pip`  
- A pinned `requirements.txt`  
- Streamlit for the user interface  
- Ollama for local model execution  
- `qwen2.5:3b` as the default generation model  
- `nomic-embed-text` as the embedding model  
- ChromaDB in persistent embedded mode  
- PyMuPDF for PDF text extraction  
- `python-docx` for DOCX text extraction  
- LangGraph for the required small workflow  
- Ragas for systematic RAG evaluation  
- pytest for automated testing  

**Evaluation Metrics:**
- [e.g., Accuracy, Precision/Recall, RMSE, BLEU score]
  
---
## 📚 Resources to Get Started

The following resources are organized around the three project milestones. Students are not expected to read every page. Begin with the quick-start resources and consult the reference documentation as needed.

### Background Reading

- [What is Retrieval-Augmented Generation (RAG)?](https://www.ibm.com/think/topics/retrieval-augmented-generation) — An introductory explanation of retrieval, grounding, and generation.
- [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401) — The original RAG paper. The abstract and architecture diagram are sufficient for initial reading.
- [Embeddings — Google Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course/embeddings) — An introduction to representing text as vectors and measuring similarity.
- [Ragas Concepts](https://docs.ragas.io/en/stable/concepts/) — An overview of systematic evaluation for RAG applications.

### September: Ingestion and Indexing

- [Python Virtual Environments](https://docs.python.org/3.11/tutorial/venv.html) — Creating and managing the project environment.
- [PyMuPDF Tutorial](https://pymupdf.readthedocs.io/en/latest/tutorial.html) — Extracting text and page metadata from PDF files.
- [python-docx Quick Start](https://python-docx.readthedocs.io/en/latest/user/quickstart.html) — Reading paragraphs and tables from DOCX files.
- [Ollama Quick Start](https://docs.ollama.com/quickstart) — Installing Ollama and running models locally.
- [nomic-embed-text](https://ollama.com/library/nomic-embed-text) — The local embedding model used by this project.
- [Chroma Getting Started](https://docs.trychroma.com/docs/overview/getting-started) — Creating collections, storing embeddings and metadata, and running local similarity searches.

### October: Retrieval and Grounded Answers

- [Ollama Python Library](https://github.com/ollama/ollama-python) — Calling local generation and embedding models from Python.
- [qwen2.5:3b](https://ollama.com/library/qwen2.5:3b) — The default local generation model used by this project.
- [Querying Chroma Collections](https://docs.trychroma.com/docs/querying-collections/query-and-get) — Retrieving top-k results and applying metadata filters.
- [LangGraph Graph API](https://docs.langchain.com/oss/python/langgraph/graph-api) — Building the small retrieve → assess evidence → answer or refuse workflow.
- [Prompt Engineering Guide](https://www.promptingguide.ai/) — A practical introduction to prompts, grounding instructions, and structured responses.

### November: User Interface, Testing, and Evaluation

- [Streamlit Get Started](https://docs.streamlit.io/get-started) — Building and running the local application.
- [Streamlit Chat Elements](https://docs.streamlit.io/develop/api-reference/chat) — Creating a question-and-answer interface.
- [Ragas Get Started](https://docs.ragas.io/en/stable/getstarted/) — Running systematic RAG evaluations.
- [Ragas Metrics](https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/) — Reference material for faithfulness, answer relevancy, context precision, and context recall.
- [pytest Getting Started](https://docs.pytest.org/en/stable/getting-started.html) — Writing and running automated tests.

### Code and Collaboration Tools

- [Visual Studio Code Python Tutorial](https://code.visualstudio.com/docs/python/python-tutorial)
- [GitHub Projects Documentation](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects)
- [GitHub Pull Request Documentation](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests)
- [Mermaid Live Editor](https://mermaid.live/) — Creating architecture and workflow diagrams.

> **Local-only requirement:** Examples in some external documentation may use hosted models or API keys. For this project, use Ollama with `qwen2.5:3b` and `nomic-embed-text`. No paid cloud account or external model API is required.  

## 🤝 How We'll Work Together

**Official check-ins:** During our biweekly 45-minute AI Studio Lab Section meeting block (2nd and 4th week of every month)

 **Other ways to reach out to me with questions:** 
* [e.g., Your team's channel within Break Through Tech’s Discord space]
* [e.g., Email; please copy your teammates and AI Studio Coach]
* [e.g., Request a team check-in on Zoom]
* [Note: I will aim to respond within 48 hours. Please reach out to your AI Studio Coach with urgent questions.]

---

## 🚀 Getting Started

1. **Review this overview document** and note any questions for our first meeting
2. **Begin reviewing the dataset** using the link above
3. **Read the GitHub Projects documentation** [here](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects)

I’m excited to work with you!

---

## ❓ Questions?

Please bring any questions to our first meeting during the week of August 24th (Break Through Tech’s Bridge to Studio - Session C). 
