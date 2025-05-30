# DeAItor – AIHumanizerBot

**DeAItor – AIHumanizerBot** is an automation pipeline designed to transform AI-generated content into fully human-like text using a multi-step, retry-until-pass process. It leverages web automation to interface with **HumanizeAI.pro** (for rewriting), **ZeroGPT** (for AI detection), and **QuillBot** (for human-likeness validation).

This tool is ideal for researchers, writers, educators, and developers seeking to eliminate AI traces from content for ethical rewriting, personalization, and compliance with anti-AI policies.

---

## Mission

The goal of **DeAItor** is to empower ethical content enhancement and AI-human hybrid authorship by:
- Helping users polish AI-generated text to sound more natural
- Reducing or eliminating AI detection rates (ZeroGPT, GPTZero)
- Increasing human-likeness confidence scores (QuillBot, Turnitin AI checks)
- Saving time through automation without compromising quality

---

## Purpose

In a world where content is increasingly flagged as AI-generated, even after rewriting, manually submitting to tools like HumanizeAI.pro, ZeroGPT, and QuillBot becomes tedious. **DeAItor automates this process** and guarantees high-quality, undetectable, and natural-sounding output with zero AI footprints.

---

## Features

| Feature                             | Description                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------|
| 🔁 Automated Humanizer Loop         | Iteratively rewrites content using HumanizeAI.pro until it passes detection |
| 🧠 ZeroGPT Integration              | Extracts AI detection scores (0–100%) automatically                         |
| ✍️ QuillBot Checker (In Progress)   | Assesses if rewritten text scores as “100% human-written”                  |
| 📉 Turnitin-Ready Output            | Produces content that can bypass advanced AI and plagiarism checkers        |
| 📝 Text Logging + History           | Saves all intermediate results and final clean version                      |
| ⏱️ Fast Output (<2 min)             | Designed for speed using browser automation                                 |
| 📦 Modular Codebase                 | Easy to extend (e.g., for Copyleaks, GPTZero, Grammarly)                    |

---

## Technology Stack

- **Language**: Python 3.8+
- **Web Automation**: Playwright (preferred over Selenium for modern JS-heavy pages)
- **Detection Tools**: HumanizeAI.pro (UI-based), ZeroGPT (UI/score scraper), QuillBot (planned)
- **Data Handling**: JSON & TXT export
- **Optional Extensions**: Streamlit / Flask for GUI

---

## Workflow

```mermaid
graph TD;
    A[AI-Generated Input Text] --> B[HumanizeAI.pro Rewriter]
    B --> C[ZeroGPT Score Checker]
    C --> D[QuillBot Human Score Validator]
    D --> E{ZeroGPT = 0% & QuillBot = 100%?}
    E -- No --> B
    E -- Yes --> F[Final Humanized Output Saved]


