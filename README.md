[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/30poBfe_)
# Project Name
Dr. Cusack - Scheduling Advisor

## Team

- Alem Kemal
- Eleanor Koh
- Katie Mozak

## Description

Dr Cusack - Scheduling Advisor is for students who are getting ready for course registration and want advice on what courses they should take at Hope College. It has course descriptions and course major requirements from the following departments: Computer Science, Engineering, Math, Physics, Chemistry, Nursing, Biology, Environmental Studies, Psychology, and Neuroscience, and can answer specific questions about these departments' courses at Hope College use RAG retrieval. It uses web scraping to get information from the web about the course requirements for majors that are part of the departments that the app supports. For courses outside these departments, it will use its own knowledge to provide descriptions about what these classes are usually like. Furthermore, it links the courses to real life applications, and can tell students how each course may come in useful in their future. In addition, it has access to a course scheduling tool, where students can ask it to generate a schedule for classes they want to take, and it outputs a maximum of 5 unique schedules for the student to choose from.

## First-Time Setup

### 1) Create + activate a venv

**macOS / Linux**
```bash
python3.13 -m venv .venv
source .venv/bin/activate
```

**Windows (PowerShell)**
```powershell
py -3.13 -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 2) Install deps

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
pip install -e .
```

### 3) Configure Gemini

1. Copy `.env.example` to `.env`
2. Set `GEMINI_API_KEY=...` (from [Google AI Studio](https://aistudio.google.com/apikey))
3. Set `USE_GEMINI=1` to enable LLM to use its own knowledge for real world applications for the courses

Never commit `.env`.

## How to Run

This app can be run on both the CLI and Streamlit. However, we recommend running it on Streamlit for a better experience.

To launch the app on Streamlit, execute:

```bash
streamlit run app.py
```

To run it in the CLI:

```bash
# Interactive multi-turn chat
python -m ai_in_loop.cli chat
