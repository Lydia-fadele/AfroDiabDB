# AfroDiabDB

**A Curated Chemoinformatics Database of Antidiabetic Phytochemicals from African Medicinal Plants**



![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.21952953-blue)

(https://doi.org/10.5281/zenodo.21952953)


![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)

(https://creativecommons.org/licenses/by/4.0/)

---

## Overview

**AfroDiabDB** is a curated, structure-validated chemoinformatics database of natural antidiabetic phytochemicals reported from African medicinal plants, benchmarked against clinically approved antidiabetic drugs. The database was built to support natural product-based drug discovery research, offering a machine-readable, structurally verified resource for virtual screening, chemical space analysis, and drug-likeness profiling.

Every compound entry in AfroDiabDB has been:
- Structurally validated and standardized directly from SMILES using **RDKit**
- Cross-checked against **PubChem** for identity and molecular formula consistency
- Annotated with literature references (DOI/URL) verified for resolvability
- Scored for drug-likeness using **Lipinski's Rule of Five**, **Veber**, and **Ghose** filters
- Scored for **QED (Quantitative Estimate of Drug-likeness)**

The database also includes a benchmark set of clinically approved antidiabetic drugs, enabling direct comparison of the chemical space, physicochemical profile, and drug-likeness of African phytochemicals against existing therapeutics.

---

## Repository Structure

AfroDiabDB/
├── data/
│   ├── AfroDiabDB.xlsx                          # Master workbook (both sheets, corrected)
│   ├── AfroDiabDB_Natural_Products.csv          # Natural product compound records
│   ├── AfroDiabDB_Clinically_Approved_Drugs.csv # Benchmark drug records
│   ├── AfroDiabDB_Natural_Products.sdf          # Structure-data file (natural products)
│   └── AfroDiabDB_Clinically_Approved_Drugs.sdf # Structure-data file (benchmark drugs)
├── figures/
│   └── Figure_3_1 – Figure_3_11                 # Chapter 3 publication-ready figures
├── tables/
│   └── Table_3_1 – Table_3_9                    # Chapter 3 summary and statistical tables
├── notebooks/
│   └── AfroDiabDB_Master_Pipeline.ipynb          # Full reproducible analysis pipeline
└── README.md

---

## Dataset Contents

### 1. Natural Products Sheet
Occurrence-level records of phytochemicals isolated or reported from African medicinal plants, including:
- Compound identity (name, PubChem CID, InChIKey, canonical SMILES)
- Botanical source (plant name, family, plant part used, country of traditional use)
- Compound classification (phytochemical superclass)
- Computed molecular descriptors (see below)
- Drug-likeness filter outcomes
- Literature reference and QC status

### 2. Clinically Approved Drugs Sheet (Benchmark Set)
A reference panel of regulatory-approved antidiabetic drugs (FDA and other regulatory bodies — EMA/CDSCO/PMDA), used as a comparative benchmark for chemical space and drug-likeness analysis.

### Computed Molecular Descriptors
All descriptors were computed directly from canonical SMILES using RDKit, ensuring internal consistency across the dataset:

| Descriptor | Description |
|---|---|
| Molecular Formula | Computed from structure |
| Molecular Weight | g/mol |
| LogP | Crippen octanol-water partition coefficient |
| HBD / HBA | Hydrogen bond donors / acceptors |
| TPSA | Topological polar surface area |
| Rotatable Bonds | Molecular flexibility |
| Fraction Csp3 | Degree of saturation |
| Ring Count / Aromatic Ring Count | Structural complexity |
| Heavy Atom Count | — |
| Molar Refractivity | — |
| QED Score | Quantitative Estimate of Drug-likeness |

### Drug-Likeness Filters Applied
- **Lipinski's Rule of Five**
- **Veber's Rule**
- **Ghose Filter**

---

## Data Validation & Quality Control

AfroDiabDB underwent a multi-tier validation process to ensure structural and referential integrity:

1. **Structural validity** — every SMILES parsed and sanitized through RDKit; invalid structures flagged for manual review.
2. **PubChem cross-check** — molecular formula of each entry verified against its PubChem CID.
3. **Reference resolution check** — every literature citation (DOI or URL) programmatically tested for resolvability.
4. **Structural consistency check** — compound names flagged where multiple SMILES were reported for the same name, for manual disambiguation.
5. **Benchmark drug structures** — canonical SMILES for clinically approved drugs pulled directly from PubChem to ensure reference-grade accuracy.

A full change log documenting every correction made to the original curated dataset is generated as part of the pipeline for full transparency and reproducibility.

---

## Analysis & Figures

The accompanying pipeline generates a complete set of chemoinformatic analyses and figures, including:

- Database composition summary (plant families, plant parts, phytochemical superclasses, countries of use)
- Descriptive statistics of molecular descriptors (AfroDiabDB vs. benchmark drugs)
- Drug-likeness pass-rate comparison (Lipinski, Veber, Ghose)
- QED score distribution and categorization
- Pearson correlation heatmap of molecular descriptors
- Principal Component Analysis (PCA) — scree plot, score plot, and loading biplot comparing the chemical space of African phytochemicals against approved antidiabetic drugs
- Normalized descriptor radar plot
- Geographic distribution of compound provenance across Africa

All figures are exported at publication-ready resolution (300 dpi).

---

## Reproducibility

The full curation, validation, analysis, and export pipeline is provided as a single, reproducible Jupyter/Colab notebook (`notebooks/AfroDiabDB_Master_Pipeline.ipynb`), built with:

- [RDKit](https://www.rdkit.org/) — cheminformatics toolkit for structure standardization and descriptor calculation
- [PubChemPy](https://pubchempy.readthedocs.io/) — PubChem API interface for structural cross-validation
- `pandas`, `numpy` — data handling
- `matplotlib`, `seaborn` — visualization
- `scikit-learn` — PCA and standardization

To reproduce the full pipeline, open the notebook in Google Colab, mount your data source, and run all cells sequentially.

---

## Citation

If you use AfroDiabDB in your research, please cite:

> Fadele, L. O. (2026). *AfroDiabDB: A Curated Chemoinformatics Database of Antidiabetic Phytochemicals from African Medicinal Plants* [Data set]. Zenodo. https://doi.org/10.5281/zenodo.21952953

```bibtex
@dataset{fadele_afrodiabdb,
  author       = {Fadele, Lydia Omowumi},
  title        = {AfroDiabDB: A Curated Chemoinformatics Database of Antidiabetic Phytochemicals from African Medicinal Plants},
  year         = {2026},
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.21952953},
  url          = {https://doi.org/10.5281/zenodo.21952953}

License
This dataset is released under the Creative Commons Attribution 4.0 International License (CC BY 4.0). You are free to share and adapt the material for any purpose, provided appropriate credit is given.


Author & Academic Affiliation
Lydia Omowumi Fadele
M.Sc. Drug Discovery and Development, University of Lagos
Drug Discovery Scientist | Natural Product Chemist | Chemoinformatician
📧 Contact: diamondlydia19@gmail.com


Acknowledgements
AfroDiabDB was developed as part of ongoing research into natural product-based drug discovery for diabetes management, drawing on structural and pharmacological data curated from published literature on African medicinal plants.
Contributing
Corrections, additional compound records, and literature updates are welcome. Please open an issue or submit a pull request with supporting references for any proposed additions
