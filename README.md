<div align="center">
  <h1>EF20K Projects: Investigative Tools</h1>
  
  <p>
    Community driven projects for analyzing 20,000+ Epstein Estate files relased by House Oversight Committee 
  </p>
  
<!-- Badges -->
<p>
  <a href="https://huggingface.co/datasets/tensonaut/EPSTEIN_FILES_20K">
    <img src="https://img.shields.io/badge/Dataset-Hugging%20Face-yellow" alt="datasets" />
  </a>
  <a href="">
    <img src="https://img.shields.io/badge/Documents-20%2C000%2B%20Pages-blue" alt="documents" />
  </a>
  <a href="">
    <img src="https://img.shields.io/badge/Community-Open%20Source-green" alt="community" />
  </a>
</p>
   
<h4>
    <a href="https://huggingface.co/datasets/tensonaut/EPSTEIN_FILES_20K">View Dataset</a>
  <span> · </span>
    <a href="https://github.com/EF20K/Datasets">Documentation</a>
  <span> · </span>
    <a href="https://github.com/EF20K/Safety/issues/">Report Issue</a>
  <span> · </span>
    <a href="https://github.com/EF20K/Projects/issues/">Request Feature</a>
  </h4>
</div>

<br />

# Table of Contents

- [About](#-about)
- [Getting Started](#-getting-started)
- [Projects](#-projects)
- [Contributing](#-contributing)
- [Resources](#-resources)

## About

This repository catalogs community developed projects for analyzing 20,000+ pages of Epstein files released by the House Oversight Committee on November 12, 2025.

> **Content Notice**: Documents contain sensitive material related to criminal investigations.

> **Verification Warning**: Many projects use generative models to analyze documents and can make errors, miss information, or even hallucinate false details. **Always cross verify findings with the actual source documents.** If you encounter erronous information, please [report it in the Safety repository](https://github.com/EF20K/Safety/issues/).

## Getting Started

### Quick Start with Python

New to the dataset? Start with our Jupyter notebook:

**[Getting_Started_w_Dataset.ipynb](Getting_Started_w_Dataset.ipynb)**

## Gathering Insights
This notebook provides basic exploration and analysis examples along with sample queries and filtering techniques

To demonstrate the dataset's utility, I built a reproducible RAG (Retrieval Augmented Generation) baseline. The implementation used simple chunking with a fixed window size and overlapping spans to capture different levels of context. Each chunk was encoded into vectors using Nomic embeddings, a lightweight yet effective embedding model.

The search infrastructure combined Elasticsearch text and vector capabilities, implementing a hybrid retrieval approach that weighted BM25  and cosine similarity scores to produce a unified relevance ranking. For any given query, the system retrieved the top ranked chunks and passed them to the Gemini API for response generation.

This straightforward setup enabled verification of publicly reported information. The system identified several associations that didn't appear in mainstream news coverage. However, the retrieval system also had limitations it missed certain details that were later highlighted in journalistic reports. This baseline serves as a starting point for the community. More sophisticated approaches using better chunking strategies, advanced embedding models, or refined retrieval methods could likely retrival quaility and faithfulness

## Projects

### Search & Analysis

#### [Epstein Document Explorer](https://github.com/maxandrews/Epstein-doc-explorer)
- **Purpose**: Browse and search document collection
- **Key Features**: Advanced search, filtering, bookmarking
- **Privacy**: Browser-based interface

#### [Epstein Files Chat](https://agents.vectorize.io/agents/7d84aa5d-84ab-4991-b268-0b379983f57a/chat)
- **Purpose**: Query documents using natural language
- **Key Features**: AI-powered Q&A, conversational interface
- **Privacy**: Configurable deployment

#### [Epstein Ranker](https://github.com/latent-variable/epstein-ranker)
- **Purpose**: Identify key documents by relevance
- **Key Features**: Algorithm-based ranking, prioritized lists
- **Privacy**: Local processing

#### [Epstein Gate](https://epsteingate.org/)
- **Purpose**: Discover investigative leads
- **Key Features**: AI scoring (0-100), entity extraction, categorization
- **Privacy**: Runs entirely offline

### Visualization

#### [Epstein Files Visualizations](https://svetimfm.github.io/epstein-files-visualizations/)
- **Purpose**: Visual analysis and patterns
- **Key Features**: Interactive charts, relationship mapping
- **Privacy**: Client side processing

## Contributing

Contributions are always welcome!

### Adding Your Project

1. Fork this repository
2. Add your project using this format:

```markdown
#### [Project Name](url)
- **Purpose**: Brief description
- **Key Features**: Main capabilities
- **Privacy**: Privacy approach
```

3. Submit a pull request

### Guidelines

- Legitimate research/journalism purposes
- Clear documentation
- Open-source preferred
- Transparent data handling

## Resources

- [Datasets Repository](https://github.com/EF20K/Datasets) - Dataset documentation and access
- [Safety Repository](https://github.com/EF20K/Safety) - Report issues with projects or data
- [House Oversight Release](https://oversight.house.gov/release/oversight-committee-releases-additional-epstein-estate-documents/) - Original source

---

<div align="center">
<p>Community-maintained • Not affiliated with any official investigation</p>
</div>
