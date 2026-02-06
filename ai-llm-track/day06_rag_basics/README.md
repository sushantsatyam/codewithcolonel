# Day 06 — RAG basics (lightweight)

This notebook introduces a **simple retrieval-augmented generation (RAG)** loop: store a few notes, retrieve the most relevant ones, and inject them into a prompt.

## What this project shows

- A tiny in-memory document store
- A naive keyword-based retriever
- A prompt template that grounds the response in retrieved context

## Folder layout

```
.
├── notebook.ipynb
└── prompts
    └── rag_prompt.txt
```

## How I run it

1. Install dependencies:
   ```bash
   pip install openai
   ```
2. Set `OPENAI_API_KEY` in your environment.
3. Open the notebook and run the cells.
