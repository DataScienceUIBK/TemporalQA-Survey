# Temporal QA Methods: Complete Reference

This directory contains comprehensive documentation of all approaches to Temporal Question Answering, organized by methodology and era.

## 📊 Methods Statistics

- **Total Methods Documented**: 50+
- **Temporal Coverage**: 2003-2025
- **Categories**: Rule-Based, Statistical, Neural, LLMs, RAG, Reasoning
- **Paradigm Shifts**: 4 major eras identified

---

## 📁 Directory Structure

- [**Temporal Language Models**](temporal_lms.md) - Pre-trained models with temporal awareness
- [**Temporal RAG Systems**](temporal_rag.md) - Retrieval-augmented generation for TQA
- [**Temporal Reasoning**](temporal_reasoning.md) - Explicit reasoning mechanisms
- [**Classical Methods**](classical.md) - Rule-based and statistical approaches (2003-2019)
- [**Benchmarking & Evaluation**](evaluation.md) - Testing temporal capabilities

---

## 🕰️ Evolution Timeline
```
📅 ERA 1: Rule-Based Systems (2003-2010)
   └─ TimeML, temporal taggers, hand-crafted rules

📅 ERA 2: Statistical & Early Neural (2011-2019)
   └─ Language models, temporal embeddings, ranking

📅 ERA 3: Transformer Revolution (2020-2022)
   └─ Temporal pretraining, time-aware architectures

📅 ERA 4: LLM & RAG Era (2023-2025)
   └─ Retrieval augmentation, temporal reasoning
```

## 📊 Comprehensive Methods Comparison

### Table 1: Method Architecture & Design Overview

| Method | Year | Type | Task | Temporal Representation | Temporal Signals | Architecture | Paper | Code |
|--------|------|------|------|------------------------|------------------|--------------|-------|------|
| **TempoT5** | 2022 | Encoder-Decoder | TQA | Explicit timestamps | Document timestamps + temporal context | T5 + temporal conditioning | [📄](https://aclanthology.org/2022.tacl-1.16/) | [💾](https://github.com/google-research/language/tree/master/language/templama) |
| **TempoBERT** | 2022 | Encoder | Semantic Change Detection, Sentence Time Prediction | Explicit timestamps | Time tokens | BERT + temporal masking | [📄](https://dl.acm.org/doi/10.1145/3488560.3498529) | [💾](https://github.com/GuyRosin/TempoBERT) |
| **BiTimeBERT** | 2023 | Encoder | Event Time Estimation, Document Dating, TQA | Explicit timestamps and content temporal expressions | Document timestamps + temporal expressions in text | BERT + dual temporal encoding | [📄](https://dl.acm.org/doi/10.1145/3539618.3591675) | Contact authors |
| **TALM** | 2023 | Temporal adaptation + Hierarchical modeling | Historical Dating | Implicit (Time-specific word variants) | Time-specific representations | BERT + Temporal Adaptation + Hierarchical Document Encoder | [📄](https://aclanthology.org/2023.findings-emnlp.908/) | Contact authors |
| **SG-TLM** | 2023 | TLM | Temporal Language Modeling, TQA | Implicit Temporal Information | Syntactic role distributions + timestamps | BERT + syntax-guided masking + temporal-aware masking | [📄](https://aclanthology.org/2023.findings-emnlp.425/) | [💾](https://github.com/szhaochen/SG-TLM) |
| **TSM** | 2023 | Encoder | Temporal language modelling, TQA | Implicit temporal spans | Temporal expressions (dates, durations) | T5 + temporal span masking | [📄](https://aclanthology.org/2023.eacl-main.221/) | Contact authors |
| **Temporal Attention** | 2022 | Encoder | Semantic Change Detection | Explicit Document timestamp | Document timestamp | Transformer encoder with time-aware attention via time matrix T | [📄](https://aclanthology.org/2022.findings-naacl.114/) | [💾](https://github.com/GuyRosin/temporal-attention) |
| **TempRetriever** | 2025 | Neural Embedding | TQA | Explicit + Implicit temporal information | Query timestamps + document timestamps | Semantic + Temporal Encoder | [📄](https://arxiv.org/abs/2502.21024) | Coming soon |
| **TsContriever** | 2024 | Neural Retrieval | TQA | Explicit + Implicit temporal information | Query timestamps + document timestamps | Semantic + Temporal Encoder | [📄](https://dl.acm.org/doi/10.1145/3627673.3679786) | Contact authors |
| **TempRALM** | 2024 | RAG | TQA | Explicit temporal Information | Query + document timestamps | RAG + temporal enhancement | [📄](https://arxiv.org/abs/2410.14333) | Contact authors |
| **TimeR4** | 2024 | RAG | TQA | Explicit temporal facts | Question constraints + TKG timestamps | Retrieve-Rewrite-Retrieve-Rerank with contrastive time-aware retriever + LLaMA2 reasoning | [📄](https://aclanthology.org/2024.emnlp-main.408/) | [💾](https://github.com/czy1999/TimeR4) |
| **MRAG** | 2024 | Neural + Symbolic | TQA | Explicit temporal information | Query constraints + Document timestamps | Modular RAG framework (Question Processing, Retrieval + Summarization + Semantic-Temporal Hybrid Ranking) | [📄](https://arxiv.org/abs/2412.15540) | Coming soon |

---

### Table 2: Method Implementation Details

| Method | Input | Output | Knowledge | Processing | Methodology | Paper | Code |
|--------|-------|--------|-----------|------------|-------------|-------|------|
| **TempoT5** | Text + temporal prefix | Masked span prediction | CUSTOMNEWS + TEMPLAMA | Temporal conditioning + uniform sampling | Input prefixing for time-aware modeling and efficient updates | [📄](https://aclanthology.org/2022.tacl-1.16/) | [💾](https://github.com/google-research/language/tree/master/language/templama) |
| **TempoBERT** | Text + timestamps | Time tokens | News corpus | Implicit temporal reasoning via time masking | Time-aware pretraining with masking | [📄](https://dl.acm.org/doi/10.1145/3488560.3498529) | [💾](https://github.com/GuyRosin/TempoBERT) |
| **BiTimeBERT** | News articles with timestamps | Time predictions (day/month/year granularity) | NYT corpus | Bi-temporal reasoning using both timestamp and content time | Time-Aware Masked Language Modeling, Document Dating | [📄](https://dl.acm.org/doi/10.1145/3539618.3591675) | Contact authors |
| **TALM** | Historical text | Time period classification | Chinese Twenty-Four Histories + English Royal Society Corpus | Temporal word adaptation and contextual learning | Learn separate word representations per time period + alignment | [📄](https://aclanthology.org/2023.findings-emnlp.908/) | Contact authors |
| **SG-TLM** | Text + timestamp | Masked token + time prediction | WMT News Crawl + Reddit Time Corpus | Syntax-guided masking (SGM) + temporal-aware masking (TAM) | Syntax-based lexicon selection for efficient temporal adaptation | [📄](https://aclanthology.org/2023.findings-emnlp.425/) | [💾](https://github.com/szhaochen/SG-TLM) |
| **TSM** | Text with temporal expressions | Masked span prediction | Wikipedia | Temporal span masking using SUTIME parser + intermediate training | SUTIME parser identifies temporal expressions (Time, Duration, Set, Date) for targeted masking during intermediate pretraining | [📄](https://aclanthology.org/2023.eacl-main.221/) | Contact authors |
| **Temporal Attention** | Text + Document timestamp | Time-specific contextualized embeddings | Time-annotated corpora (SemEval datasets) | Time-aware self-attention mechanism with additional time matrix | Extends self-attention with time matrix T to condition attention weights on temporal context via time-aware dot products | [📄](https://aclanthology.org/2022.findings-naacl.114/) | [💾](https://github.com/GuyRosin/temporal-attention) |
| **TempRetriever** | Query + Query timestamp + Document + Document timestamp | Passages with temporal + semantic relevance | NYT + ChroniclingAmerica Corpus | Temporal alignment + Temporal understanding | Learned temporal embeddings with fusion techniques + Time-based negative sampling | [📄](https://arxiv.org/abs/2502.21024) | Coming soon |
| **TsContriever** | Time-sensitive questions | Top-k temporally relevant documents | Nobel Prize benchmark corpus + Wikidata QA pairs | Contrastive learning + Query-side fine-tuning + Query routing | Supervised contrastive learning with time-aware query tuning and routing | [📄](https://dl.acm.org/doi/10.1145/3627673.3679786) | Contact authors |
| **TempRALM** | Time-sensitive queries | Answer | Knowledge base | Temporal proximity-based document ranking | Temporal scoring | [📄](https://arxiv.org/abs/2410.14333) | Contact authors |
| **TimeR4** | Time-sensitive queries | Answer (entity or timestamp) | Knowledge base | Retrieve-Rewrite-Retrieve-Rerank pipeline with contrastive learning and LLM finetuning | Temporal fact retrieval, question rewriting, time-aware reranking, and LLM finetuning | [📄](https://aclanthology.org/2024.emnlp-main.408/) | [💾](https://github.com/czy1999/TimeR4) |
| **MRAG** | Temporal questions + Document | Ranked passages | Wikipedia | Symbolic temporal scoring + Semantic-temporal hybrid ranking | Question decomposition (MC + TC) + Symbolic temporal | [📄](https://arxiv.org/abs/2412.15540) | Coming soon |

**Table Notes:**
- **Type**: Architectural paradigm (Encoder, Encoder-Decoder, RAG, etc.)
- **Temporal Representation**: Whether temporal information is explicit or implicit
- **Temporal Signals**: What temporal cues the model uses
- **Processing**: Core mechanisms for handling temporal information
- **Methodology**: Training strategy or modeling paradigm

---

## 📈 Method Statistics

### By Method Type

| Type | Count | Methods |
|------|-------|---------|
| **Encoder-only** | 5 | TempoBERT, BiTimeBERT, TALM, TSM, Temporal Attention |
| **Encoder-Decoder** | 1 | TempoT5 |
| **Neural Retrieval** | 2 | TempRetriever, TsContriever |
| **RAG Systems** | 3 | TempRALM, TimeR4, MRAG |

### By Temporal Representation

| Representation Type | Count | Methods |
|-------------------|-------|---------|
| **Explicit Timestamps** | 6 | TempoT5, TempoBERT, BiTimeBERT, Temporal Attention, TempRALM, TimeR4 |
| **Implicit Temporal** | 3 | TALM, SG-TLM, TSM |
| **Explicit + Implicit** | 3 | TempRetriever, TsContriever, MRAG |

### By Primary Task

| Task | Count | Methods |
|------|-------|---------|
| **TQA** | 9 | TempoT5, BiTimeBERT, SG-TLM, TSM, TempRetriever, TsContriever, TempRALM, TimeR4, MRAG |
| **Semantic Change Detection** | 2 | TempoBERT, Temporal Attention |
| **Document/Event Dating** | 2 | BiTimeBERT, TALM |
| **Temporal Language Modeling** | 2 | SG-TLM, TSM |

### By Year

| Year | Count | Methods |
|------|-------|---------|
| **2022** | 3 | TempoT5, TempoBERT, Temporal Attention |
| **2023** | 3 | BiTimeBERT, TALM, SG-TLM, TSM |
| **2024** | 4 | TsContriever, TempRALM, TimeR4, MRAG |
| **2025** | 1 | TempRetriever |

---

## 🏗️ Architectural Categories

### Temporal Language Models (Pretraining-based)

| Method | Architecture Base | Temporal Innovation | Training Corpus |
|--------|------------------|---------------------|-----------------|
| **TempoT5** | T5 | Temporal prefix conditioning | CUSTOMNEWS + TEMPLAMA |
| **TempoBERT** | BERT | Time token masking | News corpus |
| **BiTimeBERT** | BERT | Dual temporal encoding (timestamp + content) | NYT corpus |
| **TALM** | BERT | Hierarchical temporal word representations | Historical texts |
| **SG-TLM** | BERT | Syntax-guided + temporal masking | WMT News + Reddit |
| **TSM** | T5 | Temporal span masking | Wikipedia |
| **Temporal Attention** | Transformer | Time matrix in attention | SemEval datasets |

### Temporal RAG Systems (Retrieval-based)

| Method | Pipeline Stages | Retrieval Strategy | Generation Model |
|--------|----------------|-------------------|------------------|
| **TempRetriever** | Single-stage retrieval | Fusion-based temporal embeddings | - |
| **TsContriever** | Single-stage retrieval | Contrastive learning | - |
| **TempRALM** | Retrieve → Generate | Temporal proximity ranking | LLM |
| **TimeR4** | Retrieve → Rewrite → Retrieve → Rerank | Multi-stage with query rewriting | LLaMA2 |
| **MRAG** | Question Processing → Retrieval → Summarization → Ranking | Modular with symbolic temporal scoring | LLM |

## 🏗️ Architecture Patterns

### Pattern 1: Temporal Input Encoding

**Approaches**: TempoT5, BiTimeBERT, TsContriever
```
Text Input + Timestamp → Enhanced Embedding → Model
```

**Advantages**: 
- Simple to implement
- Works with existing architectures
- Explicit temporal signal

**Limitations**:
- Requires timestamp metadata
- May not capture implicit temporal cues

### Pattern 2: Temporal Pretraining Objectives

**Approaches**: TempoBERT, TSM, SG-TLM
```
Standard LM → Temporal Masking → Time-Aware Representations
```

**Advantages**:
- Learns temporal patterns from data
- No inference-time timestamps needed
- Generalizes to implicit temporal language

**Limitations**:
- Computationally expensive
- Requires large temporal corpora

### Pattern 3: Retrieval-Then-Generate

**Approaches**: TimeR4, MRAG, TempRALM
```
Query → Temporal Retrieval → Context + Temporal Signals → Generation
```

**Advantages**:
- Handles knowledge updates
- Explainable (retrieval visible)
- Modular (swap retrievers)

**Limitations**:
- Retrieval quality critical
- Latency from multiple steps

### Pattern 4: Explicit Temporal Reasoning

**Approaches**: TIMERS, ConTempo, ECONET
```
Text → Event/Relation Extraction → Temporal Graph → Reasoning
```

**Advantages**:
- Structured reasoning
- Multi-hop capabilities
- Interpretable

**Limitations**:
- Complex pipelines
- Error propagation

---


## 📝 Contributing

We welcome contributions to keep this survey comprehensive and up-to-date!

### Missing a Paper or Dataset?

If we've missed your work or you know of a relevant paper/dataset that should be included, please send us an email at:

📧 **[bhawna.piryani@uibk.ac.at](mailto:bhawna.piryani@uibk.ac.at)**

Please include:
- Paper title and authors
- Link to paper and code/data (if available)
- Brief description of the contribution

You can also [open an issue](../../issues) on GitHub.
---

[← Back to Main README](../../README.md)
