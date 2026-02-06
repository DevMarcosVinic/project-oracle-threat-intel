# Project Oracle: Automated Threat Intelligence & OSINT Pipeline 🕵️‍♂️🤖

> An automated system that monitors global feeds, analyzes geopolitical/tech risks using Generative AI, and delivers actionable intelligence via Telegram.

![Status](https://img.shields.io/badge/Status-Active-success)
![Security](https://img.shields.io/badge/Focus-Blue_Team_%2F_OSINT-blue)

## 🎯 Objective
To solve the "information overload" problem in Cybersecurity and Tech markets by creating an autonomous agent that:
1.  **Ingests** data from multiple OSINT sources (RSS, APIs).
2.  **Processes** information to filter noise and bypass simple WAFs.
3.  **Analyzes** causality and second-order effects using **Google Gemini 2.5 Flash**.
4.  **Alerts** the user with categorized, actionable intelligence (Hardware, Crypto, Geopolitics).

## 🛠️ Architecture & Tech Stack

* **Orchestration:** [n8n](https://n8n.io/) (Self-hosted/Cloud)
* **AI Engine:** Google Gemini 2.5 Flash (via API)
* **Notifications:** Telegram Bot API
* **Logic:** JavaScript (ES6) for data aggregation and payload splitting.

### The Workflow
1.  **Data Collection:** Connects to high-signal RSS feeds (Reuters, CISA, TrendForce).
2.  **Aggregation:** JavaScript node de-duplicates and cleans input data.
3.  **AI Analysis:** A custom system prompt instructs the LLM to act as a "Risk Strategist", categorizing threats by probability and impact.
4.  **Distribution:** Splits large payloads (over 4096 chars) and delivers to a private Telegram channel.

## 🚀 How to Run

### Prerequisites
* An instance of n8n.
* Google AI Studio API Key.
* Telegram Bot Token.

### Installation
1.  Download the `oraculo_workflow.json` file from this repository.
2.  Open n8n -> **Workflows** -> **Import from File**.
3.  Configure your Credentials in the Gemini and Telegram nodes.
4.  Activate the workflow.

## 🛡️ Security & Privacy
* **No Credentials in Code:** All API keys are managed via n8n's credential vault. This repository contains only the logic structure.
* **Data Minimization:** The bot processes public data (OSINT) and does not store user PII.

## 📝 License
This project is licensed under the MIT License.

---
*Created by Marcos Vinicius - Cybersecurity Analyst & Automation Enthusiast*
