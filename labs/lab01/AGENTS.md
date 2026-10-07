# AGENTS.md

## Purpose
This file gives the most useful, non‑obvious guidance for an OpenCode agent working in this repository.

## Repository layout
- `labs/lab01/`: contains a CSV dataset and a PDF with lab notes. No executable code.
- `notebooks/1-FFNN/`: Jupyter notebooks that illustrate a simple feed‑forward neural network.

No other source files exist; the repo is *data‑only*.

## What an agent might miss without help
- **How to run notebook cells**: Agents may assume there is a build or test script.  In fact, you must launch Jupyter (or open the `.ipynb` in VS Code) and execute the cells manually.
- **Data location**: The dataset lives at `labs/lab01/dataset_lab_1.csv`.  Any data‑loading code should reference that path.
- **PDF content**: `labs/lab01/Lab1_FFNN.pdf` contains the theoretical background.  It is not parsed automatically by agents.

## Quick actions for an agent
| Action | Command | Notes |
|--------|---------|-------|
| Start Jupyter to run notebooks | `jupyter notebook --notebook-dir=notebooks/1-FFNN` | Requires Python 3 and the `ipykernel` package.  Use a virtual environment if needed. |
| Open PDF in default viewer | `xdg-open labs/lab01/Lab1_FFNN.pdf` (Linux) | On macOS use `open`. |

## Avoiding common mistakes
- **Do not run**: `npm install`, `pip install .`, or any build scripts; none exist.
- **Do not look for tests**: There are no unit or integration tests in this repo.
- **Do not assume a CI pipeline**: No `.github/workflows` directory.

## References to other instruction files
- None – this repository has no `opencode.json`, `CLAUDE.md`, or other instruction sets.

---
This file is intentionally short because the repo contains only data and notebooks.  If new code is added, update AGENTS.md accordingly.
