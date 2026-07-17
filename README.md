# claude-api

Notebooks for learning the Anthropic (Claude) Python SDK, from basic requests through tool use, RAG, and prompt caching.

## Prerequisites

- Python 3.10+
- Jupyter support in your editor (e.g. the VS Code Jupyter extension - ms-toolsai.jupyter)
- An [Anthropic API key](https://console.anthropic.com/) and, for the embeddings notebooks, a [Voyage AI API key](https://dash.voyageai.com/)

## Setup

```bash
python -m venv .venv
.venv\Scripts\activate       # Windows
pip install anthropic voyageai python-dotenv jupyter
```

Copy `.env.example` to `.env` and fill in your keys:

```
ANTHROPIC_API_KEY="your key"
VOYAGE_API_KEY="your key"
```

## Usage

Open any notebook and run the cells in order. Notebooks are numbered by topic progression; where multiple `_vN` versions exist, the highest version is the current iteration.
