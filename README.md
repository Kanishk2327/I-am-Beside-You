# AI Agent Internship Project: Academic RAG Agent

* **Name:** Kanishk Dhariwal
* **University:** IIT Kanpur
* **Department:** Chemical Engineering

## Project Overview

[cite_start]This project fulfills the internship assignment by building an AI agent to automate a daily university task: finding information in course notes. [cite: 3]

[cite_start]The agent uses a Retrieval-Augmented Generation (RAG) architecture to answer questions based *only* on a user's personal PDF documents (e.g., lecture slides, textbooks). [cite: 13]

## Core Features (Assignment Deliverables)

1.  [cite_start]**Automated Task:** Automates the manual task of searching through multiple, complex PDFs for specific formulas, definitions, and concepts. [cite: 3]
2.  [cite_start]**Fine-Tuned Model:** The agent's **Generator** component is the fine-tuning target. [cite: 4]
    * [cite_start]**Rationale:** The goal is **task specialization** and **improved reliability**. [cite: 9] A generic model is fine-tuned to become an "Expert Tutor" that answers questions in an academic style, bases its answers *only* on the provided documents, and reliably cites its sources.
    * **Dataset:** A sample fine-tuning dataset (`tutor_finetuning_data.jsonl`) is included, built from the user-provided PDFs. [cite_start]The notebook simulates this fine-tuned model using a detailed system prompt. [cite: 23]
3.  [cite_start]**Evaluation Metrics:** The agent's quality is measured using an **LLM-as-a-Judge** methodology. [cite: 10]
    * **Metrics:** An evaluator LLM provides quantitative scores (1-5) for **Groundedness** (is the answer based on context?) and **Helpfulness** (does it answer the question?).
    * [cite_start]The notebook runs a test suite and calculates the average scores for the final report. [cite: 24]

## Optional Features (Bonus Points)

* [cite_start]**RAG:** The agent uses an external integration (RAG) pipeline. [cite: 13]
* [cite_start]**Multi-Agent:** The system is structured as a multi-agent system (Retriever, Generator, Evaluator). [cite: 12]
* [cite_start]**UI:** The final notebook cell provides a simple, command-line "chat" interface (CLI). [cite: 15]

## How to Run

1.  **Clone the Repository:** Download or clone all files to your local machine.
2.  **Add PDFs:** Place your 14 PDF documents (the ones listed in `Cell 7` of the notebook) in the same directory as the notebook.
3.  **Install Dependencies:** Open the `.ipynb` file in Jupyter Notebook and run **Cell 3** (the `!pip install...` cell) to install all required libraries.
4.  **Set API Key:**
    * Go to **Cell 5**.
    * Get a Google AI Studio API key and paste it into the `YOUR_API_KEY_HERE` string.
5.  **Run All Cells:**
    * From the menu, select "Cell" -> "Run All".
    * **Cell 9** will create and save a local vector database (`my_course_notes_db`).
    * **Cell 16** will run the full evaluation.
    * **Cell 18** will launch the live demo chat.

## Deliverables in this Repository

1.  [cite_start]**Source Code:** `[Your_Notebook_Name].ipynb` [cite: 20]
2.  [cite_start]**AI Agent Architecture:** `ARCHITECTURE.pdf` [cite: 21]
3.  [cite_start]**Data Science Report:** `DATA_SCIENCE_REPORT.pdf` (which includes evaluation outcomes). [cite: 22, 24]
4.  [cite_start]**Fine-Tuning Data:** `tutor_finetuning_data.jsonl` [cite: 23]
5.  [cite_start]**Interaction Logs:** `INTERACTION_LOGS.txt` (The chat history with Gemini used to build this project). [cite: 25]
6.  [cite_start]**README:** `README.md` (This file). [cite: 30]
