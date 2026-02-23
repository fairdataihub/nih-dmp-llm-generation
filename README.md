# Using LLMs to Generate NIH Data Management Plans (DMPs)

## Overview

This repository contains the code associated with the paper:

"Evaluating the Performance of LLMs in Drafting NIH Data Management
Plans."

The objective of this project is to automatically generate NIH-compliant
Data Management Plans (DMPs) using two large language models:

-   Llama 3.3
-   GPT-4.1

The repository includes the DMP generation workflow, evaluation
components, and the outputs produced during the study.

------------------------------------------------------------------------

## Project Standards

The overall structure of the repository follows the FAIR-BioRS
guidelines: https://fair-biors.org/

The Python code in the Jupyter notebook `main.ipynb` adheres to PEP 8
style guidelines: https://peps.python.org/pep-0008/

All required dependencies are listed in the `requirements.txt` file.

------------------------------------------------------------------------

## Getting Started

### Prerequisites

This project includes one primary Jupyter notebook:

    main.ipynb

To run the code, you will need:

-   Python 3.9 or higher
-   Internet access and an OpenAI API key (for GPT-4.1 usage)
-   Ollama installed locally (for running Llama 3.3)

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

Open `main.ipynb` and select the registered kernel (e.g.,
`nih-dmp-llm-env`).

------------------------------------------------------------------------

## Inputs and Outputs

The notebook uses structured input files included in this repository.

Generated NIH Data Management Plans from GPT-4.1 and Llama 3.3 are saved
in the `outputs/` directory:

https://github.com/fairdataihub/nih-dmp-llm-generation/tree/main/outputs

------------------------------------------------------------------------

## License

This project is distributed under the MIT License. See the `LICENSE`
file for full details.

------------------------------------------------------------------------

## Contributions and Feedback

Contributions and feedback are welcome. Please use the GitHub Issues
page to report problems or suggest improvements:

https://github.com/fairdataihub/nih-dmp-llm-generation/issues

You may also fork the repository and submit a pull request.

------------------------------------------------------------------------

## Citation

If you use this code in your research, please follow the citation
instructions provided in the `CITATION.cff` file.
