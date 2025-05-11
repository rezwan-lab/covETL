# SARS-CoV-2 Genomic Surveillance Toolkit

A comprehensive suite of Python-based tools for large-scale SARS-CoV-2 genomic surveillance, lineage classification, mutation profiling, and real-time data transformation. This toolkit was instrumental in supporting national and international pandemic response efforts by enabling fast, efficient, and automated analysis of GISAID and Nextstrain metadata at scale. With thousands of SARS-CoV-2 sequences being generated weekly across India and globally, manual curation and analysis became impractical. To address this challenge, we developed a robust and modular toolkit that streamlines the end-to-end workflow—from **Extract-Transform-Load (ETL)** to variant classification and mutation-based reporting.

This toolkit was deployed across multiple genomic surveillance projects, including India's national SARS-CoV-2 genomic surveillance (INSACOG) and BRICS-NGS networks. It was designed to:

- Ingest and normalize high-volume genomic metadata
- Classify lineages into WHO-defined variants (e.g., VOC, VOI, VUM)
- Explode amino acid mutations and group them by gene, position, and effect
- Perform weekly and monthly batch analyses
- Generate Excel and TSV reports for integration with dashboards and government briefings

Whether you're managing a genomic surveillance lab or analyzing global trends for public health insights, this toolkit provides scalable and reproducible workflows for variant monitoring and mutation analytics.

---

## Key Features

- 📊 **Exploratory Data Analysis (EDA)**: Clean and visualize Nextstrain metadata with lineage classification and mutation statistics.
- 🧬 **Lineage Classification**: Map Pango lineages to WHO-recognized variants using batch logic and ImpLin tagging.
- 🔬 **Mutation Profiling**: Extract, parse, and explode amino acid changes with gene and position-based summaries.
- 📁 **ETL Pipeline Automation**: Fully automated extraction, transformation, and loading of large-scale metadata files.
- 📈 **Pivot Tables & Interactive Reports**: HTML pivot tables, Excel/TSV exports for seamless reporting.
- 🧠 **Batch Processing Support**: Handle high-throughput weekly/monthly batches with reproducible analytics.

---

## 🧪 Scripts Overview

| Script | Purpose |
|--------|---------|
| `wa_analysis_v3.py` | Full mutation and lineage analysis pipeline, generates pivot tables and summary sheets |
| `etl_sars_cov_2_surveillance.py` | ETL pipeline: clean, transform, classify, and enrich metadata |
| `eda_sars_cov_2_surveillance.py` | Explore lineage distributions and generate mutation status |
| `example_batch_lineage.py` | Batch lineage parsing and ImpLin classification from weekly metadata |
| `example_batch_mutation.py` | Batch mutation-level processing across time-sliced reports |
| `batch_mutation_analysis.py` | Weekly mutation pattern analysis with lineage/variant annotation |
| `aa_explode.py` | Amino acid mutation parser and exploder (by gene and AA position) |
| `lineage_status.py` | Annotates lineage status and assigns VOC/VOI classification tags |

---

## Input Format

- Input files should be `.tsv` (tab-separated) format from GISAID, Nextstrain, or custom pipelines.
- Required columns include: `lineage`, `aaSubstitutions`, `date`, `division`, `clade`, etc.

## Output Files

- Cleaned datasets in `.tsv` or `.xlsx` for downstream reporting
- Mutation explosion tables with gene and position breakdown
- WHO Variant Classification (VOC, VOI, Monitoring)
- Interactive HTML pivot tables for visualization
- Summary sheets for recent months (e.g., May–August analysis)


## Requirements

- Python 3.7+
- Required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `pivottablejs`


## Author

Rezwanuzzaman Laskar

Lead Bioinformatician, INSACOG & NGS-BRICS
