# ⚡ Decision Debt Tracker
### Corporate Decision Intelligence Platform — Built for the Enterprise

> *"We track the decisions companies forget they made."*

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-Hugging_Face-orange?style=for-the-badge)](https://huggingface.co/spaces/swastikraj/decision-debt-tracker)
[![Colab](https://img.shields.io/badge/📓_Notebook-Google_Colab-yellow?style=for-the-badge)](https://colab.research.google.com/drive/1q9TlICdD6L1Kw41dTvyY4bpxNi-7d5ay)
[![Hackathon](https://img.shields.io/badge/🏆_Build_%26_Beyond-VIT_Vellore-blue?style=for-the-badge)](https://vitcc.edu.in)

---

## 🧠 The Problem

Every MNC makes hundreds of decisions daily — in boardrooms, emails, Slack threads, and meeting notes. These decisions are:

- **Never formally recorded** with rationale or assumptions
- **Never cross-checked** against previous decisions
- **Silently contradictory** — one team freezes hiring while another approves headcount expansion
- **Never audited** for outcome vs. original intent

This invisible accumulation of untracked, conflicting, and forgotten decisions is called **Decision Debt** — and it costs enterprises millions in wasted execution, repeated arguments, and failed strategies.

> McKinsey estimates poor decision-making costs organizations **$1.3M+ annually**. Bain & Company found **37% of executive time** is spent revisiting decisions already made.

---

## 💡 The Solution

**Decision Debt Tracker** is the world's first AI-powered platform that:

1. **Extracts** structured decision objects from any unstructured text (emails, transcripts, meeting notes)
2. **Stores** decisions in a semantic vector database for intelligent retrieval
3. **Detects** contradictions and dependencies against all historical decisions
4. **Scores** accumulated organizational risk as a **Decision Debt Score (0–100)**
5. **Visualizes** the entire decision network as an interactive graph

---

## 🏗️ Architecture

```
Input (Text / Transcript)
        ↓
[Module 1] Decision Extractor — Llama 3.3 70B via Groq
        ↓
Structured Decision Object
{decision, rationale, owner, assumptions, deadline, domain, keywords}
        ↓
[Module 2] Embedding + ChromaDB Storage — all-MiniLM-L6-v2
        ↓
[Module 3] Contradiction & Dependency Detector — Semantic Search + LLM
        ↓
[Module 4] Decision Debt Scorer — Rule-based + LLM Hybrid (0–100)
        ↓
[Module 5] Decision Graph Builder — Plotly Interactive Network
        ↓
[Module 6] Gradio UI — Deployed on Hugging Face Spaces
```

---

## ⚙️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **LLM** | Llama 3.3 70B via Groq API |
| **Embeddings** | `sentence-transformers/all-MiniLM-L6-v2` |
| **Vector Store** | ChromaDB |
| **Contradiction Detection** | Cosine Similarity + LLM Reasoning |
| **Graph Visualization** | Plotly |
| **UI Framework** | Gradio |
| **Deployment** | Hugging Face Spaces |
| **Development** | Google Colab |

---

## 🚀 Features

- 📝 **Natural Language Input** — paste any corporate text, meeting transcript, or email
- 🤖 **AI Decision Extraction** — automatically identifies decision, rationale, owner, deadline, domain, and assumptions
- ⚠️ **Real-Time Conflict Detection** — flags Direct Contradictions, Dependencies, and Redundancies against all stored decisions
- 📊 **Decision Debt Score** — quantifies organizational risk on a 0–100 scale with contributing factors
- 🕸️ **Interactive Decision Graph** — live network visualization with color-coded domains and conflict edges
- 💡 **Quick Examples** — pre-loaded corporate scenarios for instant demo

---

## 🖥️ Local Setup

```bash
# Clone the repository
git clone https://github.com/swastikraj/decision-debt-tracker.git
cd decision-debt-tracker

# Install dependencies
pip install gradio requests chromadb sentence-transformers plotly

# Set your Groq API key
export GROQ_API_KEY="your_groq_api_key_here"

# Run
python app.py
```

Get a free Groq API key at [console.groq.com](https://console.groq.com)

---

## 📁 Project Structure

```
decision-debt-tracker/
│
├── app.py                  # Main application (all 6 modules)
├── requirements.txt        # Python dependencies
└── README.md               # This file
```

---

## 🎯 How It Works — Demo

**Input:**
```
The board has decided to expand into Southeast Asia by Q3 2025,
hiring 200 new staff. CEO owns this. Deadline: June 30th.
```

**Output:**
```json
{
  "decision": "Expand into Southeast Asia by Q3 2025",
  "rationale": "Growth into new markets",
  "owner": "CEO",
  "deadline": "June 30th",
  "domain": "Strategy",
  "keywords": ["expansion", "hiring", "Southeast Asia"]
}
```

**Conflict Detected:**
```
🔴 [High] Direct Contradiction
   Against: Freeze all external hiring for Q3 2025
   Reason: Expansion requires 200 new hires which directly
           contradicts the active hiring freeze.

📊 Decision Debt Score: 80/100 — 🔴 Critical
```

---

## 🏆 Hackathon

**Event:** Build & Beyond — Hackathon + Designathon
**Organized by:** The Whitehats Club, VIT Vellore
**Duration:** 36 Hours
**Mode:** Hybrid (Online + Offline)

---

## 👤 Author

**Swastik Raj**
Registration No: 22BCE0411
Computer Science & Engineering — SCOPE
Vellore Institute of Technology
Team: HackyNTechGuy

---

## 📄 License

MIT License — feel free to use, modify, and build on this.

---

<p align="center">Built in 36 hours. Solo. Live on Hugging Face Spaces.</p>
<p align="center"><i>"Every organization is drowning in decisions. We built the life raft."</i></p>
