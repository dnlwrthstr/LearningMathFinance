# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this project is

A personal learning project: applied mathematics for finance. Each notebook connects a concept from
the sibling course repos (LearningProbability, LearningLinearAlgebra, LearningCalculus) to a
finance application. There is no application code, build system, or test suite; the deliverables
are notebooks.

## Structure

- `CURRICULUM.md`: the module plan. Check it before creating a notebook; keep it in sync (mark notebooks done, add new ones in the right module).
- `modules/NN_<topic>/NN_<notebook>.ipynb`: notebooks, numbered.
- `GUIDELINES.md`: the authoritative spec for every notebook, including the "Finance notebooks" section at the end. Read it before creating or editing a notebook.

## Creating notebooks

Follow GUIDELINES.md. Finance-specific essentials:

- Open with a **Math link** cell naming the prerequisite concept and linking the sibling-repo notebook that teaches it (GitHub URL, see CURRICULUM.md).
- Derive before you apply: the math result first (short, with LaTeX), then the finance interpretation.
- Default to synthetic data with a fixed seed (`np.random.default_rng(42)`) so notebooks run offline. Real data, when used, is read from `data/` and the source is cited in the notebook.
- State units every time: returns as decimals or %, periodicity (daily/monthly/annual), currency (CHF by default).
- Currency in markdown follows the GUIDELINES rule: no literal dollar signs; write `CHF 1,000` or code spans.

## Environment

Python 3 with Jupyter, run from PyCharm or `jupyter notebook`. Write numpy code that works in numpy 1.x and 2.x (avoid `np.trapz`, `np.in1d`, `np.row_stack`).

## Git

Notebook outputs are stripped on commit via nbstripout (`.gitattributes` + local git config). Register once per clone with `nbstripout --install --attributes .gitattributes`. Never commit notebooks with outputs.
