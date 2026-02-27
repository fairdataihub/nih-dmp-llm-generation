# Code: Using LLMs to Generate NIH Data Management Plans (DMPs)

## Overview

This repository contains the code associated with the paper: "Evaluating the Performance of LLMs in Drafting NIH Data Management Plans." The objective of this project is to automatically generate NIH-compliant using two large language models: Llama 3.3 & GPT-4.1. The repository includes the DMP generation workflow and the outputs produced during the study. 

In the associated paper, DMP generation was conducted over 10 independent runs to ensure robustness. Due to storage constraints, this repository provides the outputs from a single representative run.

------------------------------------------------------------------------
## Standards followed
The overall codebase is organized in alignment with the **[FAIR-BioRS guidelines](https://fair-biors.org/)**. All Python code follows **[PEP 8](https://peps.python.org/pep-0008/)** conventions, including consistent formatting, inline comments, and docstrings. Project dependencies are fully captured in **[requirements.txt](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/Requirements.txt)**. We also retain **[dmp-template](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/inputs/dmp-template.md)** as inside the prompt template used by the DMP generation workflow.

------------------------------------------------------------------------

## Getting Started
### Step 1 — Clone the repository
```bash
git clone https://github.com/fairdataihub/nih-dmp-llm-generation.git
cd dmpchef
code .
```
### Step 2 — Create and activate a virtual environment

**Windows (cmd):**
```bash
python -m venv venv
venv\Scripts\activate.bat
```
**macOS/Linux:**
```bash
python -m venv venv
source venv/bin/activate
```
### Step 3 — Install dependencies
```bash
pip install -r requirements.txt
```
---
### Step 4 — Configure Large Language Models
**Llama 3.3 (via Ollama)**

1.  Install Ollama from:\
    https://ollama.com/

2.  Pull the Llama 3.3 model:

``` bash
ollama pull llama3.3
```

3.  Ensure that the Ollama service is running before executing the
    notebook or pipeline.

**GPT-4.1 (OpenAI API)**

Set your OpenAI API key as an environment variable.

**Windows (cmd):**

``` bash
setx OPENAI_API_KEY "your_api_key_here"
```

**macOS/Linux:**

``` bash
export OPENAI_API_KEY="your_api_key_here"
```

After setting the environment variable, restart your terminal session to ensure the key is available to Python.

### step 5- Running the Notebook
Use **[`main.ipynb`](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/main.ipynb)**.

------------------------------------------------------------------------

## Inputs and Outputs

The notebook uses structured input files which is included **[dmp-template](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/inputs/dmp-template.md)** and **[inputs](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/inputs/inputs.xlsx)** in this repository. Generated NIH Data Management Plans from GPT-4.1 and Llama 3.3 are saved in the `outputs/` directory: https://github.com/fairdataihub/nih-dmp-llm-generation/tree/main/outputs

------------------------------------------------------------------------

## License
This work is licensed under the **[MIT License](https://opensource.org/license/mit/)**. See **[LICENSE](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/LICENSE)** for more information.

------------------------------------------------------------------------

## Feedback and contribution
Use **[GitHub Issues](https://github.com/fairdataihub/nih-dmp-llm-generation/issues)** to submit feedback, report problems, or suggest improvements.  
You can also **fork** the repository and submit a **Pull Request** with your changes.

------------------------------------------------------------------------

## How to cite
If you use this code, please cite this repository using the **versioned DOI on Zenodo** for the specific release you used (instructions will be added once the Zenodo record is available). For now, you can reference the repository here: **[fairdataihub/nih-dmp-llm-generation](https://github.com/fairdataihub/nih-dmp-llm-generation)**.
