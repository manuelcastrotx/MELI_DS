# MELI Project
Manuel Castro (manuel.castro@utexas.edu)


## Overview

This repository contains notebooks and scripts to build a documentation corpus, explore raw data files, and generate Q&A pairs.

Included files:

- `Solution/EDA.ipynb`
  - Exploratory data analysis of the raw documentation folders.
  - Lists file types and creates a distribution chart of content formats.

- `Solution/corpus_build.ipynb`
  - Builds corpus files from Markdown, JSON, and YAML documentation.
  - Extracts and normalizes content into JSONL entries with project, path, version, section, and content fields.
  - Generates consolidated corpus files under `Solution/corpus/`.

- `Solution/Q&A_Build.ipynb`
  - Reads generated corpus data and creates question-answer pairs.
  - Uses Ollama to enforce JSON output for Q&A generation.
  - Saves the final Q&A dataset under `Solution/Q&A/qa.jsonl`.

## Data paths

- Raw documentation: `docs_raw/`
- Generated corpus output: `Solution/corpus/`
- Generated Q&A output: `Solution/Q&A/`

## Dependencies

Required Python packages:

- pandas
- numpy
- plotly
- ollama
- pyyaml

Standard library modules used:

- os
- json

Install dependencies with:

```bash
pip install pandas numpy plotly pyyaml ollama
```

For LLAMA 3.1

```bash
ollama pull llama3.1:latest
```