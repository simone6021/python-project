# Python Project Scaffold

## Installation

```bash
# Install uv (if not already installed)
curl -LsSf https://github.com/astral-sh/uv/releases/latest/download/uv-installer.sh | sh

# Create a virtual environment
uv venv

# Activate the virtual environment (optional; uv run can be used without activation)
source .venv/bin/activate

# Install the package in editable mode together with development dependencies
uv pip install -e .[dev]

# Lock the exact versions
uv lock

# Export a reproducible requirements.txt (optional for environments that need it)
uv export -f requirements.txt -o requirements.txt
```

## Updating Dependencies

```bash
# Upgrade packages and re‑lock
uv pip install -U -e .[dev]
uv lock
uv export -f requirements.txt -o requirements.txt
```

## Running the Application

```bash
uv run python -m src.python_project.main
```

## Development

- Run tests: `uv run pytest`
- Lint and format: `uv run ruff check .` and `uv run ruff format .`
- Type checking: `uv run mypy src`

## Installing from requirements.txt (fallback)

```bash
uv pip install -r requirements.txt
```

### Updating Dependencies

```bash
uv pip install -U -r requirements.txt
```

