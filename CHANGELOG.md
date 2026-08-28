# 📦 Changelog

All notable changes to this dataset are documented in this file.
This project adheres to [Semantic Versioning](https://semver.org/).

---

## [2.0.0] - 2026-08-27

### Added

* **`.zenodo.json`** – Added complete Zenodo metadata for DOI registration and open-science compliance.
* **`doi.txt`** – Added the dataset DOI extracted from `CITATION.cff`.
* **`orcid_ids.txt`** – Added a consolidated list of author ORCID identifiers.
* **`metadata_schema.json`** – Added a machine-readable JSON Schema describing the dataset metadata and structure.
* **`schemaorg.jsonld`** – Added Schema.org JSON-LD metadata for dataset discovery and catalog indexing.
* **`dcat.ttl`** – Added DCAT metadata in Turtle format for RDF-based data catalogues.
* **`datapackage.json`** – Added a Frictionless Data Package describing the dataset resources and their structure.
* **`CHANGELOG.md`** – Added structured version history for the dataset.
* **Metadata documentation** – Expanded the repository metadata to support FAIR data principles and improved machine readability.

### Changed

* **`README.md`** – Rewritten with updated badges, clearer documentation, metadata information, dataset description, and links to metadata resources.
* **`CITATION.cff`** – Updated formatting and metadata to align with the current Citation File Format schema.
* **`metadata_schema.json`** – Corrected the dataset name and updated the repository URL.
* **`schemaorg.jsonld`** – Updated the dataset URL and keywords to remain consistent with the repository documentation.
* **`dcat.ttl`** – Updated publisher affiliation information to reflect the current institutional affiliation.
* **Dataset metadata** – Improved consistency between repository, citation, DOI, and machine-readable metadata.

### Fixed

* **`orcid_ids.txt`** – Removed duplicate ORCID identifiers.
* **`doi.txt`** – Corrected the DOI format to match the registered dataset record.
* **Metadata consistency** – Corrected inconsistencies between dataset name, repository URL, DOI, keywords, and publisher information.

### Deprecated

* None.

### Removed

* None.

### Security

* None.

---

## [1.0.0] - Initial Release

### Added

* **Initial dataset release** – Published the first version of the Orofacial Myofunctional Therapy dataset.
* **Clinical dataset** – Included anonymized clinical and treatment-response data from **87 adult patients** who underwent AI-assisted Orofacial Myofunctional Therapy (OMT).
* **Study population** – Included participants with **Obstructive Sleep Apnea (OSA)** and **Primary Snoring (PS)**.
* **Study period** – Dataset covered the period from **November 2021 to November 2022**.
* **Study location** – Data were collected at **NEUMOMED Clinic, Medellín, Colombia**.
* **Data format** – Provided the primary dataset in CSV format.
* **Basic metadata** – Included fundamental information describing the dataset, study design, population, period, location, format, and intended research use.
* **Repository documentation** – Added an initial `README.md` describing the dataset and its intended use.
* **Citation information** – Added initial citation information for the dataset and associated scientific publication.
* **License information** – Provided licensing information for reuse of the dataset.

### Dataset Scope

The initial release supports research in:

* Clinical research
* Sleep medicine
* Obstructive Sleep Apnea research
* Primary Snoring research
* Orofacial Myofunctional Therapy
* Treatment-outcome analysis
* Artificial intelligence and machine learning
* Telemedicine and digital health

### Metadata

Version 1 provided **basic dataset metadata** intended to make the dataset understandable and reusable. The initial release did not yet include the expanded machine-readable metadata and FAIR infrastructure introduced in Version 2.

### Changed

* None. This was the initial public dataset release.

### Fixed

* None.

### Deprecated

* None.

### Removed

* None.

### Security

* No known security changes.

---

## Version History

| Version   | Date            | Description                                                                                                    |
| --------- | --------------- | -------------------------------------------------------------------------------------------------------------- |
| **1.0.0** | Initial Release | Initial dataset upload with basic metadata and documentation.                                                  |
| **2.0.0** | 2026-08-27      | Expanded metadata, FAIR infrastructure, DOI/ORCID resources, schemas, and machine-readable catalogue metadata. |

## Source Repository

The dataset is based on the **Orofacial Myofunctional Therapy Survivor Dataset** repository:

[ST-OSA-PS-OMT-Teraphy-Data on GitHub](https://github.com/Inneumo/ST-OSA-PS-OMT-Teraphy-Data?utm_source=chatgpt.com)

The source repository describes the dataset as an open clinical dataset supporting research on AI-assisted Orofacial Myofunctional Therapy for OSA and Primary Snoring.
