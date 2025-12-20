# Google AI Intensive – Capstone Project  
## Evaluating an AI Agent Assistant for Data Science Workflows

This repository contains my capstone project for the **Google 5-Day AI Intensive**, focused on evaluating the effectiveness and limitations of an AI agent designed to assist with data science analysis.
The project emphasizes **accuracy, statistical rigor, and failure-mode analysis** when using LLM-based assistants in analytical workflows.  It is not optimized for performance.  
As this is course work it aligns to the course objectives.

---

## Project Focus

- Assessing where AI assistance meaningfully improves data science workflows  
- Identifying common failure modes in AI-assisted analysis, including:
  - hallucinated code generation 
  - improper statistical test selection  
  - inadequate problem framing and analytical planning  
- Comparing AI-assisted workflows against a fully manual baseline  

---

## Techniques Explored

- Gemini API–based LLM orchestration  
- Retrieval-Augmented Generation (RAG)  
- Function calling and compositional tool use  
- Zero-shot prompting for analytical task decomposition  

These techniques were evaluated as *means*, not ends. (they are major topics in the course)

---

## Evaluation Approach

I established a **manual, non-AI baseline notebook**, representing how I would conduct the analysis without AI assistance. This baseline was used to:

- Evaluate when AI output had statistical rigor 
- Identify where human judgment remained essential  
- Surface systematic weaknesses in agent-driven statistical reasoning  

---

## Repository Contents

- `AprilSubmission.ipynb` – Final capstone submission  
- `BasicAnalysisEngine.ipynb` – Proof-of-concept tools used by the agent  
- `ManualStats.ipynb` – Fully manual analysis baseline used for comparison  

---

## Notes on Scope

The manual baseline notebook reflects my direct Python and statistical analysis work. Other notebooks include structured experiments based on course-provided patterns, adapted and evaluated within this project to explore their strengths and limitations.
