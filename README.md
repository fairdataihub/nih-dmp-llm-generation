# Using LLMs to Generate NIH Data Management Plans (DMPs)

## Overview

This repository contains the code associated with the paper: "Evaluating the Performance of LLMs in Drafting NIH Data Management
Plans." The objective of this project is to automatically generate NIH-compliant using two large language models: Llama 3.3 & GPT-4.1
The repository includes the DMP generation workflow and the outputs produced during the study.

------------------------------------------------------------------------

## Project Standards

## Standards followed
The overall codebase is organized in alignment with the **[FAIR-BioRS guidelines](https://fair-biors.org/)**. All Python code follows **[PEP 8](https://peps.python.org/pep-0008/)** conventions, including consistent formatting, inline comments, and docstrings. Project dependencies are fully captured in **[requirements.txt](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/Requirements.txt)**. We also retain **[dmp-template](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/inputs/dmp-template.md)** as inside the prompt template used by the DMP generation workflow.

------------------------------------------------------------------------

## Getting Started

### Prerequisites

This project includes one primary Jupyter notebook **[main](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/main.ipynb)**.
------------------------------------------------------------------------

## Installation

### 1. Clone the Repository

Open a terminal (Anaconda Prompt on Windows or system terminal on
macOS/Linux) and run:

    git clone https://github.com/fairdataihub/nih-dmp-llm-generation.git

Navigate into the project directory:

    cd nih-dmp-llm-generation

------------------------------------------------------------------------

### 2. Create and Activate a Virtual Environment

Create a virtual environment:

    python -m venv venv

Activate it:

Windows: venv`\Scripts`{=tex}`\activate`{=tex}

macOS / Linux: source venv/bin/activate

------------------------------------------------------------------------

### 3. Install Dependencies

    pip install -r requirements.txt

------------------------------------------------------------------------

### 4. Register a Jupyter Kernel

    python -m ipykernel install --user --name=nih-dmp-llm-env

------------------------------------------------------------------------

### 5. Deactivate When Finished

    deactivate

------------------------------------------------------------------------

## LLM Configuration

### Llama 3.3 (via Ollama)

1.  Install Ollama from: https://ollama.com/

2.  Pull the Llama 3.3 model:

    ollama pull llama3.3

3.  Ensure Ollama is running before executing the notebook.

------------------------------------------------------------------------

### GPT-4.1 (OpenAI API)

Set your OpenAI API key as an environment variable.

Windows: setx OPENAI_API_KEY "your_api_key_here"

macOS / Linux: export OPENAI_API_KEY="your_api_key_here"

------------------------------------------------------------------------

## Running the Notebook

Start JupyterLab:

    jupyter lab

Open `main.ipynb` and select the registered kernel (e.g.,`nih-dmp-llm-env`).

------------------------------------------------------------------------

## Inputs and Outputs

The notebook uses structured input files which is included **[dmp-template](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/inputs/dmp-template.md)** and **[inputs](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/inputs/inputs.xlsx)** in this repository. Generated NIH Data Management Plans from GPT-4.1 and Llama 3.3 are saved in the `outputs/` directory: https://github.com/fairdataihub/nih-dmp-llm-generation/tree/main/outputs

------------------------------------------------------------------------

## License
This work is licensed under the **[MIT License](https://opensource.org/license/mit/)**. See **[LICENSE](https://github.com/fairdataihub/nih-dmp-llm-generation/blob/main/LICENSE)** for more information.


---

## Feedback and contribution
Use **[GitHub Issues](https://github.com/fairdataihub/nih-dmp-llm-generation/issues)** to submit feedback, report problems, or suggest improvements.  
You can also **fork** the repository and submit a **Pull Request** with your changes.

---

## How to cite
If you use this code, please cite this repository using the **versioned DOI on Zenodo** for the specific release you used (instructions will be added once the Zenodo record is available). For now, you can reference the repository here: **[fairdataihub/nih-dmp-llm-generation](https://github.com/fairdataihub/nih-dmp-llm-generation)**.