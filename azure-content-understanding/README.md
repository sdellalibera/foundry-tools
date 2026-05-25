# Azure AI Content Understanding — Demos

These notebooks demonstrate how to use [Azure AI Content Understanding](https://learn.microsoft.com/azure/ai-services/content-understanding/overview) to build intelligent content analyzers that can extract structured information from documents, images, audio, and video.

## What is Azure AI Content Understanding?

Azure AI Content Understanding is a managed service that lets you define *analyzers* — reusable AI pipelines that extract fields you specify from a variety of content types. Once an analyzer is created you can submit content to it and receive structured JSON results.

## Prerequisites

- Python 3.9 or later
- An [Azure AI Services](https://portal.azure.com) resource (Content Understanding is part of the multi-service resource or a dedicated endpoint)
- VS Code with the [Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)

## Setup

### 1. Install dependencies

From the repo root, activate your virtual environment and install:

```bash
pip install -r azure-content-understanding/requirements.txt
```

### 2. Environment variables

Ensure your `.env` file (copied from `.env.sample` at the repo root) contains:

```
AZURE_CONTENT_UNDERSTANDING_ENDPOINT=https://<your-account>.cognitiveservices.azure.com/
```

Authentication uses `DefaultAzureCredential`. Run `az login` once before opening the notebooks.

## Samples

| Notebook | Description |
|----------|-------------|
| `01_create_analyzer.ipynb` | Define and create a custom content analyzer |
| `02_analyze_document.ipynb` | Submit a document URL to an analyzer and inspect the extracted fields |

## Running the Notebooks

Open any notebook in VS Code, select the **Python (foundry-tools)** kernel, and run cells top to bottom. The first cell in each notebook installs all required packages via `%pip install`.
