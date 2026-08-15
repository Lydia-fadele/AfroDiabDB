# AfroDiabDB v1.2: A Curated Chemoinformatics Database of Antidiabetic Phytochemicals from African Medicinal Flora

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![RDKit](https://img.shields.io/badge/RDKit-2023.03%2B-green.svg)
![License](https://img.shields.io/badge/License-CC--BY--4.0-lightgrey.svg)
![Status](https://img.shields.io/badge/Status-Publication--Ready-brightgreen)

[![Open Chapter 2 In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lydia-fadele/AfroDiabDB/blob/main/notebooks/AfroDiabDB_v1_2_Chapter2_Pipeline.ipynb)
[![Open Chapter 3 In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lydia-fadele/AfroDiabDB/blob/main/notebooks/AfroDiabDB_v1_2_Chapter3_Workflow.ipynb)

---

##  Overview
**AfroDiabDB v1.2** is an open-access, manually curated ethnobotanical and chemoinformatics database cataloging antidiabetic phytochemicals isolated from African medicinal flora[cite: 1, 2].

The **v1.2 release** integrates literature-derived ethnobotanical information with PubChem API verification, RDKit-computed molecular descriptors, drug-likeness filter evaluations (Lipinski, Veber, Ghose), Quantitative Estimate of Drug-likeness (QED) scoring, and chemical space comparison against benchmark FDA-approved antidiabetic drugs[cite: 1, 2].

---

## 📊 Release v1.2 Metrics Summary

* **Total Occurrence Records:** 248 curated entries across 37 standardized metadata fields.
* **Unique Chemical Entities:** 217 validated unique chemical structures (202 canonical SMILES)[cite: 1].
* **Botanical Diversity:** 51 distinct African medicinal plant species spanning 28 families.
* **Drug-Likeness Compliance:** >80% pass rate across standard oral bioavailability filters.
* **Chemical Space Coverage (PCA):** Multi-dimensional PCA capturing chemical space overlap against reference FDA-approved antidiabetic drugs[cite: 2].

---

## 🔄 Computational Workflow & Reproducibility

```text
[ Literature Extraction & Ethnobotanical Sourcing ]
                          │
                          ▼
┌─────────────────────────────────────────────────────────┐
│ Chapter 2: Curation & Descriptor Pipeline               │
│ (notebooks/AfroDiabDB_v1_2_Chapter2_Pipeline.ipynb)     │
├─────────────────────────────────────────────────────────┤
│ • Structure standardization, salt stripping & tautomers │
│ • PubChem CID & Canonical SMILES cross-verification     │
│ • RDKit 2D/3D molecular descriptor generation           │
│ • Multi-filter drug-likeness evaluation                 │
└─────────────────────────┬───────────────────────────────┘
                          │
                          ▼
            [ AfroDiabDB_v1.2_final.xlsx ] (Master Dataset)
                          │
                          ▼
┌─────────────────────────────────────────────────────────┐
│ Chapter 3: Statistical Profiling & PCA Chemical Space   │
│ (notebooks/AfroDiabDB_v1_2_Chapter3_Workflow.ipynb)     │
├─────────────────────────────────────────────────────────┤
│ • Taxonomic distribution & plant family profiling       │
│ • QED scoring & oral bioavailability compliance matrices │
│ • PCA Chemical Space mapping vs. FDA Benchmark Drugs    │
│ • High-resolution publication figures (3.1 – 3.5)      │
└─────────────────────────────────────────────────────────┘
