<div align="center">
  <h1>Building Your Second Brain AI Assistant Using Agents, LLMs and RAG</h1>
  
  
</div>

</br>

<p align="center">
  <a href="https://decodingml.substack.com/p/build-your-second-brain-ai-assistant">
    <img src="static/system_architecture.png" alt="Architecture" width="600">
  </a>
</p>




### So What Is the Second Brain AI Assistant?

The Second Brain, a concept by Tiago Forte, is your personal knowledge base of notes, ideas, and resources. Our AI Assistant leverages this knowledge to answer questions, summarize documents, and provide insights.

Imagine asking your AI Assistant to recommend agent courses, list top PDF parsing tools, or summarize LLM optimization methods - all based on your research, without manually searching through notes.

While we use Notion for this course, the code is adaptable to other sources like Google Drive or Calendar. We'll provide our curated AI/ML resource list from Notion, covering GenAI, LLMs, RAG, MLOps, and more. **No Notion account needed** - but if you want to use yours, our flexible pipeline supports any Notion database.

<table>
  <tr>
    <td align="center" width="50%">
        <img src="static/rag_feature_pipeline_architecture.png" alt="RAG Feature Pipeline Architecture" width="100%">
    </td>
    <td align="center" width="50%">
        <img src="static/agentic_rag_architecture.png" alt="Agentic RAG Architecture" width="100%">
    </td>
  </tr>
</table>


### What W 'll Do:

- Build an agentic RAG system powered by your Second Brain
- Design production-ready LLM architectures
- Apply LLMOps and software engineering best practices
- Fine-tune and deploy LLMs
- Use industry tools: OpenAI, Hugging Face, MongoDB, ZenML, Opik, Comet, Unsloth, and more
- LLM system architecture (FTI) and MLOps best practices
- Pipeline orchestration and tracking with ZenML
- LLMOps and RAG evaluation using Opik
- Large-scale web crawling and content normalization
- Quality scoring with LLMs and heuristics
- Dataset generation through distillation
- Llama model fine-tuning with Unsloth and Comet
- Serverless model deployment to Hugging Face
- Advanced RAG with contextual or parent retrieval and vector search
- Agent building using smolagents
- Modern Python tooling (uv, ruff)


<table>
  <tr>
    <td align="center" width="50%">
        <img src="static/dataset_generation_pipeline_architecture.png" alt="Dataset Generation Pipeline Architecture" width="100%">
    </td>
    <td align="center" width="50%">
        <img src="static/training_pipeline_architecture.png" alt="Training Pipeline Architecture" width="100%">
    </td>
  </tr>
</table>


------

<div align="center">
  <h1>🧠 Building Your Second Brain AI Assistant</h1>
  <h3>Using Agents, RAG, and LLMOps</h3>
  
  <p>
    <a href="#about">About</a> •
    <a href="#architecture">Architecture</a> •
    <a href="#features">Features</a> •
    <a href="#tech-stack">Tech Stack</a> •
    <a href="#getting-started">Getting Started</a>
  </p>
</div>

---


## 🏗️ Architecture {#architecture}

### System Overview

<p align="center">
  <img src="static/system_architecture.png" alt="Complete System Architecture" width="800">
  <br>
  <em>End-to-end architecture showing data ingestion, RAG pipeline, training, and inference</em>
</p>

The system implements a complete MLOps lifecycle with four main pipelines:

### 1️⃣ Data Collection & RAG Feature Pipeline

<p align="center">
  <img src="static/rag_feature_pipeline_architecture.png" alt="RAG Feature Pipeline" width="700">
  <br>
  <em>Scalable and modular RAG feature engineering pipeline</em>
</p>

**Key Components:**
- **Data Collection Pipeline**: Ingests raw Notion documents and stores them in S3
- **ETL Pipeline**: Processes and normalizes content using ZenML orchestration
- **Document Quality Filtering**: Multi-stage filtering for high-quality content
- **Contextual Chunking**: Intelligent document segmentation with context preservation
- **Vector Indexing**: Embedding storage with efficient retrieval

### 2️⃣ Agentic Inference Pipeline

<p align="center">
  <img src="static/agentic_rag_architecture.png" alt="Agentic RAG Architecture" width="700">
  <br>
  <em>Agentic RAG module powering intelligent query handling</em>
</p>

**Agentic Layer Features:**
- **Multi-Tool Orchestration**: Coordinates retriever, summarization, and utility tools
- **LiteLLM Integration**: Unified interface for multiple LLM providers
- **Contextual Retrieval**: Fetches top-K relevant chunks with parent document linking
- **Smart Summarization**: Fine-tuned models for domain-specific content
- **Gradio UI**: Interactive interface for seamless user experience
- **Observability**: Real-time prompt monitoring and LLM evaluation

### 3️⃣ Dataset Generation Pipeline

<p align="center">
  <img src="static/dataset_generation_pipeline_architecture.png" alt="Dataset Generation Pipeline" width="700">
  <br>
  <em>Automated summarization instruction dataset generation</em>
</p>

**Process:**
- Document exploration and quality assessment
- Automated summarization with configurable parameters
- Summary quality filtering
- Dataset versioning and registration

### 4️⃣ Training Pipeline

<p align="center">
  <img src="static/training_pipeline_architecture.png" alt="Training Pipeline" width="700">
  <br>
  <em>Modular LLM fine-tuning and deployment pipeline</em>
</p>

**Training Workflow:**
- Model evaluation with experiment tracking (Comet ML)
- LoRA/QLoRA-based efficient fine-tuning (Unsloth)
- Automated hyperparameter optimization
- Model registry integration
- Serverless deployment to Hugging Face

---

## ✨ Features {#features}

### 🔧 Technical Capabilities

- **Production-Ready Architecture**: FTI pattern (Feature/Training/Inference pipelines)
- **Advanced RAG Techniques**: Contextual retrieval, parent document chunking, hybrid search
- **Agentic Workflows**: Tool orchestration using smolagents framework
- **LLM Fine-Tuning**: Domain-specific model optimization with Llama architecture
- **Automated Evaluation**: LLM-as-judge, prompt monitoring, and performance tracking
- **Scalable Data Processing**: Large-scale web crawling and content normalization
- **MLOps Best Practices**: Pipeline orchestration, versioning, experiment tracking

### 🛠️ Engineering Highlights

- Modern Python tooling (`uv`, `ruff`)
- Modular and extensible codebase
- Docker containerization
- CI/CD ready
- Comprehensive logging and monitoring

---

## 🚀 Tech Stack {#tech-stack}

| Category | Technologies |
|----------|-------------|
| **LLMs** | OpenAI GPT-4, Llama 3, Hugging Face Transformers |
| **Orchestration** | ZenML |
| **Monitoring** | Opik, Comet ML |
| **Vector Database** | MongoDB Atlas Vector Search |
| **Fine-Tuning** | Unsloth, QLoRA |
| **Agents** | smolagents |
| **Storage** | AWS S3, MongoDB |
| **Deployment** | Hugging Face Inference Endpoints |
| **UI** | Gradio |
| **Data Source** | Notion API |

---

## 📚 Key Learnings

This project demonstrates:

1. **LLMOps Pipeline Design**: Building production-grade LLM systems with proper separation of concerns
2. **RAG Optimization**: Advanced retrieval strategies beyond basic similarity search
3. **Model Fine-Tuning**: Efficient adaptation of large models for specific domains
4. **Agentic Systems**: Designing AI agents that intelligently orchestrate multiple tools
5. **MLOps Best Practices**: Reproducible pipelines, experiment tracking, model versioning
6. **Quality at Scale**: Automated content scoring and dataset generation

---

## 🎯 Use Cases

- **Personal Knowledge Management**: Query your research and notes conversationally
- **Research Assistance**: Quickly find relevant information across documents
- **Content Summarization**: Automatically digest long documents
- **Learning Aid**: Get explanations based on your curated educational content
- **Idea Discovery**: Uncover connections between different notes and concepts

---

## 🔮 Future Enhancements

- [ ] Multi-modal support (images, PDFs, videos)
- [ ] Integration with additional data sources (Google Drive, Slack, etc.)
- [ ] Real-time learning from user feedback
- [ ] Multi-user support with access controls
- [ ] Mobile application
- [ ] Voice interface integration

---



---

## 🙏 Acknowledgments

- **Tiago Forte** for the Second Brain methodology
- **ZenML** for pipeline orchestration framework
- **Unsloth** for efficient fine-tuning capabilities
-**Decoding ML ** for Project idea and guidance 
- The open-source AI/ML community

---

## Demo
<video  controls>
  <source src="static/second_brain_ai_assistant_example.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
