# Azure AI Language — Demos

These notebooks demonstrate how to use [Azure AI Language](https://learn.microsoft.com/azure/ai-services/language-service/overview) to analyze text with pre-built natural language processing (NLP) models.

## What is Azure AI Language?

Azure AI Language is a cloud-based service that provides NLP capabilities for building intelligent applications. Key features include:

- **Sentiment Analysis** — determine the sentiment (positive, neutral, negative) of text and individual sentences
- **Key Phrase Extraction** — identify the main talking points in text
- **Named Entity Recognition (NER)** — identify and categorize entities such as people, places, organizations, and dates
- **Language Detection** — identify the language in which text is written
- **PII Detection** — identify and redact personally identifiable information

## Prerequisites

- Python 3.9 or later
- An [Azure AI Language](https://portal.azure.com) resource (or Azure AI multi-service resource)
- VS Code with the [Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)

## Setup

### 1. Install dependencies

From the repo root, activate your virtual environment and install:

```bash
pip install -r azure-language/requirements.txt
```

### 2. Environment variables

Ensure your `.env` file (copied from `.env.sample` at the repo root) contains:

```
AZURE_LANGUAGE_ENDPOINT=https://<your-account>.cognitiveservices.azure.com/
AZURE_LANGUAGE_KEY=<your-language-key>
```

You can find these values in the Azure Portal under your Language resource → **Keys and Endpoint**.

## Samples

| Notebook | Description |
|----------|-------------|
| `01_sentiment_analysis.ipynb` | Analyze sentiment and opinion at the document and sentence level |
| `02_key_phrase_extraction.ipynb` | Extract the main topics and concepts from text |
| `03_named_entity_recognition.ipynb` | Identify and categorize entities (people, places, organizations, dates, etc.) |

## Running the Notebooks

Open any notebook in VS Code, select the **Python (foundry-tools)** kernel, and run cells top to bottom. The first cell in each notebook installs all required packages via `%pip install`.
