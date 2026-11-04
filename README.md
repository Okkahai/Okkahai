# Gün Deniz

**Software Engineer · Backend Systems, AI/ML & Developer Tools**

I build backend services, developer tooling and machine-learning pipelines, preferably the kind whose behaviour can be checked: explicit state machines, deterministic rules around anything a model produces, and tests that exercise real failure modes.

[LinkedIn](https://linkedin.com/in/g%C3%BCn-deniz-039654298) · [okkahaitemp@gmail.com](mailto:okkahaitemp@gmail.com)

## About

I work part-time as a software developer at ANDRITZ, writing C#/.NET and Python software for industrial process reporting. Most of my own projects are complete systems rather than isolated scripts: a Python or TypeScript backend with background workers and PostgreSQL, a web frontend, Docker for local runs and CI, and documentation that separates what is verified from what is planned.

When a project uses an LLM, the model proposes and ordinary code decides. Evidence is captured by the server, risk rules are fixed, and nothing merges without a backup and passing checks. On the machine-learning side, my hands-on work so far is training and evaluating image classifiers in a university team project, and that is the area I want to go deeper in next.

**Currently interested in:** backend and distributed systems, developer tools for coding agents, reliable AI integration, model evaluation and dataset quality, observability and cloud infrastructure.

## Selected projects

### [AgentOffice](https://github.com/Okkahai/AgentOffice)
*Local-first orchestration for autonomous coding agents · TypeScript, Node.js, SQLite, Git*

Runs CLI coding agents on tasks, each in its own Git branch and worktree, and passes every result through a fixed pipeline before it reaches the main branch: commit, run the project's checks, review, pre-merge backup, merge, post-merge verification.

- Explicit task state machine persisted in SQLite, with restart recovery tested at several crash points
- Dependency-aware scheduler with a parallelism limit; a planner turns a goal into a validated task graph
- Merge safeguards enforced in code: a backup ref is created and re-read before merging, stale or dirty state and failed checks block the merge, the reviewer must differ from the implementing agent, and rollback resets to the recorded backup
- Agent processes run over pipes or a PTY with API keys and tokens stripped from their environment; a local web UI follows the live event stream

Status: the core loop is covered by tests on throwaway repositories and has completed a full run with Claude Code. Codex and OpenCode adapters are not yet tested end to end, the planner is not yet wired into the UI, and the review gate is deterministic; an agent-based reviewer and OS-level sandboxing are on the roadmap.

### [OpsPilot](https://github.com/Okkahai/SREAgent)
*Evidence-first incident investigation for SRE · Python, FastAPI, Celery, PostgreSQL, Redis, OpenTelemetry, Next.js*

Ingests telemetry, detects incidents with deterministic rules, and investigates them with an LLM or built-in rules that may only cite evidence the server captured itself. The only action it can execute is opening a pull request, and only after a human approves that exact payload.

- OTLP ingestion into daily-partitioned PostgreSQL; Celery beat rules for error rate, p95 latency and DB pool saturation drive an incident lifecycle with deduplication and recovery
- Every claim is labelled observation, hypothesis or confirmed fact; a verifier drops uncited claims and caps confidence by the amount of independent evidence
- A fixed policy table assigns risk to proposed actions; approval is bound to a payload hash, execution sits behind a kill switch, and audit rows cannot be edited
- Unit and integration tests, a Playwright smoke test, enforced module layering, dependency and secret scanning, and a CI job that replays the full failure scenario on every pull request; Kubernetes manifests (restricted Pod Security, default-deny network policies) are exercised on `kind`

Status: demonstrated against a bundled demo shop with injectable faults, not a real production system. LLM investigations have only been tested with a scripted stand-in, and pull-request execution only against a mocked GitHub.

### [MarketOS](https://github.com/Okkahai/MarketOS)
*Financial-intelligence and paper-trading lab · Python, FastAPI, Celery, PostgreSQL, Redis, Next.js*

Simulation only: there is no broker integration and it never places real orders. It collects daily prices, news, SEC filings and Fed releases, groups articles into scored events, turns them into signals, trades those signals in a virtual portfolio and later checks each one against a benchmark.

- Point-in-time queries prevent lookahead; a test covers late-arriving price bars
- Append-only signal journal; trades, the cash ledger and risk decisions are protected by database triggers, and money is `Decimal` throughout
- Deterministic risk engine (position size, sector cap, cooldown, drawdown breaker) with next-bar fills, slippage and fees
- Backtests replay the same engine over a past window in an isolated portfolio

Status: the default analyst is a deterministic rules baseline, with an optional Claude analyst. The stock data feed has been verified live; the news feeds and whether the signals have any edge are not yet proven.

### [Alibi](https://github.com/Okkahai/Alibi)
*Daily murder-mystery logic puzzle · TypeScript, Next.js, Zod, Vitest*

A new case every UTC day, generated deterministically from the date. Players work out the culprit, method, room and false alibi from the exhibits.

- Backtracking constraint solver: the generator rejects any clue set that does not have exactly one solution, and the solver's input type cannot include the answer
- Hints come from a clue-only deduction trace; a deduction matrix with undo/redo and keyboard control; an interactive tutorial case
- Published days are frozen by fingerprint: a test regenerates each past case and fails if any has changed, and a scheduled workflow records each new day
- Generated cases are schema-validated before they reach the player

### [AI Information Detection](https://github.com/sssseaurchin/AI-Information-Detection)
*University team project: detecting AI-generated images and text · Python, TensorFlow/Keras, Flask, Docker*

My contributions were on the image-classification track:

- Interchangeable model backbones (a dual-input artifact CNN, EfficientNet, ResNet50, ConvNeXt, CLIP ViT) and a shared preprocessing module with a Haar-wavelet mode
- Manifest-based train, validation and holdout splits; duplicate audits, a fix for exact-duplicate leakage between splits, and corrupt-image cleanup
- Evaluation tooling for temperature-scaling calibration, corruption robustness, ensembles and benchmark sweeps across backbones, with automatic best-run selection
- Logged, rate-limited access to the held-out set with file-hash drift checks, and a Docker GPU training and benchmarking workflow

## Stack

**Languages** · Python, TypeScript, C#, SQL, JavaScript<br>
**Backend** · FastAPI, Celery, SQLAlchemy and Alembic, PostgreSQL, Redis, Node.js, .NET<br>
**AI / ML** · TensorFlow/Keras, pretrained CNN and ViT backbones, model evaluation and calibration, LLM integration<br>
**Frontend** · Next.js, React, Tailwind CSS<br>
**Infrastructure** · Docker and Compose, GitHub Actions, OpenTelemetry, Kubernetes (Kustomize, kind), Linux, Git

## Contact

Open to software engineering roles and internships in backend, AI/ML and platform engineering.

[okkahaitemp@gmail.com](mailto:okkahaitemp@gmail.com) · [gunndenizz@gmail.com](mailto:gunndenizz@gmail.com) · [LinkedIn](https://linkedin.com/in/g%C3%BCn-deniz-039654298)
