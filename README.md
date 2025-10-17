<h1 align="center">
  <img src="images/hourglass.png" alt="Logo" width="55" style="vertical-align: middle; margin-right: 10px; position: relative; top: 8px;">
  It's High Time: A Survey of Temporal Question Answering
</h1>


<p align="center">
  <strong>Bhawna Piryani</strong> · Abdelrahman Abdallah · Jamshid Mozafari · Avishek Anand · Adam Jatowt  
  <br>
  <em>University of Innsbruck · TU Delft</em>
  <br><br>
  📄 <a href="https://arxiv.org/abs/2505.20243v3">Read the Paper on arXiv</a> &nbsp;|&nbsp; 🗓️ <strong>2025</strong>
</p>

---

### 📘 Overview

This repository accompanies our paper  on *Temporal Question Answering (TQA)* — exploring how AI models reason about time, adapt to evolving knowledge, and answer temporally constrained questions.

<p align="center">
  <img src="images/TemporalSurveyFigure.png" alt="Temporal QA Taxonomy" width="700">
</p>

---

## ❤️ Recap

We present a comprehensive **survey of Temporal Question Answering (TQA)** — a field that studies how AI systems reason about *when* events happen, adapt to evolving knowledge, and answer **time-sensitive or time-dependent questions**.

We organize the literature along three major research pillars:

- **Temporal Representation and Understanding** — detecting and normalizing time expressions, estimating event and document focus time.  
- **Temporal Modeling and Reasoning** — temporal language models (TLMs) and retrieval-augmented generation (RAG) approaches for reasoning over time.  
- **Temporal Evaluation and Robustness** — datasets, benchmarks, and metrics assessing temporal consistency, recency awareness, and reasoning reliability.

<p align="center">
  <img src="images/TemporalSurveyFigure.png" alt="Temporal QA Taxonomy" width="700"><br>
  <em>Taxonomy of Temporal QA: datasets, benchmarks, and approaches</em>
</p>

---

## 🚀 Table of Contents

- [Overview](#overview)
- [1️⃣ Temporal Foundations](#1️⃣-temporal-foundations)
  - [1.1 Temporal Information Retrieval (TIR)](#11-temporal-information-retrieval-tir)
  - [1.2 Temporal Question Answering (TQA)](#12-temporal-question-answering-tqa)
- [2️⃣ Datasets and Benchmarks](#2️⃣-datasets-and-benchmarks)
  - [2.1 Diachronic & Synchronic Corpora](#21-diachronic--synchronic-corpora)
  - [2.2 Temporal QA Datasets](#22-temporal-qa-datasets)
- [3️⃣ Methods and Models](#3️⃣-methods-and-models)
  - [3.1 Temporal Language Models](#31-temporal-language-models)
  - [3.2 Temporal Retrieval-Augmented Generation (RAG)](#32-temporal-retrieval-augmented-generation-rag)
  - [3.3 Temporal Reasoning Capabilities](#33-temporal-reasoning-capabilities)
- [4️⃣ Future Directions](#4️⃣-future-directions)
- [📚 Citation](#-citation)
- [🪪 License](#-license)

---

## Overview

Temporal QA focuses on systems that can **understand, retrieve, and reason over time-dependent information**.  
This includes interpreting vague expressions like “recently” or “after the war,” resolving temporal ambiguity, and aligning retrieved evidence with a question’s time frame.

---

## 1️⃣ Temporal Foundations

### 1.1 Temporal Information Retrieval (TIR)
Time-aware retrieval aims to identify documents that are not only topically relevant but also **temporally aligned** with the query’s intent — e.g., “latest Apple earnings” or “climate policy in 2015.”

### 1.2 Temporal Question Answering (TQA)
Goes beyond retrieval by requiring reasoning over **temporal constraints**, such as ordering events or computing intervals (e.g., “At what age did Obama win the Nobel Peace Prize?” → 48 years).

---

## 2️⃣ Datasets and Benchmarks

### 2.1 Diachronic & Synchronic Corpora
- **Diachronic**: Long-term archives (e.g., *NYT*, *Chronicling America*) capturing event evolution.  
- **Synchronic**: Snapshot datasets (e.g., *Wikipedia dumps*) reflecting world knowledge at a fixed time.

### 2.2 Temporal QA Datasets
Key datasets include **TimeQA**, **ArchivalQA**, **TempLAMA**, and **ComplexTempQA**, covering both explicit and implicit temporal reasoning.

---

## 3️⃣ Methods and Models

### 3.1 Temporal Language Models
Models such as **TempoT5**, **TempoBERT**, and **BiTimeBERT** incorporate timestamps or temporal cues directly into their architecture for better time-aware representations.

### 3.2 Temporal Retrieval-Augmented Generation (RAG)
Approaches like **TempRetriever** and **TempRALM** integrate neural retrieval with generative reasoning to dynamically incorporate up-to-date evidence.

### 3.3 Temporal Reasoning Capabilities
Beyond modeling, recent works explore **event ordering**, **duration estimation**, and **temporal robustness** — testing whether LLMs can reason consistently over time.

---

## 4️⃣ Future Directions

We highlight open challenges for building truly time-aware systems:
- Dynamic temporal knowledge management  
- Diachronic–synchronic integration  
- Temporal uncertainty and confidence modeling  
- Multilingual and multimodal temporal reasoning  
- Implicit temporal intent detection  

---



## Table of Contents
1. [Surveys & Tutorials](#surveys--tutorials)
2. [Temporal IR – Query & Ranking](#temporal-ir--query--ranking)
3. [Document Dating & Event‑Time Estimation](#document-dating--event‑time-estimation)
4. [Datasets & Benchmarks for Temporal QA](#datasets--benchmarks-for-temporal-qa)
5. [Temporal QA – Models & Methods](#temporal-qa--models--methods)
6. [Temporal Language Models & Representation Learning](#temporal-language-models--representation-learning)

---

## Surveys & Tutorials
| Year | Title & Link | Citation key |
|------|--------------|--------------|
| 2025 | **From Matching to Generation: A Survey on Generative Information Retrieval** – Li *et al.* [[ACM]](https://doi.org/10.1145/3722552) | `li2024matching` |
| 2023 | **Large Language Models for Information Retrieval: A Survey** – Zhu *et al.* [[arXiv]](https://arxiv.org/abs/2308.07107) | `zhu2023large` |
| 2021 | **Retrieving and Reading: A Comprehensive Survey on Open‑Domain Question Answering** – Zhu *et al.* [[arXiv]](https://arxiv.org/abs/2101.00774) | `zhu2021retrieving` |
| 2016 | **Temporal Information Retrieval** (SIGIR tutorial) – Kanhabua & Anand [[ACM]](https://doi.org/10.1145/2911451.2914805) | `kanhabua2016temporal` |
| 2014 | **Survey of Temporal Information Retrieval and Related Applications** – Campos *et al.* [[ACM]](https://doi.org/10.1145/2619088) | `campos2014survey` |

---

## Temporal IR – Query & Ranking
| Year | Title & Link | Citation key |
|------|--------------|--------------|
| 2009 | **Time Will Tell: Leveraging Temporal Expressions in IR** – Arikan *et al.* |
| 2009 | **Improving Search Relevance for Implicitly Temporal Queries** – Metzler *et al.* |
| 2010 | **A Language‑Model Approach for Temporal Information Needs** – Berberich *et al.* |
| 2010 | **Determining Time of Queries for Re‑Ranking Search Results** – Kanhabua & Norvåg |
| 2007 | **Temporal Profiles of Queries** – Jones & Diaz |
| 2008 | **Answering General Time‑Sensitive Queries** – Dakka *et al.* |
| 2014 | **Identifying Time Intervals of Interest to Queries** – Gupta & Berberich |
| 2003 | **Time‑Based Language Models** – Li & Croft |

---

## Document Dating & Event‑Time Estimation
| Year | Title & Link | Citation key |
|------|--------------|--------------|
| 2021 | **Event Occurrence Date Estimation via Multivariate Time‑Series** – Wang *et al.* |
| 2018 | **Leveraging Linked Entities to Estimate Focus Time of Short Texts** – Morbidoni *et al.* |
| 2017 | **Estimating Event Focus Time Using Neural Word Embeddings** – Das *et al.* |
| 2017 | **Concept‑Driven Graph‑Based Focus‑Time Estimation** – Shrivastava *et al.* |
| 2018 | **Dating Documents with Graph Convolution Networks** – Vashishth *et al.* |
| 2013 | **Estimating Document Focus Time** – Jatowt *et al.* |
| 2012 | **Dating Texts without Explicit Temporal Cues** – Kumar *et al.* |
| 2008 | **Improving Temporal LMs for Dating Non‑Timestamped Docs** – Kanhabua & Norvåg |
| 2005 | **Temporal Language Models for Disclosure of Historical Text** – Jong *et al.* |

---

## Datasets & Benchmarks for Temporal QA
| Year | Dataset | Paper / Link |
|------|---------|--------------|
| 2024 | **TimeBench** – Chu *et al.* [[ACL]](https://aclanthology.org/2024.acl-long.66/) |
| 2024 | **TIQ** (Temporal QA with Implicit Constraints) – Jia *et al.* [[ACM]](https://doi.org/10.1145/3589335.3651895) |
| 2024 | **ChroniclingAmericaQA** – Piryani *et al.* [[ACM]](https://doi.org/10.1145/3626772.3657891) |
| 2023 | **MenatQA** – Wei *et al.* [[ACL]](https://aclanthology.org/2023.findings-emnlp.100/) |
| 2022 | **ArchivalQA** – Wang *et al.* [[ACM]](https://doi.org/10.1145/3477495.3531734) |
| 2021 | **A Dataset for Answering Time‑Sensitive Questions** – Chen *et al.* (NeurIPS Datasets) |
| 2020 | **TORQUE** – Ning *et al.* [[ACL]](https://aclanthology.org/2020.emnlp-main.88/) |
| 2018 | **TempQuestions** – Jia *et al.* [[ACM]](https://doi.org/10.1145/3184558.3191536) |

---

## Temporal QA – Models & Methods
| Year | Title & Link | Citation key |
|------|--------------|--------------|
| 2024 | **Continual Learning for Temporal‑Sensitive QA** – Yang *et al.* (IJCNN) |
| 2024 | **Enhancing Temporal Sensitivity & Reasoning for Time‑Sensitive QA** – Yang *et al.* [[ACL]](https://aclanthology.org/2024.findings-emnlp.848/) |
| 2023 | **Benchmarking & Improving Temporal Reasoning of LLMs** – Tan *et al.* [[ACL]](https://aclanthology.org/2023.acl-long.828/) |
| 2021 | **Improving QA for Event‑Focused Questions in News Collections** – Wang *et al.* (IR Journal) |
| 2020 | **Machine Reading of Historical Events** – Honovich *et al.* [[ACL]](https://aclanthology.org/2020.acl-main.668/) |
| 2009 | **Enhancing QA with Complex Temporal Question Processing** – Saquete *et al.* |
| 2005 | **QA Based on Temporal Inference** – Harabagiu & Bejan |
| 2004 | **Splitting Complex Temporal Questions for QA Systems** – Saquete *et al.* |

---

## Temporal Language Models & Representation Learning
| Year | Title & Link | Citation key |
|------|--------------|--------------|
| 2024 | **Time‑Sensitive Knowledge Editing via Efficient Finetuning** – Ge *et al.* [[ACL]](https://aclanthology.org/2024.acl-short.53/) |
| 2023 | **Efficient Continue‑Training of Temporal LMs with Structural Info** – Su *et al.* [[ACL]](https://aclanthology.org/2023.findings-emnlp.418/) |
| 2023 | **Salient Span Masking for Temporal Understanding** – Cole *et al.* [[ACL]](https://aclanthology.org/2023.eacl-main.222/) |
| 2023 | **BiTimeBERT: Extending PLMs with Bi‑Temporal Information** – Wang *et al.* [[ACM]](https://doi.org/10.1145/3539618.3591686) |
| 2022 | **Time‑Aware LMs as Temporal KBs** – Dhingra *et al.* [[TACL]](https://aclanthology.org/2022.tacl-1.15/) |
| 2022 | **Time Masking for Temporal LMs** – Rosin *et al.* [[ACM]](https://doi.org/10.1145/3488560.3498529) |
| 2022 | **Temporal Attention for Language Models** – Rosin & Radinsky [[ACL]](https://aclanthology.org/2022.findings-naacl.112/) |
| 2022 | **Temporal Effects on Pre‑trained Models** – Agarwal & Nenkova [[TACL]](https://aclanthology.org/2022.tacl-1.53/) |
| 2021 | **Dynamic Contextualised Word Embeddings** – Hofmann *et al.* [[ACL]](https://aclanthology.org/2021.acl-long.542/) |
| 2021 | **Mind the Gap: Assessing Temporal Generalisation in NLMs** – Lazaridou *et al.* (NeurIPS) |
| 2019 | **Neural Temporality Adaptation for Document Classification** – Huang & Paul [[ACL]](https://aclanthology.org/P19-1403/) |

---

## 🪪License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ✨Citation
If you find this work useful, please cite [📜our paper](https://arxiv.org/pdf/2505.20243):
### Plain
Piryani, B., Abdullah, A., Mozafari, J., Anand, A., & Jatowt, A. (2025). It's High Time: A Survey of Temporal Question Answering. arXiv preprint arXiv:2505.20243.
### Bibtex
```bibtex
@article{piryani2025s,
  title={It's High Time: A Survey of Temporal Question Answering},
  author={Piryani, Bhawna and Abdullah, Abdelrahman and Mozafari, Jamshid and Anand, Avishek and Jatowt, Adam},
  journal={arXiv preprint arXiv:2505.20243},
  year={2025}
}

```
