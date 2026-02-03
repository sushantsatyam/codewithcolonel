# Day 02 — Prompt chaining (planner → executor → critic)

Today I’m building a small **prompt-chaining** notebook. The idea is simple: a planner breaks a request into steps, an executor handles each step, and a critic reviews the final output.

## What this project shows

- **Prompt chaining**: planner → executor → critic.
- **Sequential flow**: the outputs of one prompt feed the next.
- **Parallel option**: run multiple executor steps concurrently and merge results.

## Folder layout

```
.
├── notebook.ipynb
├── prompts/
│   ├── planner.txt
│   ├── executor.txt
│   └── critic.txt
└── outputs/
```

## How I run it

1. Install dependencies:
   ```bash
   pip install openai python-dotenv
   ```
2. Add an API key to `.env` (or export it in your shell):
   ```bash
   export OPENAI_API_KEY="your_key_here"
   ```
3. Open the notebook and run the cells.

## Notes (written by me)

- I’m keeping the prompts short so I can iterate quickly.
- The critic is optional, but it helps me catch vague steps.
- I’ll extend this with tools and memory later.
