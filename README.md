# 📊 Ad-Hoc Analysis Repository

Welcome to the **Ad-Hoc Analysis Repository**. This repo is designed to help organize, document, and share data analysis work conducted for Rounds. The structure is optimized for reusability, version control, and reproducibility of your analyses.

## 📂 Folder Structure

Here's an overview of the folder structure and its purpose:

```
ad-hoc-analysis/
├── data/
│   ├── raw/                # Unprocessed datasets from source
│   ├── processed/          # Cleaned and transformed data
│   └── external/           # Third-party datasets
├── notebooks/
│   ├── exploratory/        # Exploratory analysis notebooks
│   └── final/              # Polished and finalized analysis
├── scripts/
│   ├── etl/                # Extract, transform, load scripts
│   ├── analysis/           # Core analysis scripts
│   └── utils/              # Helper functions and utilities
├── reports/
│   └── figures/            # Generated plots and visualizations
├── config/
├── tests/                  # Unit tests for scripts
├── pyproject.toml          # All project info, including dependencies
├── uv.lock                 # Lockfile for `uv` package manager
├── requirements.txt        # For compatibility with `pip`
├── README.md               # Project documentation
├── .gitignore              # Files to exclude from version control
├── .python-version         # Python version (used by `uv`)
└── .pre-commit-config.yaml # Pre-commit hooks

```

## 🔧 How to Use This Repo

### 1. Clone the Repository

```bash
git clone git@github.com:anbelc/rounds.git
cd rounds
```

### 2. Set up the virtual environment and install dependencies

You can use `pip` or `uv` to install dependencies. The preferred method is `uv`.

#### Using `pip`
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

#### Using `uv`
```bash
uv sync
```

### 4. Run Your Analysis

You can explore the data and run your analysis by executing scripts or opening Jupyter notebooks. Note that the virtual environment has to be activated to run the scripts.

```bash
python -m scripts.analysis.your_script
```

Alternatively, you can run the script using `uv` without activating the virtual environment:

```bash
uv run python -m scripts.analysis.your_script
```

## 📚 Guidelines for Contributions

If you are contributing to this repo, please follow these guidelines:
- **Use clear and descriptive commit messages**.
- **Follow the folder structure**.
- **Document your code** using comments and docstrings.
- **Add tests** in the `tests/` folder where applicable.

## 🛠 Dependencies

All required packages are listed in `pyproject.toml`. Update this file preferably with `uv` if you add new dependencies. For example, to add `polars`, you can run:

```bash
uv add polars
```

The `requirements.txt` file is for compatibility with `pip`. It is automatically generated from `pyproject.toml` using `uv` via a pre-commit hook.