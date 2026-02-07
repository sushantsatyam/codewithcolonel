# Day 06 — RAG basics (lightweight)

This notebook introduces a **simple retrieval-augmented generation (RAG)** loop: store a few notes, retrieve the most relevant ones, and inject them into a prompt.

## What this project shows

- A tiny in-memory document store
- A naive keyword-based retriever
- A prompt template that grounds the response in retrieved context
- Loading open data (Palmer Penguins) to create retrievable notes

## Folder layout

```
.
├── data
│   └── penguins.csv
├── notebook.ipynb
├── theory_guide.md
└── prompts
    └── rag_prompt.txt
```

## How I run it

1. Install dependencies:
   ```bash
   pip install openai pandas
   ```
2. Set `OPENAI_API_KEY` in your environment.
3. Review the theory guide in `theory_guide.md`.
4. Open the notebook and run the cells.

## Data source

The notebook uses the **Palmer Penguins** dataset (open data) sourced from the seaborn-data repository.
