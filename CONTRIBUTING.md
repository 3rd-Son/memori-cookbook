# Contributing to Memori Cookbook

Thank you for your interest in contributing to the Memori Cookbook!

## Development Setup

### Prerequisites

- Python 3.10+ (3.12 recommended)
- [uv](https://github.com/astral-sh/uv) - Fast Python package installer
- Make

### Quick Start

```bash
# Install uv if you haven't already
curl -LsSf https://astral.sh/uv/install.sh | sh

# Clone the repository
git clone https://github.com/MemoriLabs/memori-cookbook.git
cd memori-cookbook

# Install dependencies
uv sync --extra dev

# Install pre-commit hooks
uv run pre-commit install

# Run linting
uv run ruff check .
```

## Adding a New Example

### Example Structure

Each example should be self-contained in its own directory:

```
examples/category/example-name/
├── README.md           # Documentation for the example
├── main.py             # The example code
├── pyproject.toml      # Dependencies specific to this example
└── .env.example        # Required environment variables
```

### README Template

Each example README should include:

```markdown
# Example Title

Brief description of what this example demonstrates.

## Quick Start

1. **Install dependencies**:
   ```bash
   uv sync
   ```

2. **Set environment variables**:
   ```bash
   export OPENAI_API_KEY=your_api_key_here
   ```

3. **Run the example**:
   ```bash
   uv run python main.py
   ```

## What This Example Demonstrates

- Point 1
- Point 2
- Point 3

## Prerequisites

- List any specific requirements
```

### Code Standards

- Follow PEP 8 standards
- Line length: 88 characters (Black-compatible)
- Use Python 3.10+ syntax and type hints
- Include docstrings for modules
- Keep examples simple and focused on one concept

### Example Checklist

Before submitting a new example:

- [ ] Example runs successfully with `uv run python main.py`
- [ ] README.md includes all required sections
- [ ] pyproject.toml lists all dependencies
- [ ] .env.example lists all required environment variables
- [ ] Code passes `uv run ruff check .`
- [ ] Code is formatted with `uv run ruff format .`
- [ ] Example is added to the table in the main README.md

## Code Quality

We use [Ruff](https://docs.astral.sh/ruff/) for linting and formatting:

```bash
# Format code
uv run ruff format .

# Check linting
uv run ruff check .

# Auto-fix issues
uv run ruff check --fix .
```

### Pre-commit Hooks

Pre-commit hooks run automatically on each commit:

```bash
# Install hooks (one-time setup)
uv run pre-commit install

# Run manually on all files
uv run pre-commit run --all-files
```

## Pull Request Guidelines

1. **Fork and branch**: Create a feature branch from `main`
2. **Write clear commits**: Keep commits focused and well-described
3. **Test your example**: Ensure it runs successfully
4. **Pass all checks**: Linting and formatting must pass
5. **Update documentation**: Add your example to the main README table

## Development Commands

```bash
make help         # Show all available commands
make dev          # Install dev dependencies
make lint         # Run linting
make format       # Format code
make clean        # Clean cache files
make pre-commit   # Run pre-commit on all files
```

## Questions

- [GitHub Issues](https://github.com/MemoriLabs/memori-cookbook/issues) - Bug reports and feature requests
- [Discussions](https://github.com/MemoriLabs/memori-cookbook/discussions) - Questions and community
