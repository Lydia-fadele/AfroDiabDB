# 🌿 AfroDiabDB v1.3: A Curated Chemoinformatics Database of African Antidiabetic Phytochemicals

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22046751.svg)](https://doi.org/10.5281/zenodo.22046751)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)

---

## 📌 Overview

**AfroDiabDB v1.3** (`AfroDiabDB_Master_23_Sheets`) is an open-access, manually curated ethnobotanical and chemoinformatics database cataloging antidiabetic phytochemicals isolated from African medicinal flora.

The **v1.3 release** integrates literature-derived ethnobotanical information with PubChem API verification, RDKit-computed molecular descriptors, drug-likeness filter evaluations (*Lipinski, Veber, Ghose*), Quantitative Estimate of Drug-likeness (*QED*) scoring, and multi-dimensional chemical space comparison against benchmark FDA-approved antidiabetic drugs.

---

## 📊 Release v1.3 Metrics Summary

* **Total Occurrence Records:** 248 curated entries across 38 standardized metadata fields.
* **Unique Chemical Entities:** 203 validated unique chemical structures (canonical SMILES / InChIKeys).
* **Botanical Diversity:** 49 distinct African medicinal plant species spanning 28 families.
* **Drug-Likeness Compliance:** >80% pass rate across standard oral bioavailability filters.
* **Chemical Space Coverage (PCA):** Multi-dimensional PCA capturing chemical space overlap against reference FDA-approved antidiabetic drugs.

---

## 💾 Multi-Format Data Availability

To support computational workflows, molecular modeling, and database integration, **AfroDiabDB v1.3** is provided in three standardized file formats:

| Format | File Path | Use Case |
| :--- | :--- | :--- |
| **Excel (`.xlsx`)** | `data/raw/AfroDiabDB_Master_23_Sheets.xlsx` | Master 23-sheet relational workbook containing all raw datasets, metadata schema, and statistical summary tables. |
| **CSV (`.csv`)** | `data/processed/AfroDiabDB_v1.3_standard.csv`<br>`data/processed/AfroDiabDB_Unique_Structures.csv` | Machine-readable tabular datasets for pandas, R, and automated data science pipelines. |
| **SDF (`.sdf`)** | `data/processed/AfroDiabDB_Unique_Structures.sdf` | 2D/3D structure files containing 3D-ready chemical representations and annotated property fields for virtual screening, docking, and QSAR. |

---

## 📁 Repository Directory Structure

```text
AfroDiabDB/
├── data/
│   ├── raw/
│   │   └── AfroDiabDB_Master_23_Sheets.xlsx          # Master 23-sheet Excel database
│   └── processed/
│       ├── AfroDiabDB_v1.3_standard.csv              # Machine-readable occurrence CSV
│       ├── AfroDiabDB_Unique_Structures.csv          # Machine-readable unique structures CSV
│       ├── AfroDiabDB_Unique_Structures.sdf          # 2D/3D Chemical structure file (SDF)
│       └── FDA_Antidiabetic_Benchmark.csv            # Benchmark set
├── outputs/
│   ├── figures/
│   │   ├── Figure_3.1_Taxonomic_Distribution.png
│   │   ├── Figure_3.2_Descriptor_Distributions.png
│   │   ├── Figure_3.3_PCA_Chemical_Space.png
│   │   └── Figure_3.9_PCA_Chemical_Space.png         # High-res chemical space plot
│   └── tables/
│       └── Table_3.6_Descriptor_Summary.csv          # Descriptor statistics table
├── notebooks/
│   └── AfroDiabDB_Master_Pipeline.ipynb             # Reproducible computational pipeline
├── requirements.txt
├── LICENSE
└── README.md
```

---

## 📖 Citation

If you use **AfroDiabDB v1.3** in your research, please cite this dataset as follows:

```bibtex
@dataset{fadele2026afrodiabdb,
  author    = {Fadele, Lydia Onowumi},
  title     = {{AfroDiabDB v1.3: A Curated Chemoinformatics Database of African Antidiabetic Phytochemicals}},
  month     = aug,
  year      = 2026,
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.22046751},
  url       = {https://doi.org/10.5281/zenodo.22046751}
}
```

---

## 👤 Author & Academic Affiliation

**Lydia Onowumi Fadele**  
*M.Sc. Drug Discovery and Development, University of Lagos*  
📧 Contact: diamondlydia19@gmail.com