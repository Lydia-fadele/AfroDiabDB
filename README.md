# AfroDiabDB: Ethnobotanical & Cheminformatics Database

## Overview
**AfroDiabDB** is an open-access ethnobotanical and cheminformatics database cataloging anti-diabetic phytochemicals isolated from African medicinal plants.

The **v1.1 release** integrates literature-derived ethnobotanical information with PubChem API verification, RDKit-computed molecular descriptors, drug-likeness evaluations, and chemical space mapping.

---

## Release v1.1 Metrics Summary
- **Total Ethnobotanical Records:** 223 entries across 17 standardized headings.
- **Unique Chemical Entities:** 122 validated unique chemical structures.
- **Lipinski Compliance:** 82.0% (<= 1 violation).
- **Chemical Space Coverage (PCA):** 88.7% cumulative variance captured (PC1 + PC2).

---

## Repository Directory Structure
```
├── data/
│   ├── AfroDiabDB_v1.1_Full_Master_Curated.xlsx
│   ├── AfroDiabDB_v1.1_Full_Master_Curated.csv
│   └── AfroDiabDB_v1.1_Unique_Library_Curated.xlsx
├── figures/
│   ├── AfroDiabDB_Property_Distributions.png
│   └── AfroDiabDB_Chemical_Space_PCA.png
└── README.md
```

---

## Workflow Summary
1. **Curation & Verification:** Standardized metadata and PubChem API verification.
2. **Descriptor Computation:** RDKit evaluation of MW, LogP, HBD, HBA, TPSA, Rotatable Bonds, and QED scores.
3. **Bioavailability Assessment:** Drug-likeness evaluations via Lipinski, Veber, and Ghose rules.
4. **Chemical Space Mapping:** Principal Component Analysis (PCA) across physical descriptors.
