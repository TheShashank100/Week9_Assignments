# Week 9 Assignments

Software Engineering | CT State Community College Housatonic

---

## Overview

This repository contains all Week 9 deliverables covering CI/CD pipeline design, build and deployment documentation, and supporting diagrams.

---

## Repository Structure

```
/
├── README.md
└── docs/
    ├── srs.md
    ├── architecture.md
    ├── design.md
    ├── test-strategy.md
    ├── test-cases.md
    ├── test-traceability.md
    ├── ci-cd-workflow.md
    ├── build-deploy-guide.md
    └── images/
        └── ci-cd-diagram.png
```

---

## Deliverables

### CI/CD Workflow
Describes the full CI/CD pipeline including all stages from developer commit to production deployment.
[View Document](docs/ci-cd-workflow.md)

### Build and Deployment Guide
Step-by-step guide covering project setup, build process, and deployment to cloud platforms.
[View Document](docs/build-deploy-guide.md)

### CI/CD Pipeline Diagram
Visual diagram of the pipeline stages.
[View Diagram](docs/images/ci-cd-diagram.png)

---

## Pipeline Summary

| Stage | Tool |
|---|---|
| Version Control | GitHub |
| CI Pipeline | GitHub Actions |
| Build | npm, pip |
| Testing | pytest, Jest |
| Code Quality | ESLint, Flake8 |
| Deployment | Vercel, Railway, Docker |
