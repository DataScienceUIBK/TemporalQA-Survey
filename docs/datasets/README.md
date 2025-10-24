# Temporal QA Datasets: Complete Reference

This directory contains comprehensive documentation of all Temporal QA datasets, organized by collection type and characteristics.


## 📁 Directory Structure

- [**Diachronic Corpora**](diachronic.md) - Time-stamped historical documents
- [**Synchronic Corpora**](synchronic.md) - Wikipedia snapshots at specific points in time
- [**Annotated Temporal Corpora**](annotated.md) - Explicitly annotated with TimeML/temporal relations
- [**Web & Real-Time**](web_realtime.md) - Live search and periodically updated datasets
- [**Synthetic & Specialized**](synthetic.md) - Generated datasets for specific reasoning tasks
- [**Knowledge Graph-Based**](knowledge_graphs.md) - Structured temporal KG datasets
- [**Domain-Specific**](domain_specific.md) - Medical, Legal, Financial

---

## 🗂️ Complete Dataset Catalog

### At-a-Glance Comparison Table

| Dataset | Year | #Q | Source Type | Time Coverage | Creation | Multi-Hop | Metadata | Paper | Data |
|---------|------|----|-----------|--------------|---------|-----------|---------:|-------|------|
| **DIACHRONIC (Primary Historical Sources)** |
| ArchivalQA | 2022 | 532K | NYT | 1987-2007 | AG | ✗ | ✓ | [📄](https://dl.acm.org/doi/10.1145/3477495.3531734) | [💾](https://github.com/IBM/ArchivalQA) |
| ChroniclingAmericaQA | 2024 | 485K | Historical News | 1800-1920 | AG | ✗ | ✓ | [📄](https://dl.acm.org/doi/10.1145/3626772.3657887) | [💾](https://github.com/datascienceUIBK/ChroniclingAmericaQA) |
| StreamingQA | 2022 | 147K | News | 2007-2020 | CS | ✓ | ✓ | [📄](https://proceedings.mlr.press/v162/liska22a.html) | [💾](https://github.com/deepmind/streamingqa) |
| NewsQA | 2017 | 119K | CNN/DM | 2007-2015 | CS | ✗ | ✗ | [📄](https://aclanthology.org/W17-2623/) | [💾](https://github.com/Maluuba/newsqa) |
| TempLAMA | 2022 | 50K | News | 2010-2020 | CS | ✗ | ✓ | [📄](https://aclanthology.org/2022.tacl-1.16/) | [💾](https://github.com/google-research/language/tree/master/language/templama) |
| TORQUE | 2020 | 21K | News | - | CS | ✗ | ✗ | [📄](https://aclanthology.org/2020.emnlp-main.88/) | [💾](https://github.com/rujunhan/TORQUE) |
| ForecastQA | 2021 | 10.3K | News | 2015-2019 | CS | ✓ | ✓ | [📄](https://aclanthology.org/2021.acl-long.357/) | [💾](https://github.com/wjn922/ForecastQA) |
| TDDiscourse | 2019 | 6.1K | News | Unspecified | CS | ✗ | ✗ | [📄](https://aclanthology.org/W19-5927/) | [💾](https://github.com/aknaik/TDDiscourse) |
| TemporalQuestions | 2021 | 1K | NYT | 1987-2007 | CS | ✗ | ✓ | [📄](https://link.springer.com/article/10.1007/s10791-020-09382-6) | Contact authors |
| **SYNCHRONIC (Wikipedia Snapshots)** |
| ComplexTempQA | 2024 | 100.2K | Wikipedia | 1987-2023 | AG | ✓ | ✓ | [📄](https://arxiv.org/abs/2406.04866) | [💾](https://github.com/DataScienceUIBK/ComplexTempQA) |
| TEMPREASON | 2023 | 52.8K | Wiki/Wikidata | 634-2023 | SC | ✗ | ✗ | [📄](https://aclanthology.org/2023.acl-long.828/) | [💾](https://github.com/DAMO-NLP-SG/TempReason) |
| TimeQA | 2021 | 41.2K | Wikipedia | 1367-2018 | AG | ✗ | ✗ | [📄](https://openreview.net/forum?id=pzDB_n1r_C) | [💾](https://github.com/wenhuchen/TimeQA) |
| TemporalAlignmentQA | 2024 | 20K | Wikipedia | 2000-2023 | AG | ✗ | ✗ | [📄](https://aclanthology.org/2024.findings-acl.891/) | Contact authors |
| SituatedQA | 2021 | 12.2K | Wikipedia | ≤ 2021 | CS | ✗ | ✗ | [📄](https://aclanthology.org/2021.emnlp-main.586/) | [💾](https://github.com/situatedqa/situatedqa) |
| TempTabQA | 2023 | 11.4K | Wiki Infoboxes | - | CS | ✗ | ✗ | [📄](https://aclanthology.org/2023.emnlp-main.149/) | [💾](https://github.com/vivekgupta9/TempTabQA) |
| TiQ | 2024 | 10K | Wikipedia | Unspecified | AG | ✗ | ✗ | [📄](https://dl.acm.org/doi/10.1145/3589335.3651529) | Contact authors |
| PAT-Questions | 2024 | 6.1K | Wikipedia | Present | CS | ✓ | ✗ | [📄](https://aclanthology.org/2024.findings-acl.782/) | [💾](https://github.com/vhiribarren/pat-questions) |
| TRACIE | 2021 | 5.4K | Wikipedia | ≤ 2020 | CS | ✗ | ✗ | [📄](https://aclanthology.org/2021.naacl-main.107/) | [💾](https://github.com/CogComp/TRACIE) |
| MenatQA | 2023 | 2.8K | Wikipedia | 1367-2018 | AG | ✗ | ✗ | [📄](https://aclanthology.org/2023.findings-emnlp.99/) | [💾](https://github.com/yfyuan01/MenatQA) |
| **WEB & REAL-TIME** |
| ReaLTimeQA | 2023 | 5.1K | Web Search | 2020-2024 | CS | ✗ | ✗ | [📄](https://proceedings.neurips.cc/paper_files/paper/2023/hash/9a6e9a1519ee1f031b35acb238e97bc2-Abstract-Datasets_and_Benchmarks.html) | [💾](https://github.com/realtimeqa/realtimeqa) |
| FreshQA | 2024 | 600 | Google Search | Dynamic | CS | ✓ | ✗ | [📄](https://aclanthology.org/2024.findings-acl.820/) | [💾](https://github.com/freshllms/freshqa) |
| **SYNTHETIC & SPECIALIZED** |
| COTEMPQA | 2024 | 4.7K | Wikidata | ≤ 2023 | CS | ✓ | ✗ | [📄](https://aclanthology.org/2024.acl-long.703/) | [💾](https://github.com/zhaochen0110/cotempqa) |
| UnSeenTimeQA | 2024 | 3.6K | Synthetic | - | AG | ✓ | ✗ | [📄](https://arxiv.org/abs/2407.03525) | [💾](https://github.com/mdnayeemsarker/UnSeenTimeQA) |
| Test of Time | 2024 | 1.8K | Synthetic | - | AG | ✓ | ✗ | [📄](https://arxiv.org/abs/2406.09170) | [💾](https://github.com/google-deepmind/test_of_time) |
| TIMEDIAL | 2021 | 1.1K | DailyDialog | - | CS | ✗ | ✗ | [📄](https://aclanthology.org/2021.acl-long.549/) | [💾](https://github.com/google-research-datasets/TimeDial) |

**Legend**: 
- **#Q**: Number of questions
- **Creation**: AG = Auto-Generated, CS = Crowdsourced, SC = Synthetic
- **Multi-Hop**: Requires reasoning across multiple temporal hops
- **Metadata**: Explicit temporal metadata available

---

## 📈 Dataset Characteristics


### By Temporal Complexity

| Complexity | Datasets | Key Features |
|------------|----------|--------------|
| **Simple** | NewsQA, TimeQA, TempLAMA, ArchivalQA | Direct temporal lookups, explicit dates |
| **Complex** | ComplexTempQA, TEMPREASON, MenatQA, StreamingQA | Multi-hop reasoning, temporal filtering |
| **Reasoning-Focused** | Test of Time, UnSeenTimeQA, COTEMPQA | Synthetic temporal logic, beyond memorization |

### By Temporal Orientation

| Orientation | Datasets | Description |
|-------------|----------|-------------|
| **Historical** | ChroniclingAmericaQA (1800-1920), TimeQA (1367-2018) | Past events |
| **Recent Past** | NewsQA, ArchivalQA, StreamingQA | Modern history (1987-2020) |
| **Present/Future** | FreshQA, ReaLTimeQA, ForecastQA | Current/predictive |

### By Answer Type

| Type | Count | Examples |
|------|-------|----------|
| **Extractive** | 15 | ArchivalQA, TimeQA, NewsQA |
| **Abstractive** | 7 | TEMPREASON, TemporalAlignmentQA, TRACIE |
| **Multiple Choice** | 3 | ForecastQA, ReaLTimeQA, TIMEDIAL |
| **Entities/Freeform** | 2 | TiQ, NewsQA |

---


## 🔧 Common Dataset Issues & Solutions

### Issue 1: Temporal Ambiguity
**Problem**: Questions like "Who is the president?" lack temporal context  
**Datasets addressing this**: SituatedQA, PAT-Questions  
**Solution**: Explicit temporal anchoring or temporal disambiguation

### Issue 2: Answer Drift
**Problem**: Correct answers change over time  
**Datasets addressing this**: FreshQA, ReaLTimeQA  
**Solution**: Periodic dataset updates, versioning

### Issue 3: Annotation Quality
**Problem**: Crowdsourced datasets may have inconsistent temporal understanding  
**Mitigation**: Multiple annotators, expert validation (e.g., ArchivalQA with journalistic expertise)

### Issue 4: Limited Temporal Reasoning Types
**Problem**: Many datasets focus on simple lookup  
**Datasets addressing this**: ComplexTempQA, TEMPREASON, Complex-TR  
**Solution**: Synthetic generation with explicit reasoning templates

---

## 📊 Dataset Comparison Framework

When comparing datasets, consider these dimensions:

1. **Temporal Scope**: Historical range covered
2. **Temporal Granularity**: Day, month, year, era
3. **Question Complexity**: Simple lookup vs. multi-hop reasoning
4. **Temporal Explicitness**: Explicit dates vs. implicit temporal references
5. **Answer Volatility**: How quickly answers become outdated
6. **Evaluation Protocol**: Static test set vs. periodic updates
7. **Annotation Quality**: Crowdsourced vs. automatic vs. expert
8. **Metadata Richness**: Availability of document timestamps, temporal expressions

---

## 🔄 Dataset Updates

| Dataset | Last Updated | Update Frequency | Notes |
|---------|-------------|------------------|-------|
| ReaLTimeQA | 2024-06 | Weekly | Continuous updates |
| FreshQA | 2024-03 | Periodic | Manual updates |
| PAT-Questions | 2024 | Self-updating mechanism | Automated |
| Others | Static | One-time release | - |

---

## 📝 Contributing

Found a dataset we missed? Please [open an issue](../../issues):
- Dataset name and paper
- Statistics (#questions, time coverage)
- Links to paper and data
- Key characteristics

---

[← Back to Main README](../../README.md)
