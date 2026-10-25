# Learning Math for Finance

Applied companion to my math courses. Every notebook takes a concept I learned in
[LearningProbability](https://github.com/dnlwrthstr/LearningProbability),
[LearningLinearAlgebra](https://github.com/dnlwrthstr/LearningLinearAlgebra) or
[LearningCalculus](https://github.com/dnlwrthstr/LearningCalculus) and shows where it does real
work in finance: returns, risk, portfolios, factor models, pricing.

The rule: **no finance formula without the math behind it, and no math without a finance use.**

## Project Structure

- [`CURRICULUM.md`](./CURRICULUM.md): the full module plan, with the math prerequisite for each notebook and the reference courses the plan is based on.
- `modules/NN_<topic>/`: one numbered folder per module, notebooks numbered inside.
- `data/`: downloaded market data (CSV). Large files stay local and are git-ignored.
- `GUIDELINES.md`: the notebook specification, shared with the other Learning* repos, plus a finance-specific section.

## Getting Started

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
nbstripout --install --attributes .gitattributes   # once per clone
jupyter notebook
```

## License
This project is for educational purposes.
