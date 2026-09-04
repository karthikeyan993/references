# 📚 References & Knowledge Hub

A curated repository to store, organize, and share reference links, technical notes, workshop handouts, talk slides, and architecture patterns.

---

## 📂 Repository Structure

```text
references/
├── README.md                      # Master index & quick reference catalog
├── TEMPLATE.md                    # Template for adding new reference notes
├── agents/                        # AI Agents, Multi-Agent Frameworks & Harnesses
│   ├── README.md                  # Category index
│   └── hermes-agent.md            # Hermes Team Harness reference & notes
└── talks/                         # Tech Talks, Workshops & Presentations
    ├── README.md                  # Category index
    └── google-adk-talk.md         # Google ADK Launch Kit workshop notes
```

---

## ⚡ Master Reference Catalog

| Name / Topic | Category | Tags | Direct Link | Notes / Summary |
| :--- | :--- | :--- | :--- | :--- |
| **Hermes Team Harness** | `agents` | `ai-agents`, `hermes`, `copilot`, `gcp`, `harness` | [Artifact Link](https://claude.ai/code/artifact/a6875e0e-a178-4998-98e2-36d612860edd) | [agents/hermes-agent.md](./agents/hermes-agent.md) |
| **Google ADK Launch Kit** | `talks` | `google-adk`, `gemini`, `agents`, `workshop` | [Artifact Link](https://claude.ai/code/artifact/3ad65c98-a580-4a50-87e8-19aa95d89bb1) | [talks/google-adk-talk.md](./talks/google-adk-talk.md) |

---

## 🏷️ Categories

### 🤖 [AI Agents & Harnesses](./agents/)
References related to agent systems, team harnesses, runtime environments, evaluation frameworks, and LLM integrations.
- **[Hermes Team Harness](./agents/hermes-agent.md)** — Guide on running Hermes Agent on developer Copilot seats with GCP-hosted shared infrastructure.

### 🎤 [Talks, Workshops & Presentations](./talks/)
Slides, workshop handouts, live demos, and notes from tech talks and conferences.
- **[Google ADK Launch Kit](./talks/google-adk-talk.md)** — Hands-on workshop handout taking you from an empty directory to a deployed Google ADK agent.

---

## ➕ How to Add a New Reference

1. **Pick or create a category folder** (e.g., `agents/`, `talks/`, `tools/`, `system-design/`).
2. **Copy the template**:
   ```bash
   cp TEMPLATE.md <category>/<your-topic-slug>.md
   ```
3. **Fill in the details** (direct URL, summary, key highlights, tags).
4. **Update the tables** in:
   - `<category>/README.md`
   - Master Catalog table in root [`README.md`](./README.md)
