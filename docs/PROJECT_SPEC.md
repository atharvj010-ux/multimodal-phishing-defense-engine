# Multi-Modal Phishing & Impersonation Defense Engine

## Purpose

A defensive cybersecurity platform that analyzes URLs, email/text,
domains, screenshots, and webpage characteristics to identify
phishing and impersonation attempts.

## Core objective

The system must combine multiple detection signals and produce:

1. Risk score
2. Risk level
3. Individual modality predictions
4. Explainable evidence
5. Analysis history

## Primary modalities

1. URL
2. Email/Text
3. Domain
4. Screenshot/Webpage
5. Brand/Impersonation

## Architecture

Frontend:
Next.js + TypeScript

Backend:
FastAPI + Python

Database:
PostgreSQL

ORM:
SQLAlchemy

Migrations:
Alembic

ML:
scikit-learn initially

Deep Learning:
PyTorch/Transformers later

Computer Vision:
OpenCV + OCR

Containerization:
Docker Compose

## Core entities

User
Analysis
URLArtifact
EmailArtifact
DomainAnalysis
VisualAnalysis
ModelPrediction
RiskEvidence

## Core workflow

Input
→ Artifact creation
→ Individual analyzers
→ Model predictions
→ Risk fusion
→ Evidence generation
→ Final assessment
→ Database persistence
→ Dashboard

## Important design principles

- Modular analyzers
- Explainable results
- No hard-coded secrets
- No business logic inside API routes
- Every analysis must be persisted
- Every model prediction must record its model/version
- Every final risk assessment must have evidence
- ML models must be replaceable without changing the API
- All security analysis must remain defensive