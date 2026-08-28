# 📊 Orofacial Myofunctional Therapy for Obstructive Apnea Theraphy in Adults Dataset

| | |
| :--- | :--- |
| **Docs** | [![English](https://img.shields.io/badge/English-EN-blue)](README.md) [![Español](https://img.shields.io/badge/Español-ES-red)](docs/README.es.md) |
| **Open Science** | [![License: CC BY 4.0](https://img.shields.io/badge/License-CC--BY--4.0-lightgrey.svg)](LICENSE) [![Open Science](https://img.shields.io/badge/open%20science-yes-brightgreen)](https://www.fosteropenscience.eu/) [![FAIR Data](https://img.shields.io/badge/FAIR-Compliant-4db8ff)](FAIR.md) |
| **Code** | [![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](notebooks/) |
| **Metadata** | [![DCAT-TTL](https://img.shields.io/badge/meta-DCAT%20TTL-brightgreen)](metadata/dcat.ttl) [![JSON-Schema](https://img.shields.io/badge/metadata-JSON%20Schema-blue)](metadata/metadata_schema.json) [![Schema.org JSON-LD](https://img.shields.io/badge/metadata-JSON%20LD-orange)](metadata/schemaorg.jsonld) [![DOI](https://img.shields.io/badge/metadata-DOI-ff69b4)](metadata/identifiers/doi.txt) [![ORCID](https://img.shields.io/badge/metadata-ORCID-ffb6c1)](metadata/identifiers/orcid_ids.txt) |
| **Cite** | [![DOI: 10.1016/j.rmed.2025.108460](https://zenodo.org/badge/DOI/10.1016/j.rmed.2025.108460.svg)](https://doi.org/10.1016/j.rmed.2025.108460) |

<h4 align="right"><strong>English</strong> | <a href="docs/README.es.md">Español</a> </h4>

---

## 🧭 Overview

This dataset supports the study _"Artificial Intelligence-Enhanced Telemedicine for Orofacial Myofunctional Therapy in Sleep Apnea: Adult Patient Outcomes"_. It includes anonymized clinical and treatment response data from 87 adult patients who underwent AI-assisted Orofacial Myofunctional Therapy (OMT) using the Smart Therapy Manager® system, aimed at treating Obstructive Sleep Apnea (OSA) and Primary Snoring (PS).

### Study Digest

- **Study Type**: Retrospective Observational Cohort  
- **Period**: November 2021 – November 2022  
- **Location**: NEUMOMED Clinic, Medellín, Colombia  
- **Sample Size**: 87 patients  
- **Format**: CSV (anonymized), XLSX, TTL, XML, JSON  
- **Target Use**: Clinical research, machine learning, sleep medicine, treatment outcome analysis.

---

## 📚 Table of Contents
  - [🧭 Overview](#overview)
  - [📚 Table of Contents](#table-of-contents)
  - [📁 Files and Structure](#files-and-structure)
  - [🧬 FAIR Statement](#fair-statement)
  - [📖 Citation](#citation)
  - [🤝 Contributing](#contributing)
  - [📬 Contact](#contact)


---

## 📁 Files and Structure

```
📦 ST-OSA-PS-OMT-Theraphy-Data/
├── data/external/raw/   # Original data files
├── docs/                # Documentation and codebook
├── notebooks/           # Data exploration and analysis notebooks
├── metadata/            # Machine-readable metadata (DCAT, JSON-Schema, etc.)
├── LICENSE
├── CITATION.cff
└── README.md
````

### 📂 Key Files

- `data/external/raw/*.csv`: Primary clinical and treatment datasets (available in English and Spanish).
- `data/external/raw/metadata.csv`: Metadata describing the contents of the raw data files.
- `docs/*.md`: Essential documentation including `data_dictionary.md`, `methodology.md`, and `quality_report.md`.
- `metadata/*.json|ttl|jsonld`: Machine-readable metadata following FAIR principles (DCAT-TTL, JSON-Schema, and Schema.org).
- `notebooks/*.ipynb`: Jupyter notebooks for data exploration, preprocessing, and analysis.

---

## 🧬 FAIR Statement

This dataset follows the [FAIR Data Principles](https://www.go-fair.org/fair-principles/):

- **Findable**: DOI assigned and metadata indexed in open repositories  
- **Accessible**: Openly licensed under CC-BY 4.0 with no access restrictions  
- **Interoperable**: Provided in standard formats with machine-readable metadata  
- **Reusable**: Includes clear licensing, documentation, and citation guidelines

Machine-readable metadata is available in the [`metadata/`](metadata/) folder.

➡️ See the [`FAIR.md`](FAIR.md) file for a complete FAIR compliance breakdown.

---

## 📖 Citation

Please cite both the dataset and the corresponding paper, the suggested BiBtex entry is the following:

```bibtex
@article{RiveraCapacho2025,
author = {{Rivera Capacho}, Eliana Elizabeth and Bossa, Claudia Patricia Diaz and Campos, Mar{\'{i}}a Del Carmen and Rincon-Yanez, Diego and Rangel-Navia, Heriberto and Bianchini, Esther Mandelbaum Gon{\c{c}}alves},
doi = {10.1016/j.rmed.2025.108460},
issn = {15323064},
journal = {Respiratory medicine},
month = {nov},
pmid = {41176093},
title = {{Telemedicine-supported structured Orofacial Myofunctional Therapy model for Obstructive Sleep Apnea: Patients' report outcomes measurements}},
volume = {249},
year = {2025}
}
```

### Acknowledgments

- **NEUMOMED Sleep and Pulmonology Clinic**  
- **University of Pamplona**  
- All contributing authors and patients who consented to data usage

---

## 📜 License

This dataset is shared under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. You are free to reuse, adapt, and distribute it with proper attribution.

This project is licensed under the [CC BY 4.0 License](LICENSE).

## 🤝 Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to contribute to this project.

This project adheres to a [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this standard.


## 📬 Contact

For questions or collaboration inquiries, contact the dataset curators listed in the [`CITATION.cff`](./CITATION.cff).

If there are any troubles or you have any questions, please open an issue stating the encountered problem. Contributing is always welcome. The [Github repository Issues URL](https://github.com/Inneumo/ST-OSA-PS-OMT-Therapy-Data/issues).  And contributing is always welcome. The [Github repository URL](https://github.com/Inneumo/ST-OSA-PS-OMT-Therapy-Data).


Happy hacking!! 🖖🖖.
