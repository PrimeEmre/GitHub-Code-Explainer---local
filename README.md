# 🛠️ GitHub Code Explainer

<div align="center">

![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-3.0-000000?style=for-the-badge&logo=flask&logoColor=white)
![CrewAI](https://img.shields.io/badge/CrewAI-Agentic_Automation-FF4B4B?style=for-the-badge)
![GitHub API](https://img.shields.io/badge/GitHub_API-V3-181717?style=for-the-badge&logo=github)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**An autonomous developer relations agent that monitors your GitHub commits and transforms raw code changes into professional, human-readable technical blog posts.**

[🚀 Live Demo](#) • [📖 Documentation](#installation) • [🐛 Report Bug](https://github.com/PrimeEmre/GitHub-Code-Explainer---local/issues) • [✨ Request Feature](https://github.com/PrimeEmre/GitHub-Code-Explainer---local/issues)

</div>

---

## 📌 What is GitHub Code Explainer?

**GitHub Code Explainer** is an agentic automation tool designed to bridge the gap between "coding" and "documenting." For many developers, keeping a technical blog (DevLog) updated is a chore that takes time away from actual building. This project solves that by deploying a specialized crew of AI agents that act as your personal technical writer. 

When you push code to a repository, this tool fetches the specific "diff" (what changed) and the commit message. It then hands that data to a **Technical Code Analyst** (Agent 1) who breaks down the logic of the changes. Finally, a **DevLog Writer** (Agent 2) takes that analysis and crafts a narrative-driven blog post for your blog. It explains not just *what* changed, but *why* it matters to the project.

By utilizing **CrewAI's** sequential workflow, the tool ensures that the technical details are accurate before the creative writing begins. This prevents "hallucinations" and produces high-quality content that sounds like it was written by the lead developer.

---

## ✨ Features

- 🔄 **GitHub Commit Integration** — Automatically pulls latest commit diffs and messages via REST API.
- 🤖 **Multi-Agent Pipeline** — Separate agents for technical analysis and creative writing.
- 📊 **Agentic Logic** — High-fidelity explanations of code logic (not just file names).
- 📝 **Markdown Native** — Outputs are perfectly formatted for WordPress, Ghost, or static site generators.
- 🎨 **Professional UI** — Dark-themed dashboard with glassmorphism and real-time execution tracking.
- 🔐 **Private & Secure** — Uses Personal Access Tokens (PAT) and `.env` for secure repository access.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Backend** | Python, Flask |
| **Frontend** | HTML5, CSS3 (Glassmorphism), JavaScript |
| **AI Orchestration** | CrewAI Enterprise / Cloud |
| **LLM Models** | GPT-4o-mini (via CrewAI) |
| **Data Sourcing** | GitHub REST API v3 |
| **Environment** | python-dotenv |

---

## 🏗️ Project Structure

```text
github-code-explainer/
│
├── static/
│   ├── style.css          # Professional "Midnight & Gold" UI
│   └── script.js          # AJAX calls and Agent Stepper logic
│
├── templates/
│   └── index.html         # Main Automation Dashboard
│
├── github_fetcher.py      # Logic for connecting to GitHub REST API
├── app.py                 # Flask server & CrewAI Kickoff logic
├── requirements.txt       # Project dependencies
├── .env                   # Secret Keys (GITHUB_TOKEN, CREWAI_TOKEN)
└── README.md
