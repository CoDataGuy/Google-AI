# Google AI Intensive – Capstone Project  
## Evaluating an AI Agent Assistant for Data Science Workflows

### Executive Summary
The core contribution is a comparative evaluation framework that benchmarks AI-assisted methodology against a fully manual, non-AI baseline. The inability of the agent to correctly the tools (functions) available to it, generate accurate SQL and impropper planning of analytical methdology and indicate the agent fails as an automated assistant.

These failures are likely partly due to the methods taught in the class - tools without reference schema and prompting method which did not specify evaluative steps or similarly grounding in statistical methods.

### Introduction
This repository contains my capstone project for the **Google 5-Day AI Intensive**, focused on evaluating the effectiveness and limitations of an AI agent designed to assist with data science analysis.
The project emphasizes **methodology, statistical rigor, and failure-mode analysis** when using LLM-based assistants in analytical workflows.  It is not optimized for performance.  
As this is course work it aligns to the course objectives.

---

## Project Focus
LLMs are increasingly positioned as autonomous or semi-autonomous analytical agents, yet to be useful they must be trusted. 

- Assessing if AI assistance meaningfully improves data science workflows  
- Identifying common failure modes in AI-assisted analysis, including:
  - hallucinated code generation 
  - improper statistical test selection  
  - inadequate problem framing and analytical planning  
- Comparing AI-assisted workflows against a fully manual baseline  

---

## Techniques Explored

- Gemini API–based LLM orchestration  
- Function calling and compositional tool use  
- Zero-shot prompting for analytical task decomposition  

These techniques were evaluated as *means*, not ends. (they are major topics in the course)

---

## Evaluation Approach
This project treats AI-assisted analysis as a system under test, not a black box deliberatly exposing failure modes.

**Primary evaluation dimensions:**

- Statistical, methodology, correctness and test selection  
- Susceptibility to hallucinated code or results  
- Analytical planning and problem framing  
- Utility with minimal prompting or constraints and without grounding  

Rather than optimizing prompts to achieve desired outputs, the evaluation intentionally allows failure modes to emerge in order to characterize risk and limitations.

I established a **manual, non-AI baseline notebook**, representing how I would conduct the analysis without AI assistance. This baseline was used to:

- Evaluate when AI output had statistical rigor
- Identify where human judgment remained essential  
- Surface systematic weaknesses in agent-driven statistical reasoning  

# Methodology Overview

### 1. Manual Baseline Construction

A fully manual Python notebook was created to represent how the analysis would be conducted **without AI assistance**, using:

- NumPy
- SciPy
- Matplotlib
- Seaborn

This baseline establishes:
- Ground-truth analytical reasoning
- Appropriate statistical test selection
- Expected intermediate artifacts (plots, summaries, checks)

### 2. AI-Assisted Workflow

An LLM-based agent (Gemini 1.7) was evaluated using:
- Gemini API integration
- Tool and function calling
- Structured task decomposition
- Zero-shot analytical prompts


AI outputs were assessed **relative to the manual baseline**, not in isolation.

### 3. Comparative Evaluation

Outputs were compared across:
- Correctness of statistical reasoning
- Appropriateness of chosen methods
- Presence of hallucinated or invalid steps
- Degree of human intervention required

---

## Key Findings

- Porperly crafted LLM assistance can accelerate exploratory analysis, particularly for boilerplate code and visualization scaffolding.

- The agent demonstrated **systematic weaknesses in statistical reasoning**, including improper test selection and incomplete analytical framing.
- Several failure modes produced outputs that appeared plausible but were analytically invalid, underscoring the risk of over-trusting fluent responses.
- Explicit constraints and baseline comparisons materially improved interpretability and trustworthiness.

These findings may suggest: **LLM agents are best evaluated as components within constrained workflows**, not as autonomous analysts.

---

## What This Project Demonstrates
The approach generalizes beyond this specific model or task and is applicable to evaluating AI systems in production analytical environments.

**Real World Implications**
As the steps of statistical analysis are well understood, I would implement a routing workflow to analyze a finite set of data.  

**Evaluation Skills**
- Designing manual baselines for comparison
- Identifying and categorizing analytical failure modes
- Distinguishing surface-level correctness from substantive validity

**Technical Skills**
- Python-based statistical analysis
- Tool-augmented LLM workflows
- Reproducible notebook-based experimentation

**AI Systems Understanding**
- Strengths and limits of generative AI in analytical contexts
- Risks of hallucination in high-trust domains
- Importance of human-in-the-loop evaluation

---

## Repository Structure

- `AprilSubmission.ipynb`  
  Final capstone submission integrating AI-assisted workflows and evaluation results

- `BasicAnalysisEngine.ipynb`  
  Proof-of-concept tools and functions used by the AI agent

- `ManualStats.ipynb`  
  Fully manual, non-AI baseline used for comparative evaluation

---

## Next Steps
To migrate the project to Anthropic LLM to see how it performs as is  
Address tool selection failure by adding schemas   

Use Claude Code to accelerate development 









---

## Limitations and Scope

- This project is exploratory rather than predictive
- Results are specific to the evaluated model and task framing
- The goal is not to exhaustively benchmark LLMs, but to demonstrate **evaluation methodology**

---

## Open Questions / Areas for Extension

*(Intentionally left partially open to invite discussion)*

- How should statistical rigor be operationalized for automated agents?
- What minimum constraints are required to prevent high-confidence analytical errors?
- How might this evaluation framework scale to multi-agent or long-horizon workflows?
- What quantitative metrics could complement the qualitative failure-mode analysis?
