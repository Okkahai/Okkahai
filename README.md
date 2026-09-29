<div align="center">

# Gün Deniz

**Software Developer · Industrial Automation · Machine Learning**

Building reliable software for industrial processes at **ANDRITZ**, and growing toward machine learning and data-driven systems.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/g%C3%BCn-deniz-039654298)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:okkahaitemp@gmail.com)

</div>

---

## About

I'm a software developer working part-time at **ANDRITZ**, where I build software for industrial automation and process reporting. Day to day I work with **C# / .NET** and **Python**, and I'm currently deepening my skills in **machine learning and deep learning**.

| | |
|---|---|
| **Role** | Software Developer (part-time) @ ANDRITZ |
| **Focus** | Industrial automation and SCADA, full-stack development, data analysis |
| **Learning** | Neural networks, deep learning, TensorFlow |
| **Open to** | Internships, junior roles and collaboration |

## Tech Stack

**Languages**
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![Python](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54)
![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=flat-square&logo=javascript&logoColor=F7DF1E)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

**Frameworks and libraries**
![.NET](https://img.shields.io/badge/.NET-5C2D91?style=flat-square&logo=dotnet&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![DevExpress](https://img.shields.io/badge/DevExpress-FF5722?style=flat-square&logoColor=white)

**Data and cloud**
![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0072C6?style=flat-square&logo=microsoftazure&logoColor=white)

**Tools**
![Git](https://img.shields.io/badge/Git-F05033?style=flat-square&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-0DB7ED?style=flat-square&logo=docker&logoColor=white)
![Visual Studio](https://img.shields.io/badge/Visual%20Studio-5C2D91?style=flat-square&logo=visualstudio&logoColor=white)

## Projects

### [AI Information Detection (AID)](https://github.com/sssseaurchin/AI-Information-Detection)
*Team graduation project · Python, TensorFlow, Flask, Docker*

Detects AI-generated content in images (CNN) and text (LSTM), served through a Flask API with a web frontend.

- **What I did:** Built most of the image-detection track: seven interchangeable architectures (custom CNNs, EfficientNet, ResNet50, ConvNeXt, CLIP ViT), RGB, Sobel and wavelet preprocessing, manifest-based train/val splits, a benchmark runner, calibration, corruption-robustness evaluation and dataset audit tooling.
- **What I learned:** Evaluation matters as much as the model. Duplicate images leaking between train and validation splits inflate results, so I built tools to find and fix them. I also learned to compare backbones fairly with reproducible splits and to run training in Docker.

### OpsPilot (SREAgent) · *going public soon*
*Python, FastAPI, Celery, PostgreSQL, Redis, OpenTelemetry, Next.js, Docker*

AI-assisted DevOps/SRE platform that follows an incident from failure to root cause: telemetry ingestion, deterministic incident detection, AI investigation, proposed fixes and human approval.

- **What I did:** Designed the architecture and built it in phases: a demo microservice app with fault injection, an OpenTelemetry ingestion pipeline with partitioned Postgres storage, rule-based incident detection with a timeline, AI investigation, read-only GitHub integration, an approval workflow and a dashboard.
- **What I learned:** Observability with OpenTelemetry, background job design with Celery, and how to keep AI output trustworthy by labelling every claim as observation, hypothesis or confirmed fact and by requiring human approval for risky actions.

### ColdCase AI (Alibi) · *going public soon*
*TypeScript, Next.js, Zod, Tailwind, Drizzle, PostgreSQL, Vitest*

AI detective game where the player questions suspects, examines evidence and catches contradictions against a case truth that is fixed before play begins.

- **What I did:** Wrote ten design documents first, then built the game engines: case-truth schema, NPC knowledge, evidence and interrogation systems, with a test suite that checks the anti-hallucination guarantees. It runs without an API key using a deterministic mock LLM.
- **What I learned:** Constraining an LLM with schema validation so it cannot contradict the ground truth, and testing AI features deterministically.

### MarketOS · *going public soon*
*Python, FastAPI, Celery, PostgreSQL, Redis, Next.js, TypeScript, Docker*

AI financial-intelligence and **paper-trading** lab (simulation only, no real orders). It collects market data and news, clusters news into events, produces AI investment hypotheses, runs them through deterministic risk rules and measures afterwards whether each hypothesis was right.

- **What I did:** Built the full pipeline across nine phases: market data and news ingestion, event clustering, a validated AI signal journal with cost budgeting, a risk engine with a ledger, analytics against SPY, BTC and cash, and backtesting.
- **What I learned:** Financial accounting and risk rules, avoiding invented data when providers are missing, and measuring AI predictions instead of trusting them.

### SoulCurve · *going public soon*

## GitHub Metrics

<div align="center">

![GitHub metrics](./github-metrics.svg)

</div>

## What I'm Working On

- Machine learning coursework: neural networks, deep learning and data analysis with TensorFlow
- Reporting tools and dashboards for industrial process data
- Desktop applications with C# and .NET
- Python for automation and data science

## Get in Touch

I'm happy to talk about roles, projects or anything in software and data.

- Email: [okkahaitemp@gmail.com](mailto:okkahaitemp@gmail.com) · [gunndenizz@gmail.com](mailto:gunndenizz@gmail.com)
- LinkedIn: [Gün Deniz](https://linkedin.com/in/g%C3%BCn-deniz-039654298)
