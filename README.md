# Milestone 0 - Environment & CI Setup
 
[![CI](https://github.com/AnanyaaaRao/IDS568-MLOPS-PROJECT-ANANYA/actions/workflows/ci.yml/badge.svg)](https://github.com/AnanyaaaRao/IDS568-MLOPS-PROJECT-ANANYA/actions/workflows/ci.yml)
 
## Setup
```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .\.venv\Scripts\activate
pip install -r requirements.txt
pytest -v
```
## Reproducibility and ML Lifecycle Reliability

Reproducibility is a foundational principle in machine learning system development. A reproducible environment ensures that experiments, data preprocessing steps, and model training pipelines produce consistent results when executed across different machines or at different points in time. Without strict control over software versions and dependencies, even minor environmental differences can lead to inconsistent outputs and unreliable conclusions.

In this project, reproducibility is achieved by isolating the Python runtime using a virtual environment and pinning all library dependencies to exact versions in the `requirements.txt` file. This approach guarantees that the same versions of critical libraries such as NumPy, pandas, and scikit-learn are used consistently, eliminating variability caused by dependency drift.

Reproducibility directly supports reliability across the machine learning lifecycle. During data ingestion and preprocessing, consistent library behavior ensures stable feature generation. In the model development and evaluation phases, reproducible environments allow experiments to be reliably compared and validated. Finally, automated testing and continuous integration reinforce reliability by detecting environment or dependency issues early, before they propagate to downstream stages such as deployment or monitoring.

By combining environment isolation, dependency pinning, automated smoke tests, and continuous integration, this milestone establishes a reliable foundation for building, testing, and scaling machine learning systems throughout the ML lifecycle.
