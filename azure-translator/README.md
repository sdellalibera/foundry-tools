# Azure AI Translator — Demos

These notebooks demonstrate how to use the [Azure AI Translator](https://learn.microsoft.com/azure/ai-services/translator/overview) service to translate text, retrieve supported languages, and transliterate text between scripts.

## What is Azure AI Translator?

Azure AI Translator is a cloud-based neural machine translation service that supports 100+ languages. It offers:

- **Text translation** — translate text across supported languages
- **Language detection** — automatically detect the source language
- **Transliteration** — convert text between scripts (e.g., Arabic → Latin)
- **Supported languages** — query the full list of available languages and scripts

## Prerequisites

- Python 3.9 or later
- An [Azure Translator](https://portal.azure.com) resource (or Azure AI multi-service resource)
- VS Code with the [Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)

## Setup

### 1. Install dependencies

From the repo root, activate your virtual environment and install:

```bash
pip install -r azure-translator/requirements.txt
```

### 2. Environment variables

Ensure your `.env` file (copied from `.env.sample` at the repo root) contains:

```
AZURE_TRANSLATOR_KEY=<your-translator-key>
AZURE_TRANSLATOR_REGION=<your-region>
```

You can find these values in the Azure Portal under your Translator resource → **Keys and Endpoint**.

## Samples

| Notebook | Description |
|----------|-------------|
| `01_get_languages.ipynb` | Retrieve the full list of supported translation and transliteration languages |
| `02_translate_text.ipynb` | Translate text into one or more target languages with auto language detection |
| `03_transliterate_text.ipynb` | Convert text from one script to another (e.g., Chinese Simplified → Latin) |

## Running the Notebooks

Open any notebook in VS Code, select the **Python (foundry-tools)** kernel, and run cells top to bottom. The first cell in each notebook installs all required packages via `%pip install`.
