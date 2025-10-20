
Key design principles:
- **Separation of concerns:** ingestion, preprocessing, model calls and persistence are separate modules.  
- **Determinism:** preprocessing and parsing are deterministic to make model outputs auditable.  
- **Minimal coupling to model provider:** model call logic is wrapped so provider or prompts can be swapped without changing pipeline.  
- **Export-first:** outputs are structured for analytics (parquet schema / timestamped partitions).

---

## Features
- Async, rate-aware Twitter ingestion utilities  
- Reusable preprocessing pipeline (cleaning, normalization, basic NLP features)  
- Prompt templates and a safe response parser for GenAI outputs  
- Output writers: CSV and parquet support  
- Example notebooks / scripts demonstrating local runs and schematized outputs  
- Tests for preprocessing and parser components (unit tests)

---

## Getting started

### Requirements
- Python 3.10+  
- Recommended: virtualenv / venv or conda environment

### Installation
```bash
git clone https://github.com/mgamzec/sentiment-analysis-GenAI.git
cd sentiment-analysis-GenAI
python -m venv .venv
source .venv/bin/activate        # macOS / Linux
# .venv\Scripts\activate         # Windows
pip install --upgrade pip
pip install -r requirements.txt

