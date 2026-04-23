# 🎭 Sentiment Analysis

A Streamlit web app that performs sentence-level sentiment analysis using any OpenAI-compatible LLM API.

## Features

- Analyzes each sentence in the submitted text individually
- Color-coded results: **positive** ✅, **negative** ❌, **neutral** ➖
- Summary metrics (counts per sentiment + total)
- Results cached per input — repeated submissions don't hit the API
- Works with any OpenAI-compatible endpoint (OpenAI, Azure, local models, etc.)

## Requirements

- Python ≥ 3.12
- An OpenAI-compatible API (key, base URL, and model name)

## Installation

```bash
pip install -e .
```

Or with [uv](https://github.com/astral-sh/uv):

```bash
uv sync
```

## Configuration

Set the following environment variables before running:

| Variable          | Description                                      |
|-------------------|--------------------------------------------------|
| `OPENAI_API_KEY`  | Your API key                                     |
| `OPENAI_BASE_URL` | Base URL of the OpenAI-compatible API endpoint   |
| `OPENAI_MODEL`    | Model name to use (e.g. `gpt-4o`, `llama3`, …)  |

Example:

```bash
export OPENAI_API_KEY=sk-...
export OPENAI_BASE_URL=https://api.openai.com/v1
export OPENAI_MODEL=gpt-4o
```

## Usage

```bash
streamlit run app.py
```

Then open the URL printed in the terminal (usually `http://localhost:8501`).

1. Paste or type any text into the input box.
2. Click **🔍 Analyze Sentiment**.
3. Each sentence is displayed with a color-coded sentiment badge and a summary is shown below.
