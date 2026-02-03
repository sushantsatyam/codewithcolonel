# Day 01 — Prompting styles + simple agent execution (Python + OpenAI)

I’m starting my AI/LLM track with a small notebook that shows **prompting styles** and **agent execution patterns**. I kept this lightweight so I can build on it later.

## What this project shows

- **Prompting styles**: zero-shot, few-shot, and role prompting.
- **Execution patterns**: sequential calls vs. parallel calls.
- **Same question, different prompts**: I compare outputs side-by-side.

## Folder layout

```
.
├── notebook.ipynb
├── prompts/
│   ├── zero_shot.txt
│   ├── few_shot.txt
│   └── role_prompt.txt
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

- I’m focusing on clarity over complexity right now.
- I’ll add tools, memory, and multi-agent patterns in later days.
- If I tweak prompts, I store them in `prompts/` so I can reuse them.
