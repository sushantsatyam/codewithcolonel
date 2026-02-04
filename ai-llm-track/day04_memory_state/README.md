# Day 04 — Memory + state (lightweight)

This notebook introduces a **lightweight memory** pattern: capture user preferences in a short notes list and inject them into the next prompt.

## What this project shows

- Keeping a compact memory store for user preferences
- Rendering prompts with memory context
- Updating memory after each interaction

## Folder layout

```
.
├── notebook.ipynb
└── prompts
    └── memory.txt
```

## How I run it

1. Install dependencies:
   ```bash
   pip install openai
   ```
2. Set `OPENAI_API_KEY` in your environment.
3. Open the notebook and run the cells.
