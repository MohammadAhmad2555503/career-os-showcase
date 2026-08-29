# Case Study: Career OS

## Problem

Most career tooling optimises for volume: more saved jobs, more generated cover letters, more outbound applications. That creates a quality and trust problem. A strong career system should know which claims are true, which evidence supports them, which jobs fit hard constraints, and where a human must review before action.

## Solution

Career OS is a local-first personal career operating system. It combines profile intelligence, project evidence, job ranking, application generation, interview preparation, offer analysis, and career-growth tracking under a single evidence model.

## What I Built

- A modular Python product core with SQLite, explicit migrations, services, repositories, and CLI/API workflows.
- Career Brain for CV ingestion, skills, preferences, goals, writing style, and evidence verification.
- Project Brain for static code/folder/ZIP ingestion, secret filtering, chunking, cited search, dependency detection, and claim lineage.
- Job intelligence for structured import, normalization, deduplication, hard filters, scoring, ranking, and feedback learning.
- Application Studio for CV, cover letter, and application-answer generation with Truth Audit checks.
- Browser-assisted apply workflows with explicit stop points, CAPTCHA/unknown-field handling, private-network blocking, and dual-gated Autopilot.
- Interview, offer, analytics, backup, restore, export, and growth-readiness modules.

## Engineering Judgement

Career OS avoids the trap of treating AI confidence as truth. It separates repository content from personal contribution, supports deterministic fallbacks when optional local AI models are unavailable, and keeps all consequential automation conservative by default.

## Evidence

- 95 tests across 21 modules passed in bounded verification.
- Fresh end-to-end flow passed through Career Brain, Project Brain, ranking, documents, Truth Audit, Assisted Apply, synthetic Autopilot, interview, offer, growth, export, backup, and restore.
- 100,000-job scale gate passed with top-50 deep-ranked recommendations.
- Critical focused coverage: Hard Filters 95%, Truth Audit 98%, Autopilot Policy 97%.
- Backup validation and restore passed across 47 tables.

## Employer Signal

This project demonstrates product thinking, privacy-first design, applied AI judgement, test discipline, local automation safety, backend architecture, and the ability to build a system that handles messy real-world workflows rather than only polished demos.
