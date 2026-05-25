# Azure AI Foundry Tools — Demos

Code samples for working with **Azure AI Foundry** tools using Python and Jupyter notebooks. Each service folder is self-contained and includes its own setup instructions and numbered notebooks.

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

### 1. Create a virtual environment

From the repo root:

**Bash (macOS/Linux):**

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r <service-folder>/requirements.txt
python -m ipykernel install --user --name foundry-tools-py --display-name "Python (foundry-tools)"
```

**PowerShell (Windows):**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r <service-folder>\requirements.txt
python -m ipykernel install --user --name foundry-tools-py --display-name "Python (foundry-tools)"
```

> If you get an execution-policy error on Windows, run this once first:
> `Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned`

### 2. Configure environment variables

Copy the sample env file and fill in your values:

```bash
cp .env.sample .env
# then edit .env with your endpoint and key details
```

Each notebook calls `load_dotenv(find_dotenv())` in its setup cell, which locates and loads `.env` from the repo root automatically.

### 3. Select the kernel in VS Code

Open any notebook, click the kernel picker in the top-right, and choose **Python (foundry-tools)**. If you skipped the `ipykernel install` step, pick **Python Environments → .venv** instead.

## Authentication

Notebooks that use `DefaultAzureCredential` pick up your active `az login` session automatically (no API key required). Notebooks for services that only support key-based auth (Translator, Speech, Vision, Language) read their keys from the `.env` file.

## Service Samples

- [Azure Content Understanding →](azure-content-understanding/README.md)
- [Azure Translator →](azure-translator/README.md)
- [Azure Speech →](azure-speech/README.md)
- [Azure Vision →](azure-vision/README.md)
- [Azure Language →](azure-language/README.md)
