# Day 05 — Evaluation + guardrails

This notebook introduces a **lightweight evaluation loop**: draft a response, score it with a rubric, and use the score to decide whether to revise.

## What this project shows

- A reusable rubric prompt for grading responses
- A basic evaluation call that returns JSON scores
- A simple decision point for revisions

## Folder layout

```
.
├── notebook.ipynb
└── prompts
    └── eval_rubric.txt
```

## How I run it

1. Install dependencies:
   ```bash
   pip install openai
   ```
2. Set `OPENAI_API_KEY` in your environment.
3. Open the notebook and run the cells.
