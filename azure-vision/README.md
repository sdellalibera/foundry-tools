# Azure AI Vision — Demos

These notebooks demonstrate how to use the [Azure AI Vision](https://learn.microsoft.com/azure/ai-services/computer-vision/overview) service to analyze images and extract text using optical character recognition (OCR).

## What is Azure AI Vision?

Azure AI Vision (Image Analysis 4.0) provides a rich set of AI algorithms for processing images and returning information about their content:

- **Image Analysis** — detect objects, describe scenes, read text, generate captions, and more via a single API call
- **OCR (Read API)** — extract printed and handwritten text from images and documents
- **Smart crops** — generate region-of-interest thumbnails
- **Background removal** — separate foreground subjects from the background

## Prerequisites

- Python 3.9 or later
- An [Azure AI Services](https://portal.azure.com) or dedicated Vision resource
- VS Code with the [Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)

## Setup

### 1. Install dependencies

From the repo root, activate your virtual environment and install:

```bash
pip install -r azure-vision/requirements.txt
```

### 2. Environment variables

Ensure your `.env` file (copied from `.env.sample` at the repo root) contains:

```
AZURE_VISION_ENDPOINT=https://<your-account>.cognitiveservices.azure.com/
AZURE_VISION_KEY=<your-vision-key>
```

You can find these values in the Azure Portal under your Vision / AI Services resource → **Keys and Endpoint**.

## Samples

| Notebook | Description |
|----------|-------------|
| `01_image_analysis.ipynb` | Analyze an image for captions, objects, tags, and people using Image Analysis 4.0 |
| `02_ocr.ipynb` | Extract printed and handwritten text from an image using the Read (OCR) API |

## Running the Notebooks

Open any notebook in VS Code, select the **Python (foundry-tools)** kernel, and run cells top to bottom. The first cell in each notebook installs all required packages via `%pip install`.
