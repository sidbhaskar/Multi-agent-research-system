# Multi-Agent AI Research System 🤖🔍

A complete, open-source Multi-Agent AI Research System built from scratch utilizing LangChain, Large Language Models (LLMs), and a professional Streamlit UI. This project demonstrates how to architect and orchestrate multiple AI agents to perform complex, multi-step research tasks autonomously.

## 🌟 Overview: Agents vs. Simple Chains

Unlike simple LLM chains that follow a rigid, linear prompt-response path, this system implements **Agentic AI**. Agents are equipped with tools and decision-making capabilities, allowing them to dynamically search the web, scrape specific pages, evaluate their own findings, and pass state to one another. This modular approach results in highly accurate, well-researched, and critically reviewed outputs.

## ✨ Core Features & Pipeline

This repository provides a clean, real-world structure for agentic projects, featuring a robust multi-agent pipeline:

* **Search Agent:** Retrieves live, reliable data from the web, acting as the system's dynamic information gatherer.
* **Reader Agent:** Takes target URLs provided by the Search Agent to scrape and extract deep, contextually relevant content.
* **Writer Chain:** Synthesizes the extracted raw data to generate highly structured, detailed research reports.
* **Critic Chain:** Acts as an automated reviewer. It evaluates the Writer's output, scores the content for accuracy and relevance, and ensures high-quality results.
* **Shared Pipeline State:** Efficiently manages the flow of data, ensuring context and state are seamlessly passed between agents throughout the research lifecycle.
* **Streamlit Interface:** A clean, professional UI for users to input research topics, monitor the live pipeline, and read the final reports.

## 🏗️ Architecture Flow

1. **Query Input:** The user submits a research topic via the Streamlit frontend.
2. **Information Retrieval:** The Search Agent finds relevant, up-to-date sources.
3. **Deep Extraction:** The Reader Agent scrapes the identified URLs for granular data.
4. **Drafting:** The Writer Chain compiles the data into a comprehensive report.
5. **Review & Refinement:** The Critic Chain scores the draft, prompting revisions if the output falls below quality thresholds.
6. **Final Output:** The polished report is delivered to the UI.

## 📂 Project Structure

The codebase is organized into a clean, flat structure to demonstrate how real-world agentic AI pipelines are built and managed:

```text
Multi-agent-research-system/
├── .gitignore             # Specifies intentionally untracked files to ignore
├── agents.py              # Core logic for Search, Reader, Writer, and Critic agents
├── app.py                 # Streamlit UI entry point
├── pipeline.py            # State management and multi-agent orchestration
├── requirements.txt       # Project dependencies
└── tools.py               # Custom tools for agents (e.g., live search, URL scraping)

