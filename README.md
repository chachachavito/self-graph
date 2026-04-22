

# self-graph

A system for modeling and analyzing developer identity through structured outputs from multiple LLMs.

---

## 🧠 Core Idea

- Each **project** becomes a node
- Each **LLM analysis** becomes structured data
- Over time, patterns emerge

This is not just storage — it's a way to **map technical identity as a graph**.

---

## 🎯 Goal

Turn subjective technical identity into a **queryable, evolving system**.

Instead of:
- opinions
- self-descriptions
- static portfolios

You get:
- structured data
- cross-project insights
- emergent patterns

---

## 🧱 Architecture (initial)

- **Next.js** (App Router)
- **Neon (Postgres)**
- JSON-first ingestion (no normalization)

---

## 📦 Data Model (conceptual)

### Project

```json
{
  "name": "architecture-analyzer",
  "type": "tooling"
}
```

### Analysis

```json
{
  "source": "claude",
  "analysis": { /* raw LLM output */ }
}
```

---

## ⚠️ Principles

- Store **raw LLM output** (no early normalization)
- Treat data as **event stream**, not final schema
- Optimize for **learning over structure** (at first)

---

## 💸 Cost Control (Default Behavior)

All projects using `self-graph` should enforce cost control by default.

### Principles

- Always use the cheapest viable model (`gpt-4.1-mini`) as default
- Never expose model selection directly to end users
- Treat model choice as an internal system decision

### Implementation Pattern

```ts
function getModel(mode: string = "default") {
  switch (mode) {
    case "deep":
      return "gpt-4.1"; // expensive
    default:
      return "gpt-4.1-mini"; // cheap
  }
}
```

### Fallback Strategy

```ts
async function runWithFallback(prompt: string) {
  try {
    return await runModel("gpt-4.1-mini", prompt);
  } catch {
    return await runModel("gpt-4.1", prompt);
  }
}
```

### Goal

> Cost should be controlled by architecture, not by user behavior.

This ensures scalability and prevents accidental overuse of expensive models.
---

## 🚀 Roadmap

- [ ] Ingestion API (`POST /api/analysis`)
- [ ] Store raw JSON
- [ ] Basic project listing
- [ ] Cross-analysis queries
- [ ] Pattern extraction

---

## 🧩 Long Term Vision

self-graph evolves into:

> A system that understands how a developer thinks, builds, and evolves — across projects, time, and contexts.

Potential directions:
- Developer identity engine
- Architecture intelligence tool
- Dataset for meta-analysis of engineering behavior

---

## 👤 Author

Bruno Chaves

---

## 🧪 Status

Early stage — focused on **data capture and structure**.