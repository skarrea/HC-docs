# Good Practice

## Overview

### Purpose

Describe the good practices users preferred to follow on the Hunt Cloud environment.

### Scope

This guide covers good practice recommendations for programming, structuring, data handling.

### Audience

All users.

## Data Usage

- Sensitive data **MUST** be uploaded and kept only on the cloud.

- Sensitive data **MUST NOT** be downloaded from the cloud.

  > [NOTE] If deemed necessary to download sensitive data, you MUST have a written permission to do so from the Lab or Space leader.

- Avoid copying none-sensitive data to personal machines, USB drives, or external cloud services. _Except if deemed necessary (e.g., for publication)_.

- If data was downloaded, delete it as soon as you don't need it locally anymore.

- Raw data should be located under its dedicated folder under `/mnt/archive`.

- Don't save processed data under `/mnt/archive`, but save it under your project folder.

- Don't make multiple copies of raw data.

- Have a code to process the data automatically depending on the raw data, if possible.

- Don't keep multiple copies of the processed data.

## Collaborative Projects

- If you are collaborating with others on the same project, consider locating the project folder under `/mnt/work/projects`.

## Data Structuring and Project Organization

- Create a `ReadMe` file, describing the name and objectives of the project, the name of those who work on it, and the timeline (start date, estimated end date).

- Use a clear and predictable structure with clear folder names, such as:

  ```text
  project-name/
  ├─ docs/           # Documentation, protocols, README files
  ├─ config/         # Config files (YAML/JSON) and environment files
  ├─ data/
  │   ├─ raw/        # Original, read-only input data
  │   ├─ interim/    # Intermediate processed data
  │   └─ processed/  # Final analysis-ready datasets
  ├─ notebooks/      # Jupyter/R notebooks
  ├─ src/            # Source code (modules, scripts)
  ├─ results/        # Figures, tables, model outputs
  └─ logs/           # Logs and run metadata
  ```

## Workbench Usage

- Prefer using the **provided workbench solutions** (e.g., JupyterLab, RStudio, VS Code, or similar managed environments) instead of local tools.

## Programming

### Processing

- Keep all code execution, data access, and processing **inside the cloud environment** to maintain security and compliance.

- If Nodes were used to process data, transfer output.

- Make a conda environment for each project and delete it when you are done with it.

- When you run tasks that include multi-processing, make sure to not use all the computing cores. **Preserve at least 30% of the cores** for others.

### Version Control and Reproducibility

- Use **Git** for version control of scripts and notebooks.

  - Create meaningful branches (e.g., `feature/qc-pipeline`, `bugfix/mri-loader`).

  - Write clear commit messages describing _what_ and _why_.

- Store **configuration files** (e.g., `environment.yml`, `requirements.txt`, or `renv.lock`) to document software dependencies.

- Prefer **notebooks for exploration** and **scripts/modules for pipelines**:

  - Use notebooks for initial analysis and visualization.

  - Move stable code into reusable functions and scripts.

### Coding Style and Documentation

- Follow a consistent coding style (e.g., **PEP 8** for Python).

- Add short, clear **docstrings** and comments, especially for:

  - Data loading functions.

  - Pre-processing pipelines.

  - Model training and evaluation scripts.

- Log key steps and parameters (e.g., using simple logging libraries or structured text files).

## Using GitHub

GitHub provides a secure and structured way to collaborate on code, notebooks, documentation, and workflows. It ensures version control, transparency, and reproducibility across all team members working in HUNT Cloud.

### Use CIMORe Groupe Lab

- If the code or repo will be public or cited in publication, Locate your repo within
  https://github.com/ntnu-mr-cancer

  > [NOTE] if you don't have access to it, ask the CIMORe Group leader to point you towards who can add you to it.

- If the code or repo will be private and only meant for private or small group collaboration, it can be located on your private account or the CIMORe lab.

### Use Git for Version Control

- Track all scripts, notebooks, and configuration files through Git.

- Commit frequently with clear and descriptive messages.

- Avoid committing any sensitive data files (use `.gitignore` for this).

- Avoid committing large data files (use `.gitignore` for this).

#### Branch-Based Workflow

- Create a new branch for each feature, analysis, or task:

  - Example: `feature/qc-pipeline`, `analysis/mri-cleaning`, `fix/dicom-loader`

- In case of collaboration, open a Pull Request to merge changes and request review from team members.

#### Documentation in the Repository

- Include a `README.md` explaining:

  - How to run the code

  - Required dependencies

  - Folder structure

- Maintain additional documentation in `/docs` if needed.

#### Avoid Storing Data in GitHub

- Do **not** upload raw or sensitive data.

- Use symbolic references or documented file paths to shared cloud folders.

- Store only:

  - Code.

  - Metadata templates.

  - Example dummy datasets (if allowed).

### Repository Structure

Have an organized, clear structure, such as:

```text
repo-name/
  ├─ src/             # Scripts and modules
  ├─ notebooks/       # Jupyter notebooks
  ├─ config/          # Environment and configuration files
  ├─ docs/            # Documentation, SOPs, wiki files
  ├─ tests/           # Unit tests if applicable
  ├─ .gitignore       # Files/folders to exclude
  └─ README.md
```

## Using Large Language Models (LLMs) and Chatbots

#### Keep All Sensitive Information Inside the Cloud

- Do **not** paste patient data, filenames containing identifiers, project paths, or other sensitive information into external chatbots (e.g., ChatGPT).

- Only share **generic** code fragments or simplified examples when seeking help.

- For tasks involving real data or sensitive logic, work entirely **within the cloud workbench**.

#### Use LLMs as Assistants, Not Authorities

- Validate all model-generated code before use.

- Review logic, imports, file paths, and assumptions.

- Treat LLM responses as suggestions that require scientific and technical interpretation.

### Using Copilot in Secure Environments

- Don **NOT** use Copilot through tools (VS Code, JetBrains, etc.) **inside the cloud**.
