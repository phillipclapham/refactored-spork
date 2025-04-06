# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project: AI Chat Arena with Moderator

### Build & Run Commands
- Start application: `python main.py`
- Install dependencies: `pip install -r requirements.txt`
- Run tests: `pytest`
- Run single test: `pytest tests/test_file.py::test_function`
- Lint code: `flake8`
- Type check: `mypy .`

### Code Style Guidelines
- **Formatting**: Use Black formatter with 88 char line length
- **Imports**: Group standard lib, third-party, and local imports with blank lines between
- **Typing**: Use type hints for all function parameters and return values
- **Naming**: snake_case for functions/variables, PascalCase for classes
- **Error Handling**: Use explicit try/except blocks with specific exceptions
- **Documentation**: Docstrings for all modules, classes, and functions
- **Testing**: Write unit tests for all functionality
- **Logging**: Use the standard logging module, not print statements

### Project Memory
- Reference `/project_memory/` directory for project documentation
- Always check relevant files before implementing new features
- Update documentation when making significant changes