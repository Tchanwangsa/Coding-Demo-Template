# Data Cleaning Agent: Workshop Template

A hands-on workshop template where participants will build a Jupyter-based agent that leverages LangChain and OpenAI to perform data cleaning tasks. This template provides the foundation - we'll write the code together during the workshop!

## What We'll Build

During this workshop, you'll learn to create an AI-powered data cleaning agent that can:
- Generate python (pandas) code to clean datasets
- Handle missing values intelligently
- Create automated data summaries
- Route user queries to appropriate cleaning functions

## Prerequisites

- Anaconda or Miniconda installed
- Git (to clone this repo)
- An OpenAI API key set in your environment (`OPENAI_API_KEY`)

## Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/Tchanwangsa/Data-Cleaning-Agent_Workshop-Version.git
cd Data-Cleaning-Agent_Workshop-Version
```

### Step 2: Create Conda Environment

**Use Anaconda Prompt (Windows) or Terminal (macOS/Linux):**

```bash
# Create and activate environment
conda create -n data-cleaning-agent python=3.11 -y
conda activate data-cleaning-agent

# Install Jupyter and kernel support
conda install jupyter ipykernel -y
python -m ipykernel install --user --name data-cleaning-agent --display-name "Data Cleaning Agent"
```

**macOS/Linux:** If you get "conda: command not found", run `conda init` and restart your terminal.

### Step 3: Configure API Key

Copy the `.env.example` file or run:

**- Windows:** `copy .env.example .env`  
**- macOS/Linux:** `cp .env.example .env`

Edit the `.env` file and add your OpenAI API key:

```
OPENAI_API_KEY=your_actual_api_key_here
```

### Step 4: Launch Environment

**Jupyter Notebook:**

```bash
jupyter notebook
```

**VS Code:**

```bash
code .
```

**Important:** Select the "Data Cleaning Agent" kernel when opening notebooks. (This is the environment we created in step 2)

### Step 5: Install Dependencies

Open `main.ipynb` and run the first cell:

```python
# Install necessary packages
%pip install langchain openai pandas numpy matplotlib seaborn python-dotenv import-ipynb
```

## Workshop Structure

During the workshop, we'll work through:
2. **Setup & Introduction** - Getting familiar with the tools we'll be working with
3. **LLM Integration** - Connecting to OpenAI for code generation
4. **Feature Development** - Building specific cleaning modules
5. **Building Helper Functions** - Creating data analysis helpers
6. **Query Routing** - Creating an intelligent dispatcher
7. **Testing & Deployment** - Putting it all together

## Additional Resources

- Setup LLM call tracing with [LangSmith](https://smith.langchain.com)
- Check available models and costs on [OpenAI Pricing](https://platform.openai.com/docs/pricing)