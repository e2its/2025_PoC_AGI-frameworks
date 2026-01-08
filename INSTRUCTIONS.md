# Instructions for 2025_PoC_AGI-frameworks

## Overview
This document provides setup, usage, and contribution instructions for the 2025_PoC_AGI-frameworks project. The project contains proof-of-concept implementations and research for multi-agent AGI frameworks, focusing on orchestration, workflow management, and agent collaboration using CrewAI, Strands, and AGNO frameworks.

---

## 1. Setup

### 1.1. Clone the Repository
```
git clone <repository-url>
cd 2025_PoC_AGI-frameworks
```

### 1.2. Python Environment
- It is recommended to use a virtual environment:
```
python3 -m venv .venv
source .venv/bin/activate
```

### 1.3. Install Dependencies
It is recommended to use [uv](https://github.com/astral-sh/uv) for all dependency management:

### 1.4. Create a `.env` File

Some experiments or frameworks may require environment variables (such as API keys or configuration settings). To set these up:

1. Create a `.env` file in the project root:
	```
	cp .env.example .env
	```
	Or, if `.env.example` does not exist, create a new `.env` file manually:
	```
	touch .env
	```

2. Edit the `.env` file and add the required variables:
	```
AWS_REGION=<<XXXXXXXX>>                                               # North Viginia
AWS_ACCESS_KEY_ID=<<YYYYYYYYYYYYYYYYYY>>                              # Required for AWS authentication
AWS_SECRET_ACCESS_KEY=<<ZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZ>>     # Required for AWS authentication
AWS_IAM=<<IAM_ROLE>>
	```

3. Save the file. Your environment variables will be loaded automatically by most frameworks (using `python-dotenv` or similar).

> **Note:** Never commit your `.env` file to version control. It may contain sensitive information.

#### Install uv (if not already installed):
```
pip install uv
```

#### For requirements.txt-based projects:
- To install all dependencies:
```
uv pip install -r requirements.txt
```
- To add a new dependency and update requirements.txt:
```
uv add <package-name>
```
- To sync your environment with requirements.txt:
```
uv pip sync
```

#### For pyproject.toml-based projects (recommended for modern Python projects):
- To add a new dependency:
```
uv add <package-name>
```
- To install all dependencies:
```
uv pip install .
```
- To update all dependencies:
```
uv pip upgrade
```

> **Tip:** Prefer using `pyproject.toml` for new projects. Use `uv add <package>` to manage dependencies, and commit the updated `pyproject.toml` and `uv.lock` files.

---

## 2. Directory Structure
- See the README.md for a detailed directory structure and description of each folder and file.

---

## 3. Usage

### 3.1. Notebooks
- The main experiments are implemented as Jupyter notebooks (e.g., `crew-agent-sequential.ipynb`, `agno-agent-workflow.ipynb`).
- Open notebooks with Jupyter Lab or VS Code and run cells sequentially.

### 3.2. Configuration
- Each framework (CrewAI, Strands, AGNO) has its own configuration files under their respective `config/` directories.
- Edit YAML files to customize agents, tasks, and integration settings.

---

## 4. Adding New Experiments
1. Create a new notebook in the project root or appropriate subfolder.
2. Use a clear and descriptive name (e.g., `agno-agent-collaborate.ipynb`).
3. Update the README.md to document your experiment and findings.
4. Add or update configuration files as needed.

---

## 5. Best Practices
- Use virtual environments to avoid dependency conflicts.
- Document all new experiments and configuration changes.
- Keep code and configuration modular and organized.
- Test new workflows before committing.

---

## 6. Troubleshooting
- If you encounter issues with dependencies, ensure your virtual environment is activated and up to date.
- For configuration errors, validate your YAML files and check for required fields.
- Review the README.md troubleshooting section for common issues and solutions.

---


