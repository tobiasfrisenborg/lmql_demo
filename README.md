# LMQL Demo
Tobias Frisenborg Christensen, AI/ML Engineer - tfc@systematic.com  

The examples folder holds a few Jupyter notebooks with various examples.
* `examples/openai.ipynb`: minimal example of using LMQL with OpenAI models.
* `examples/local.ipynb`: minimal example of using local models (HuggingFace) with LMQL.
* `examples/features.ipynb`: python demonstration of most of the features of LMQL.

## Setup
### Requirements
* python >= 3.11.5
* For local models: GPU with a good amount of VRAM (i.e. RTX 3090)
* For OpenAI models: valid API credentials (see guide below)

### VS Code Extension
It is recommended to install the VS Code extension enables syntax highlighting for LMQL queries. The extension can be found here: [LMQL VS Code Extension](https://marketplace.visualstudio.com/items?itemName=lmql-team.lmql)

### Python environment
1. Create a new python virutal environment:
    ```
    python -m venv .lmql_demo_venv
    ```
2. Activate the environment:

    Linux:
    ```
    source .lmql_demo_venv/bin/activate
    ```  
    Windows:
    ```
    .lmql_demo_venv/bin/Activate.ps1
    ```
2. Install requirements:
    ```
    pip install -r requirements.txt
    ```

### OpenAI API
1. Create a file in the project root named `.env`
2. Go to the [OpenAI API](https://platform.openai.com/api-keys) and create a new API key
3. Insert your API key in the `.env` file as such:
    ```
    OPENAI_API_KEY="{your_api_key}"
    ```
4. You can now load your API key in python using the following code:
    ```
    import os
    import openai
    from dotenv import load_dotenv

    load_dotenv()
    openai.api_key = os.environ['OPENAI_API_KEY']
    ```
