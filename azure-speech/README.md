# Azure AI Speech — Demos

These notebooks demonstrate how to use the [Azure AI Speech](https://learn.microsoft.com/azure/ai-services/speech-service/overview) service to convert speech to text and text to speech.

## What is Azure AI Speech?

Azure AI Speech is a managed service offering:

- **Speech to text (STT)** — transcribe audio from a microphone, file, or stream
- **Text to speech (TTS)** — synthesize natural-sounding speech from text
- **Speaker recognition** — identify and verify speakers
- **Speech translation** — translate spoken audio in real time

## Prerequisites

- Python 3.9 or later
- An [Azure Speech](https://portal.azure.com) resource
- VS Code with the [Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
- **For microphone input** (`01_speech_to_text_mic.ipynb`): a working microphone connected to the machine running the notebook

## Setup

### 1. Environment variables

Ensure your `.env` file (copied from `.env.sample` at the repo root) contains:

```
AZURE_SPEECH_KEY=<your-speech-key>
AZURE_SPEECH_REGION=<your-speech-region>
```

You can find these values in the Azure Portal under your Speech resource → **Keys and Endpoint**.

## Samples

| Notebook | Description |
|----------|-------------|
| `01_speech_to_text_mic.ipynb` | Recognize a single utterance from the default microphone |
| `02_speech_to_text_file.ipynb` | Recognize speech from a WAV audio file with detailed timing results |
| `03_text_to_speech.ipynb` | Synthesize text into spoken audio and save it to a WAV file |

## Running the Notebooks

Open any notebook in VS Code, select the **Python (foundry-tools)** kernel, and run cells top to bottom. The first cell in each notebook installs all required packages via `%pip install`.
