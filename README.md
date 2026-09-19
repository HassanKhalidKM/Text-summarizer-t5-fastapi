# Text Summarizer App

A FastAPI-based web application that summarizes long text using a fine-tuned T5 model. The app provides a simple UI where users can paste dialogue or text and receive a concise summary.

## Features

- Summarize input text with a pretrained T5 model
- Simple web interface powered by FastAPI and Jinja2 templates
- REST API endpoint for summarization
- Supports local inference using the saved model in the project folder

## Project Structure

- app.py - FastAPI app, model loading, summarization logic, and API routes
- index.html - Frontend page for the summary UI
- saved_summary_model/ - Local T5 model and tokenizer files

## Tech Stack

- Python
- FastAPI
- Pydantic
- Transformers
- PyTorch
- Jinja2
- Uvicorn

## Setup

1. Create and activate a Python environment (optional but recommended)
2. Install the required dependencies:

```bash
pip install fastapi uvicorn transformers torch pydantic sentencepiece
```

3. Run the app:

```bash
uvicorn app:app --reload --host 0.0.0.0 --port 8000
```

4. Open your browser at:

```text
http://127.0.0.1:8000
```

## API Usage

### Summarize endpoint

Endpoint:

```text
POST /summarize/
```

Example request body:

```json
{
  "dialogue": "Your long text or dialogue goes here"
}
```

Example response:

```json
{
  "summary": "A short summary of the input"
}
```

## Notes

- The app loads the model from the local folder named saved_summary_model.
- If you want a lighter setup for CPU-only inference, make sure your PyTorch installation matches your system environment.

## Suggested GitHub Repository Name

```text
text-summarizer-t5-fastapi
```

## Suggested GitHub Repository Description

```text
A FastAPI web app for summarizing text using a T5-based transformer model with a simple browser UI.
```
