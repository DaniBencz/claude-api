# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A personal learning project of Jupyter notebooks working through the Anthropic Python SDK (`anthropic`) and Voyage AI embeddings SDK (`voyageai`), progressing from basic API requests to tool use, RAG, and prompt caching. There is no application code beyond a placeholder `main.py`/`test_main.py` (a trivial `greet()` function, unrelated to the notebooks — likely scaffolding from repo setup).

Notebooks are numbered in learning-progression order, with letter suffixes (`_v1`, `_v2`, ...) marking iterative rewrites of the same topic as concepts are added:

- `001_requests_*.ipynb` — basic `Anthropic` client requests, including a simple chatbot loop
- `002_system_prompt.ipynb` — system prompts
- `003_controlling_output.ipynb`— output formatting
- `004_streaming.ipynb` — streaming
- `005_prompt_evals_v1..v5.ipynb` — iterative build-up of a prompt evaluation harness
- `006_prompting_v1..v2.ipynb` — prompting techniques
- `007_tools_v1..v6.ipynb` — iterative build-up of tool use (function calling)
- `008_tool_streaming.ipynb` — streaming tool calls
- `009_text_editor_tool.ipynb` — the text editor tool
- `010_web_search.ipynb` — the web search tool
- `011_embeddings.ipynb`, `012_semantic_search.ipynb`, `013_bm25.ipynb`, `0014_hybrid.ipynb` — embeddings and retrieval (semantic search, BM25, hybrid search) built on `voyageai`
- `015_thinking.ipynb` — extended thinking
- `016_images.ipynb`, `017_documents.ipynb` — vision and document (PDF) inputs
- `018_caching.ipynb` — prompt caching

Supporting data files read by the notebooks: `dataset.json`, `report.md`, `earth.pdf`, `image.png`, `output.json`, `output.html`.

## Environment setup

- Python virtualenv lives in `.venv` (not currently populated with dependencies — install what a notebook imports as needed: `anthropic`, `voyageai`, `python-dotenv`, `jupyter`, etc.).
- API keys are loaded via `python-dotenv` from a `.env` file (see `.env.example` for required keys: `ANTHROPIC_API_KEY`, `VOYAGE_API_KEY`). Every notebook calls `load_dotenv()` before constructing clients.
- Run notebooks with Jupyter (VS Code notebook interface or `jupyter lab`/`jupyter notebook`). There is no build step.

## Conventions

- Each notebook is self-contained: it re-imports and re-defines helpers rather than importing from other notebooks or a shared module.
- When a topic has multiple `_vN` notebooks, later versions are the "current" iteration — treat earlier `_vN` files as historical/reference, not code to extend.
