# Rate My Web Design? — Reproducibility Materials

This repository contains the materials supporting the ICSE 2026 Companion poster  
“Rate My Web Design? Using LLMs to Predict Human Subjective Ratings of Generated Web UI Prototypes”.

The goal of this repository is to provide full access to the stimuli and datasets
used in the study, enabling independent re-analysis and replication of the reported results.

---

## Repository Structure
```
├── README.md
├── ratings/
│   ├── Ratings_Human.csv
│   ├── Ratings_Human_Demographics.csv
│   └── Ratings_Models_and_PreLLM_Features.csv
└── stimuli/
    └── screenshots.zip
```
---

## Contents

### 1. Stimuli (stimuli/)

- screenshots.zip  
  Contains the 84 web UI prototypes evaluated in the study.  

Each screenshot corresponds to a unique UI identifier (ui_id) used consistently
across all rating files.

The web UI screenshots included in this repository were created by
Danila Vologdin, Novosibirsk State Technical University, Russia,
as part of the original UI generation process used in the study.

---

### 2. Human Ratings (ratings/Ratings_Human.csv)

Participant-level ratings provided by 39 HCI experts.

Each row corresponds to one participant × one UI, including:
- ui_id
- anonymized participant_id
- ratings on 1–10 Likert scales:
  - A – Aesthetic impression
  - D – Level of detail
  - U – Utility for a designer

These raw ratings were later aggregated at the UI level
(e.g., averages per UI) for the analyses reported in the paper.

---

### 3. Participant Demographics (ratings/Ratings_Human_Demographics.csv)

Anonymized demographic information for the human participants, including:
- country
- age
- gender
- professional background

No personally identifying information is included.

---

### 4. Model Ratings and Pre-LLM Features
(ratings/Ratings_Models_and_PreLLM_Features.csv)

This file contains one row per UI and corresponds to the main analysis table
used in the paper.

It includes:
- LLM ratings (GPT-4o):
  - per-scale: A4, D4, U4
  - overall: O4
- RateMyImage overall rating: ORMI
- Pre-LLM UI features:
  - Filesize (PNG file size)
  - Whitespace
  - NIMA
- Metadata such as domain or generation context (when applicable)

Missing values reflect cases where external services failed,
as described in the paper.

## Reference
Maxim Bakaev and Julián Grigera. 2026. Rate My Web Design?: Using LLMs
to Predict Human Subjective Ratings of Generated Web UI Prototypes. In
2026 IEEE/ACM 48th International Conference on Software Engineering (ICSE-
Companion ’26), April 12–18, 2026, Rio de Janeiro, Brazil. ACM, New York,
NY, USA, 2 pages. https://doi.org/10.1145/3774748.3795676

## License

This repository is released under the same license as the paper
(Creative Commons Attribution 4.0 International, unless stated otherwise).
