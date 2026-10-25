# GUIDELINES.md

## Purpose

Template for generating high-quality educational Jupyter notebooks in the style previously established.

Use this document as the default specification when creating new math / statistics / programming learning notebooks.

---

## Core Output Requirements

- Deliver a **downloadable `.ipynb` notebook**.
- Notebook must run in a standard Python 3 environment.
- Use clean structure, readable markdown, and executable code cells.
- Prefer self-contained notebooks (minimal dependencies).

Recommended libraries:

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import sympy as sp
```

Use additional libraries only when necessary.

---

## Teaching Style

### Tone

- Clear
- Structured
- Practical
- Precise
- Beginner-friendly but not simplistic

### Explain Concepts in Layers

For each topic:

1. Intuition  
2. Formal definition  
3. Worked examples  
4. Visual explanation  
5. Python implementation  
6. Practice exercises  
7. Summary

---

## Notebook Structure (Default)

# Title

Short description of what the notebook teaches.

## 1. Introduction

- Why topic matters
- Real-world relevance
- What learner will know after completion

## 2. Theory

Use markdown with LaTeX:

```markdown
$$
f'(x)=\lim_{h\to0}\frac{f(x+h)-f(x)}{h}
$$
```

## 3. Worked Examples

Show step-by-step calculations.

## 4. Python Examples

Executable code cells demonstrating the topic.

## 5. Visualizations

Use plots where useful.

## 6. Exercises

Include short tasks.

## 7. Solutions / Checks

Optional answer cells.

## 8. Conclusion

Concise recap.

---

## Markdown Rules

- Use headings generously.
- Use bullet lists for clarity.
- Keep paragraphs short.
- Use LaTeX for formulas.

Inline math:

```markdown
$ax^2+bx+c$
```

Display math:

```markdown
$$
x = \frac{-b \pm \sqrt{b^2-4ac}}{2a}
$$
```

Currency dollar signs: never write a literal `$` (or `\$`, or `&#36;`) in markdown prose — PyCharm's renderer pairs it with the next math `$` and swallows the text between as LaTeX. Write amounts as code spans (`` `$1` ``, `` `$22,000` ``), and keep the `$` symbol out of LaTeX formulas entirely (write `= 5`, not `= \$5`; the surrounding prose carries the currency).

---

## Code Rules

- Every code cell should run independently where practical.
- Use comments sparingly but clearly.
- Prefer readable variable names.
- Avoid unnecessary abstraction.

Good:

```python
x = np.linspace(-5, 5, 400)
y = x**2
```

Avoid:

```python
a=np.linspace(-5,5,400);b=a**2
```

---

## Visualization Rules

Use matplotlib unless another library is requested.

### Standards

- Figure size readable
- Axis labels
- Title
- Grid when useful
- Legends when multiple lines

Template:

```python
plt.figure(figsize=(8,5))
plt.plot(x, y, label="f(x)")
plt.title("Function Plot")
plt.xlabel("x")
plt.ylabel("y")
plt.grid(True, alpha=0.3)
plt.legend()
plt.show()
```

---

## Topic-Specific Enhancements

### Mathematics

Include:

- Symbolic derivations with SymPy
- Numeric approximations
- Graphical intuition

### Statistics

Include:

- Simulations
- Histograms
- Hypothesis tests
- Interpretation of outputs

### Probability

Include:

- Simulations of random experiments
- Distributions and their visualizations
- Worked probability calculations

### Calculus

Include:

- Limits
- Derivatives
- Integrals
- Tangents / areas

---

## Exercise Design

Use three levels:

### Basic

Direct application.

### Intermediate

Multi-step reasoning.

### Advanced

Interpretation or proof-like thinking.

---

## Quality Checklist

Before finalizing:

- Notebook opens correctly
- JSON valid
- All cells render
- Code runs
- Plots display
- Math formatting correct
- Sections logically ordered
- No unexplained jumps in reasoning

---

## Default Closing Message

Use:

> Done — here is the notebook:

> [Download the notebook](sandbox:/mnt/data/<filename>.ipynb)

> It includes:
> - theory
> - worked examples
> - Python code
> - visualizations
> - exercises

---

## Reusable Prompt Template

```text
Create a Jupyter notebook in the established style about [TOPIC].

Include:
- intuition
- formal theory
- step-by-step examples
- Python code
- charts/visuals
- exercises
- summary

Make it downloadable as .ipynb
```

---

## Golden Rule

Every notebook should help the learner **understand**, **see**, and **apply** the concept.

---

## Finance Notebooks (this repository)

Everything above applies. In addition, every notebook in this repository:

### Adds two sections to the default structure

- **0. Math link** (before the Introduction): one or two sentences naming the math concept used,
  with a link to the sibling-repo notebook that teaches it, e.g.
  `[Variance](https://github.com/dnlwrthstr/LearningProbability/blob/main/coursera/02_discribing_distribution/05_variance.ipynb)`.
- **Finance application** (after Worked Examples): where practitioners use the result, what
  the numbers mean, and the usual misreading.

### Data

- Synthetic data with a fixed seed by default: `rng = np.random.default_rng(42)`.
- Real data only from CSVs in `data/`, with source and download date stated in the notebook.
- Always label units: periodicity, decimal vs %, currency (CHF by default).

### Conventions

- Returns: `r` for simple, `log_r` for log returns. Annualize with an explicit `periods_per_year`.
- Weights `w` are column vectors; covariance matrix `Sigma`; portfolio variance `w @ Sigma @ w`.
- Exercises include at least one "interpret this number" question, not only computations.
