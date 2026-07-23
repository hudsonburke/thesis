# Thesis: Use of Musculoskeletal Rodent Models for Investigating Neuromuscular Injury and Rehabilitation

This repository contains Hudson Burke's Master's thesis, built as a [Quarto](https://quarto.org/) book with embedded computational notebooks.

## Quickstart

```shell
# Clone with submodules
git clone --recurse-submodules https://github.com/hudsonburke/thesis.git
cd thesis

# Install Python dependencies with uv
uv sync

# Or with pip
# pip install -r requirements.txt
```

## Rendering

```shell
quarto render
```

Output formats: HTML (default), PDF, and DOCX.

## Repository structure

- `chapters/` — thesis chapters as Quarto markdown
- `src/` — submodules for supporting code and data
  - `RatHindlimb/` — rat hindlimb musculoskeletal model (model generation notebooks)
  - `tsl-optimization/` — tendon slack length optimization package
  - `rat-vml/` — volumetric muscle loss gait analysis data and figures
  - `osimpy/` — Pythonic OpenSim wrapper tools
  - `ASB2025-TSL-Optimization/` — ASB 2025 poster materials
- `data/` — analysis data (normalization results, fit parameters)
- `images/` — thesis figures
- `templates/` — cover and approval sheet templates
- `references.bib` — bibliography

## Notes

- OpenSim 4.6 wheels are available for Python 3.11–3.13. Ensure you're using one of these Python versions.
- All code that must interact with the OpenSim Python API should be run in notebooks or scripts separate from a Quarto document. Otherwise, it will crash the kernel (maybe because of a memory leak), and the Quarto document will not render.