# Harness Engineering Masterclass

A hands-on workshop for learning how to build, test, deploy, and govern AI/ML services using Harness.

This repository walks through a practical delivery journey for a Python-based machine learning application, from local development to production pipeline automation. The labs are organized as Jupyter notebooks and cover CI, CD, feature flags, and production governance patterns.

## Overview

The workshop demonstrates how Harness can be used to automate the full software delivery lifecycle for ML workloads:

- Build and validate code with CI pipelines
- Package applications with Docker
- Deploy to Kubernetes
- Use feature flags for safe model rollout
- Enforce approval and policy controls in production
- Reuse pipeline patterns across teams and environments

## Repository structure

```text
.
├── 01_introduction.ipynb
├── 02_poc1_ci_pipeline.ipynb
├── 03_poc2_cd_kubernetes.ipynb
├── 04_poc3_feature_flags.ipynb
├── 05_poc4_production_pipeline.ipynb
├── README.md
└── .git/
```

## Learning path

### 1. Introduction
File: `01_introduction.ipynb`

Introduces the core Harness concepts:

- CI/CD fundamentals
- Pipelines, stages, steps, and artifacts
- Services, environments, and triggers
- Connectors, delegates, and secrets
- YAML-based pipeline structure

### 2. POC 1: CI Pipeline
File: `02_poc1_ci_pipeline.ipynb`

Builds a simple sentiment-analysis ML app and automates its validation flow.

Topics include:

- training a scikit-learn model
- building a FastAPI prediction service
- writing tests with `pytest`
- containerizing the app with Docker
- defining a Harness CI pipeline

Typical flow:

```text
git push -> install dependencies -> run tests -> build image -> push artifact
```

### 3. POC 2: CD Pipeline to Kubernetes
File: `03_poc2_cd_kubernetes.ipynb`

Covers deployment automation for containerized ML applications.

Topics include:

- Kubernetes Deployment and Service manifests
- Harness Service and Environment objects
- rolling deployment patterns
- canary and blue-green deployment strategies

### 4. POC 3: Feature Flags for ML Experimentation
File: `04_poc3_feature_flags.ipynb`

Shows how feature flags can be used to reduce release risk and enable safe experimentation.

Topics include:

- kill switch patterns
- staged rollouts
- A/B testing multiple model versions
- user-targeted traffic routing

### 5. POC 4: Full Production Pipeline
File: `05_poc4_production_pipeline.ipynb`

Combines the earlier concepts into a realistic production delivery workflow.

Topics include:

- reusable pipeline templates
- approval gates
- policy-as-code checks
- dev/staging/production stages
- end-to-end governance and delivery patterns

## Example application

The workshop uses a lightweight text-classification API as the sample ML service. It demonstrates how a real-world AI/ML application can be delivered using a modern software delivery platform.

The app includes:

- text sentiment classification with scikit-learn
- REST API for prediction requests
- health and readiness endpoints
- Docker packaging for deployment

## Tech stack

- Python
- FastAPI
- scikit-learn
- pytest
- Docker
- Kubernetes
- YAML
- Harness CI/CD
- Feature flags and policy-as-code concepts

## Prerequisites

To get the most out of this workshop, you should have:

- Python 3.9+
- Jupyter Notebook or JupyterLab
- Familiarity with Python and basic ML workflows
- Docker installed locally
- Access to a Kubernetes environment or sandbox cluster for deployment exercises
- A Harness account or sandbox environment for pipeline experimentation

## Recommended order

1. Start with `01_introduction.ipynb`
2. Complete `02_poc1_ci_pipeline.ipynb`
3. Continue with `03_poc2_cd_kubernetes.ipynb`
4. Move to `04_poc3_feature_flags.ipynb`
5. Finish with `05_poc4_production_pipeline.ipynb`

## Notes

- This repository is designed for learning and demonstration.
- The notebooks generate YAML, manifests, and example pipeline definitions to illustrate how Harness operates in real delivery scenarios.
- It is not intended to be a production deployment blueprint using real secrets or vendor credentials.

## Goal

The goal of this workshop is to give developers, platform engineers, and ML practitioners a practical understanding of how Harness can automate and govern AI/ML application delivery from development through production.

---

This project is intended as a learning repository for practical Harness-based software delivery patterns in Python and AI/ML environments.
