# self-graph: Roadmap & Architecture

## 🏗️ Architecture (Initial)
- **Next.js** (App Router)
- **Neon (Postgres)**
- JSON-first ingestion

## 📦 Conceptual Data Model
- **Project**: Metadata about the repository.
- **Analysis**: Raw LLM output from tools like `self-commit`.

## ⚠️ Principles
- Store raw LLM output (no early normalization).
- Treat data as an event stream.
- Cost control enforced by architecture (defaulting to cheap models).

## 🚀 Roadmap
- [ ] Ingestion API (`POST /api/analysis`)
- [ ] Raw JSON Storage
- [ ] Project Listing
- [ ] Cross-analysis queries
- [ ] Pattern extraction

## 🧩 Long Term Vision
- Developer identity engine.
- Architecture intelligence tool.
