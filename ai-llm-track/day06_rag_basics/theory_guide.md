# Day 06 — RAG basics (theory guide)

## Goal

Retrieval-augmented generation (RAG) improves reliability by **injecting relevant context** into a model prompt. Instead of hoping the model “remembers” facts, we **retrieve** them from a small knowledge store and use them to ground the answer.

## Core loop

1. **Index data** (notes, docs, or embeddings).
2. **Retrieve** the most relevant items for a user question.
3. **Compose a prompt** that includes retrieved context + the user question.
4. **Generate** a response that is grounded in the context.

## Why RAG works

- **Freshness:** update the knowledge store without retraining.
- **Traceability:** you can show the context used to answer.
- **Quality:** reduces hallucinations by anchoring the response to facts.

## Retrieval in this notebook

We use a lightweight keyword overlap scorer. It is intentionally simple to highlight the flow:

- Tokenize query and documents.
- Count overlapping terms.
- Sort and select the top results.

In production, you would replace this with semantic search (embeddings + vector database).

## Grounding tips

- Keep retrieved snippets **short and focused**.
- Include **sources** (doc titles, URLs) in the context.
- Add **system rules** that forbid the model from inventing facts outside the context.

## Open data notes

The notebook builds retrievable notes from the **Palmer Penguins** dataset. This shows how to turn structured data into natural-language summaries that are ready for retrieval.

## Extension ideas

- Add chunking for long documents.
- Swap keyword scoring for embeddings (e.g., cosine similarity).
- Add evaluation: compare answers with and without retrieval.
