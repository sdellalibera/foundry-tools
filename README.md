# Microsoft Foundry Tools — Demos

Code samples for working with **Microsoft Foundry** tools using Python and Jupyter notebooks. Each service folder is self-contained and includes its own setup instructions and numbered notebooks.

| Folder | Service |
|--------|---------|
| [`azure-content-understanding/`](azure-content-understanding/README.md) | Azure AI Content Understanding |
| [`azure-translator/`](azure-translator/README.md) | Azure AI Translator |
| [`azure-speech/`](azure-speech/README.md) | Azure AI Speech |
| [`azure-vision/`](azure-vision/README.md) | Azure AI Vision |
| [`azure-language/`](azure-language/README.md) | Azure AI Language |

## Prerequisites

- Python 3.9 or later
- [Azure CLI](https://learn.microsoft.com/cli/azure/install-azure-cli) installed and signed in (`az login`) — required when using `DefaultAzureCredential`
- VS Code with the [Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) (or any other Jupyter-compatible environment)
- An active Azure subscription with the relevant services provisioned

## Quick Start

Set up once at the repo root — a single virtual environment and Jupyter kernel will work for **every** notebook in every service folder.

### 1. Create a virtual environment and install dependencies

**PowerShell (Windows):**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

**Bash (macOS/Linux):**

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

> If you get an execution-policy error on Windows, run this once first:
> `Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned`

The `ipykernel install` step registers a kernel named **Python (foundry-tools)** that points at the `.venv` you just created. Every notebook in this repo is already configured to use that kernel name, so they will work in VS Code, JupyterLab, classic Jupyter Notebook, or any other Jupyter-compatible environment without further setup.

### 2. Configure environment variables

Copy the sample env file and fill in your values:

```bash
cp .env.sample .env
# then edit .env with your endpoint and key details
```

Each notebook calls `load_dotenv(find_dotenv())` in its setup cell, which locates and loads `.env` from the repo root automatically.

### 3. Select the kernel

Open any notebook, click the kernel picker (top-right in VS Code, top-right in JupyterLab) and choose **Python (foundry-tools)**.

## Authentication

Only the **Content Understanding** notebooks use `DefaultAzureCredential` (picks up your active `az login` session — no API key required). All other services (Translator, Speech, Vision, Language) authenticate with the `AZURE_AI_KEY` from your `.env` file.

## Service Samples

- [Azure Content Understanding →](azure-content-understanding/README.md)
- [Azure Translator →](azure-translator/README.md)
- [Azure Speech →](azure-speech/README.md)
- [Azure Vision →](azure-vision/README.md)
- [Azure Language →](azure-language/README.md)
