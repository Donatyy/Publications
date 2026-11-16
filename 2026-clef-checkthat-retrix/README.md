# RETRIX at CheckThat! 2026: Source Retrieval for Scientific Web Claims

[![Venue](https://img.shields.io/badge/CLEF_2026-Working_Notes_(CEUR--WS_4283)-blue)](https://ceur-ws.org/Vol-4283/)
[![Rank](https://img.shields.io/badge/Task_1_Rank-5th_/_37_Teams-gold)](https://checkthat.gitlab.io/clef2026/task1/)
[![MRR@5](https://img.shields.io/badge/Avg_MRR@5-0.7108-brightgreen)](#official-results)

**Authors:** Fabio Baldan, **Davide Donati**, Alvise Garberino, Giancarlo Padoan, Marco Tessari, Nicola Ferro  
**Affiliation:** Department of Information Engineering (DEI), University of Padua, Italy  
**Venue:** *Working Notes of CLEF 2026 – Conference and Labs of the Evaluation Forum*, CEUR Workshop Proceedings, Vol. 4283, pp. 883–896 (October 2026)

---

## Folder Contents

* [`paper.pdf`](./RETRIX%20paper.pdf) — Full working notes paper (Open Access, CC BY 4.0).
* [`CITATION.cff`](./CITATION.cff) — Machine-readable citation metadata.

---

## Overview

**RETRIX** is a multi-stage multilingual Information Retrieval pipeline designed for **Task 1 (*Source Retrieval for Scientific Web Claims*)** of the **CLEF 2026 CheckThat! Lab**. Given a social media post containing a scientific claim in English, German, or French, the system retrieves and ranks the top-5 scholarly papers from a scientific corpus that verify or refute the claim.

### Architecture Pipeline
1. **Cross-Lingual Query Translation:** Non-English claims (German and French) are translated into English to align query representations with predominantly English scientific literature.
2. **Semantic Query Expansion:** Claims are enriched with contextual and domain-specific terms to bridge the vocabulary gap between informal social media phrasing and academic terminology.
3. **Multi-Representation First-Stage Retrieval (`BGE-M3`):** Combines dense semantic embeddings, sparse lexical weights, and multi-vector ColBERT-style late interaction scoring to maximize recall across candidate documents.
4. **Fine-Tuned Cross-Encoder Reranking:** Top candidates are re-scored jointly with the claim using a fine-tuned Cross-Encoder trained with hard negatives to optimize precision at top ranks (`MRR@5`).

---

## Official Results

RETRIX achieved **5th place overall** on the official test leaderboard:

| Metric / Split | English (EN) | German (DE) | French (FR) | **Macro Average** |
| :--- | :---: | :---: | :---: | :---: |
| **MRR@5** | `0.6806` | `0.7117` | **`0.7400`** | **`0.7108`** |
| **Leaderboard Rank** | 5th | 5th | 4th | **5th** |

---

## Citation

If you reference our paper or system architecture, please cite:

```bibtex
@inproceedings{Baldan2026RETRIX,
  author    = {Fabio Baldan and Davide Donati and Alvise Garberino and Giancarlo Padoan and Marco Tessari and Nicola Ferro},
  title     = {{RETRIX at CheckThat! 2026: Source Retrieval for Scientific Web Claims}},
  booktitle = {Working Notes of CLEF 2026 - Conference and Labs of the Evaluation Forum},
  series    = {CEUR Workshop Proceedings},
  volume    = {4283},
  pages     = {883--896},
  publisher = {CEUR-WS.org},
  year      = {2026},
  url       = {[https://ceur-ws.org/Vol-4283/](https://ceur-ws.org/Vol-4283/)}
}
