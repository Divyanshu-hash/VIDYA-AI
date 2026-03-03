# VIDYA-AI 🎓

**ATLAS: Academic Task Learning Agent System** — A multi-agent AI system built with LangGraph that provides personalized academic assistance using coordinated AI agents.

## 🧠 How It Works

VIDYA-AI uses a **multi-agent orchestration** pattern where a Coordinator agent analyzes student requests and delegates work to specialized agents that run in parallel:

```
START → Coordinator → Profile Analyzer → [Planner + NoteWriter + Advisor] → Execute → END
```

## 🤖 Agents

### 🎯 Coordinator Agent
Analyzes the student's request using the **ReACT framework** (Reasoning and Acting) to determine which agents are needed and how they should work together.

### 👤 Profile Analyzer Agent
Extracts and interprets the student's learning preferences, study patterns, and academic history to personalize all outputs.

### 📅 Planner Agent
Creates personalized study schedules by:
- Analyzing calendar events and finding available study blocks
- Prioritizing tasks by urgency, complexity, and energy requirements
- Generating structured study plans with ADHD management strategies, energy optimization, and emergency protocols

### 📚 NoteWriter Agent
Generates concise study notes and revision materials by:
- Analyzing the student's learning style (visual, hands-on, etc.)
- Applying the **80/20 principle** (focus on 20% of content that covers 80% of exam material)
- Producing **Study Notes** with:
  - 📌 Key Concepts & Definitions
  - 📐 Important Formulas & Theorems
  - ⚠️ Common Mistakes to Avoid
  - 🧠 Exam Patterns — types of questions to expect
  - 💡 Quick Revision Summary

### 👩‍🏫 Advisor Agent
Provides personalized academic guidance *(activated by the Coordinator only when guidance is needed, e.g. queries about struggling, stress, or managing workload)*:
- Analyzing the student's current situation and challenges
- Generating actionable advice for time management and stress management
- Creating emergency protocols and backup strategies

## 📁 Project Structure

```
VIDYA-AI/
├── Agent_LangGraph.ipynb   # Main notebook with all agent code
├── profile.json            # Student profile data
├── calendar.json           # Calendar/schedule events
├── task.json               # Academic tasks and deadlines
├── .env                    # API keys (GROQ_API_KEY)
├── requirements.txt        # Python dependencies
└── venv/                   # Virtual environment
```

## 🚀 Setup

1. **Clone the repo**
   ```bash
   git clone https://github.com/Divyanshu-hash/VIDYA-AI.git
   cd VIDYA-AI
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   venv\Scripts\activate      # Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up API key**
   Create a `.env` file:
   ```
   GROQ_API_KEY=your_groq_api_key_here
   ```

5. **Run the notebook**
   Open `Agent_LangGraph.ipynb` in Jupyter/VS Code and run all cells.

## 🛠️ Tech Stack

- **LangGraph** — Multi-agent workflow orchestration
- **LangChain** — LLM integration framework
- **Groq API** — LLM backend (Llama 3.1)
- **Rich** — Beautiful console output
- **Python 3.11**

## 📊 Sample Output

The system produces beautifully formatted output panels:
- **📋 PLANNER** — Structured study schedule with daily focus areas
- **📋 NOTEWRITER** — Detailed study materials with core concepts, emergency tips, and quick reference guides
- **📋 ADVISOR** — Personalized academic guidance with action steps