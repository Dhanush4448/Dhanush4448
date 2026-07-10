# Dhanush Neelakantan

Backend/data engineer. M.S. Computer Science from George Mason University. I build systems that ingest, index, and make sense of large amounts of data — mostly with Python, FastAPI, Postgres, and whatever LLM tooling actually earns its place in the stack.

[LinkedIn](https://www.linkedin.com/in/dhanush-neelakantan-15b4481bb/) · dhanushneelakantan2002@gmail.com

## What I've built

**VisaTrack** — [visatrack.vercel.app](https://visatrack.vercel.app)
Pulled all publicly available DOL LCA filings (403K+ records) into Postgres and built semantic search over them using pgvector with HNSW indexing, so you can ask plain-language questions about H-1B sponsorship instead of digging through raw government spreadsheets. FastAPI backend, Next.js frontend, Groq for the LLM layer. Ingestion re-runs itself quarterly via GitHub Actions when DOL publishes new data.

**LegacyLens**
A tool for making sense of codebases you didn't write. Embeds the repo with sentence-transformers, stores it in pgvector, and lets you semantically search across it, auto-generate docs, and get a rough tech-debt score. Built this after being dropped into unfamiliar codebases one too many times and wanting something better than grep.

**Sentinel OTA**
A telemetry ingestion pipeline for fleet data, built around the assumption that things will fail. Four worker processes, batches committed atomically in groups of 500, and a chaos injector I use to deliberately break things and see what recovers cleanly (currently exposes a gap where failures fall through to manual triage — working on closing that).

**Sentinel GCP**
Multi-tenant identity service on GKE/Cloud Run. Nothing fancy conceptually, just tuned hard for latency — sub-200ms at p95 under load.

**RepoMedic**
Multi-agent bug detection using LangGraph — agents split up the work of scanning, reasoning about, and flagging issues across a codebase.

## Stack

Python, FastAPI, PostgreSQL/pgvector, Next.js, Docker, GCP/GKE, LangChain/LangGraph, Redis, Kubernetes.

## Right now

Completed my M.S. and looking for full-time roles in data engineering, backend, or applied ML/AI engineering — open to the US. If any of the above is relevant to something you're hiring for, my LinkedIn is the fastest way to reach me.
