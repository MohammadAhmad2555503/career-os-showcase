# Architecture Brief: Career OS

## Shape

Career OS is a modular monolith for one local user. The design keeps clear service boundaries so SQLite, local files, deterministic retrieval, and the local UI can later evolve toward PostgreSQL, object storage, scalable retrieval, and richer client surfaces.

## Core Boundaries

- app/database: SQLite connection and migrations.
- career_brain: profile, skills, goals, preferences, CV ingestion, evidence verification.
- project_brain: safe import, static analysis, chunking, claims, cited search.
- job_ingestion and anking: job normalization, hard filters, evidence-aware scoring, recommendations.
- application: CV, cover letter, answers, Truth Audit, automation policy.
- browser_agent: local Playwright-assisted form handling and synthetic ATS lab.
- interview, offer, career_growth, analytics: downstream career workflows.
- security: path safety, redaction, and secret scanning.

## AI Strategy

The system works without paid AI APIs. Optional local SentenceTransformers, CrossEncoder, and Ollama adapters improve retrieval/writing where available, but deterministic paths remain usable and auditable.

## Data Model

The database tracks profile data, evidence, documents, projects, claims, jobs, scores, feedback, applications, browser actions, interviews, offers, analytics, backups, and audit logs. Evidence lifecycle rules prevent stale or revoked material from silently supporting future claims.
