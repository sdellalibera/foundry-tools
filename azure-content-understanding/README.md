# Azure AI Content Understanding — Demos

These notebooks demonstrate how to use [Azure AI Content Understanding](https://learn.microsoft.com/azure/ai-services/content-understanding/overview) to build intelligent content analyzers that can extract structured information from documents, images, audio, and video.

## What is Azure AI Content Understanding?

Azure AI Content Understanding is a managed service that lets you define *analyzers* — reusable AI pipelines that extract fields you specify from a variety of content types. Once an analyzer is created you can submit content to it and receive structured JSON results.

## Prerequisites

- Python 3.9 or later
- An [Azure AI Services](https://portal.azure.com) resource (Content Understanding is part of the multi-service resource or a dedicated endpoint)
- A Microsoft Foundry resource linked to Content Understanding. In Content Understanding Studio, use the prompt to either create the Foundry resource from the wizard or link an existing Foundry deployment before running the notebooks.
- VS Code with the [Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)

## Setup

### 1. Environment variables

Ensure your `.env` file (copied from `.env.sample` at the repo root) contains:

```
AZURE_CONTENT_UNDERSTANDING_ENDPOINT=https://<your-account>.cognitiveservices.azure.com/
```

Authentication uses `DefaultAzureCredential`. Run `az login` once before opening the notebooks.

### 2. Link Content Understanding to Foundry

Before these samples will work, open Content Understanding Studio and make sure the Content Understanding resource is connected to Microsoft Foundry. If prompted, either:

- create the Foundry resource from the Studio wizard, or
- link an existing Foundry deployment/resource that you created ahead of time.

If this linkage is missing, analyzer creation and analysis calls will not succeed even if your endpoint and authentication are configured correctly.

## Samples

| Notebook | Description |
|----------|-------------|
| `01_create_analyzer.ipynb` | Define and create a custom content analyzer |
| `02_analyze_document.ipynb` | Submit a document URL to an analyzer and inspect the extracted fields |

## Running the Notebooks

Open any notebook in VS Code, select the Python interpreter from `.venv`, and run cells top to bottom. The first cell in each notebook installs all required packages via `%pip install`.
