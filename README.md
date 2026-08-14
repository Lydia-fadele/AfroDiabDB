# AfroDiabDB v1.2: A Curated Chemoinformatics Database of Antidiabetic Phytochemicals from African Medicinal Flora

![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)
![RDKit](https://img.shields.io/badge/RDKit-2023.03%2B-green.svg)
![License](https://img.shields.io/badge/License-CC--BY--4.0-lightgrey.svg)
![Status](https://img.shields.io/badge/Status-Publication--Ready-brightgreen)

##  Overview
**AfroDiabDB v1.2** is an open-access, manually curated ethnobotanical and chemoinformatics database cataloging antidiabetic phytochemicals isolated from African medicinal flora. 

The **v1.2 release** integrates literature-derived ethnobotanical information with PubChem API verification, RDKit-computed molecular descriptors, drug-likeness filter evaluations (Lipinski, Veber, Ghose), Quantitative Estimate of Drug-likeness (QED) scoring, and chemical space comparison against benchmark FDA-approved antidiabetic drugs.

---

##  Release v1.2 Metrics Summary

* **Total Occurrence Records:** 248 curated entries across 37 standardized metadata fields.
* **Unique Chemical Entities:** 217 validated unique chemical structures (202 canonical SMILES).
* **Botanical Diversity:** 51 distinct African medicinal plant species spanning 28 families.
* **Drug-Likeness Compliance:** >80% pass rate across standard oral bioavailability filters.
* **Chemical Space Coverage (PCA):** Multi-dimensional PCA capturing chemical space overlap against reference FDA-approved antidiabetic drugs.

---

##  Repository Directory Structure

```text
AfroDiabDB/
├── data/
│   ├── AfroDiabDB_v1.0.xlsx
│   ├── AfroDiabDB_v1.1.xlsx
│   ├── AfroDiabDB_v1.2_final.xlsx                  # Master curated dataset
│   └── AfroDiabDB_v1.2_Supplementary_Data.xlsx     # Supplementary Tables S1-S4
├── figures/
│   ├── Figure_3_1_Taxonomic_Distribution.png
│   ├── Figure_3_2_Descriptor_Distributions.png
│   ├── Figure_3_3_PCA_Chemical_Space.png
│   ├── Figure_3_4_Compound_Classes.png
│   └── Figure_3_5_Flagship_PCA_Overlay.png
├── tables/
│   └── AfroDiabDB_v1.2_Chapter3_Tables.xlsx        # Summary Tables 3.1-3.6
├── notebooks/
│   └── AfroDiabDB_v1_2_Chapter3_Workflow.ipynb     # Executable Google Colab Notebook
├── requirements.txt
├── LICENSE
└── README.md
