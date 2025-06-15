
# Audio Map Repository Overview

## Purpose
Audio Map is an interactive tool for exploring large collections of audio samples using dimensionality-reduction techniques and a monome arc controller. It processes audio files, extracts features, creates 2D embedding maps, and allows real-time navigation through the audio samples.

The primary purpose of this repository is to provide musicians, sound designers, and researchers with a powerful tool for exploring and discovering relationships within large audio sample libraries.

## General Setup
This project is built using Python and requires several key dependencies:
- Python 3.8+
- Monome Arc controller (for hardware interaction)
- Various Python packages for audio processing, feature extraction, and dimensionality reduction

### Installation
The project can be installed using pip with the following command:
```bash
pip install -e .
```

For development purposes, additional tools are available:
```bash
pip install -e ".[dev]"
```

## Repository Structure
```
arc-audiomap/
├── .cursor/                  # Cursor configuration files
├── .git/                     # Git repository files
├── audio_map/                # Main package containing the core functionality
│   ├── __init__.py           # Package initialization
│   ├── cli.py                # Command-line interface implementation
│   ├── build.py              # Audio processing and map building logic
│   └── runtime.py            # Real-time navigation and playback code
├── examples/                 # Example scripts demonstrating usage
│   └── arc.py                # Basic Arc connectivity and control example
├── .gitignore                # Git ignore file
├── README.md                 # Project documentation
├── pyproject.toml            # Project configuration (dependencies, tools)
├── requirements.txt          # Additional dependencies
```

## CI Checks and Code Quality Tools
The project uses several code quality tools as part of its development workflow:

- **Black**: Code formatting (`black .`)
- **Ruff**: Linting (`ruff check .`)
- **MyPy**: Type checking (`mypy .`)
- **Pytest**: Testing (`pytest`)

These tools are configured in the `pyproject.toml` file and can be used to maintain code quality during development.

## Usage
The main functionality is accessed through command-line commands:

1. Build an audio map from a folder of samples:
   ```bash
   audio-map build ~/Music/samples
   ```

2. Run the interactive navigator:
   ```bash
   audio-map run
   ```

3. Test Arc connectivity with the example script:
   ```bash
   python examples/arc.py
   ```
