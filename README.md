# Test Case: Pip Priority Conflict - .tool-versions vs pyproject.toml

## Package Manager
Pip

## Python Version Detection
- **Source**: .tool-versions (PRIORITY #2)
- **Expected Version**: 3.9.7
- **Conflict**: pyproject.toml says >=3.10

## Files Present
- .tool-versions - python 3.9.7 (SHOULD WIN)
- pyproject.toml - requires-python = ">=3.10" (SHOULD BE IGNORED)
- requirements.txt

## Test Purpose
Validate .tool-versions beats pyproject.toml.
