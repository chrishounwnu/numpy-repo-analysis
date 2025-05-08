# PhD Coding Exercise – Code Churn Analysis on NumPy Repository

This project explores the evolution of code churn (lines of code added and removed) over time in the [NumPy](https://github.com/numpy/numpy) GitHub repository, in response to RQ3:  
**"How does code churn (lines added/removed) fluctuate over time?"**

Data was collected using GitPython and analyzed in a Jupyter Notebook. Visualizations and aggregated data are included in this repository.

---

## Reflection Questions

### 1. What difficulties or errors did you face while completing this task?

Several technical challenges were encountered:

- Initially, I attempted to use `PyDriller`, but multiple import errors and conflicts with its `__init__.py` structure forced me to switch to `GitPython`, which proved more stable.
- Working with a large repository like NumPy (over 38,000 commits) introduced performance delays, particularly in full commit-level extraction.
- Heatmap visualizations were originally implemented with `seaborn`, but dependency issues in the environment led me to recreate the plot entirely with `matplotlib`.
- Optimization/ Complexity time

These challenges were addressed step by step with appropriate tools and clear testing strategies.

---

### 2. Share the full conversation with ChatGPT or any other AI tools that you used to help you.

I used ChatGPT to help structure the analysis, debug PyDriller issues, and suggest clear data visualizations.

A full PDF export of the session is included in this repository:  
📄 [`chatgpt_transcript.pdf`](./chatgpt_transcript.pdf)

---

### 3. Choose one of your plots: What do you find surprising, confusing, or ambiguous about it? What might explain this?

I chose the line plot showing monthly insertions and deletions (Plot 1).

What surprised me was the extreme volatility visible throughout the entire timeline — with large spikes in both insertions and deletions, especially in recent years. 
While I expected some variation due to new features and bug fixes, the amplitude and frequency of these spikes suggest major codebase overhauls or big refactorings.

These fluctuations could be explained by:
- Major version releases or large pull requests being merged
- The use of automated tools generating/removing code
- Legacy cleanups and transitions (e.g., moving to Python 3, or modularization)

Despite the noise, it reveals important patterns about the development lifecycle of NumPy and shows clear bursts of high activity.

---

### 4. What would be one interesting follow-up question or analysis to pursue based on your findings?

An interesting follow-up would be to:

> **"Identify which contributors or file types are responsible for the largest churn spikes."**

This could help determine if churn is centralized (by a few developers or parts of the codebase), and whether certain subsystems (e.g., testing, C extensions, documentation) dominate structural changes.

Such analysis could be valuable for understanding maintainability, technical debt, or even training future AI models to assist with code evolution.

---

## Deliverables

- Visualizations: see `plots/`
- Data files: see `data/`
- Code & analysis: `src/notebook.ipynb`
- AI transcript: `chatgpt_transcript.pdf`

---

