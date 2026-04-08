# MiniRocket strict reproduction project

This project reproduces the **MiniRocket** paper baseline and then runs a smaller **MiniRocket-based improvement study**.

## What this project does

### Reproduction
- uses the **official MiniRocket code**
- runs the baseline on the paper dataset list
- compares our results against the paper's reported results
- saves:
  - `reproduction_results.csv`
  - `reproduction_failed.csv`
  - `paper_vs_ours.csv`
  - summary plots and summary files

### Improvements
- keeps **MiniRocket** as the main method
- tests 3 improvements:
  1. `MiniRocket_Ridge_20k`
  2. `MiniRocket_LogReg_10k`
  3. `MiniRocket_LinearSVC_10k`

## Files
- `minirocket_strict_reproduction_project.ipynb` — main notebook
- `requirements.txt` — packages to install
- `.gitignore` — ignores outputs and notebook checkpoints

## Setup

Create an environment and install:

```bash
pip install -r requirements.txt
```

## Run

Open the notebook and run cells in order.

### Helpful test setting
Inside the notebook, you can use:

```python
USE_FIRST_N = 5
```

to test on a few datasets first.

Then set:

```python
USE_FIRST_N = None
```

for the full reproduction run.

## Notes for the report

This project follows the brief by:
- using the data and code from the published paper
- checking whether the published results hold up
- recording lessons learned from reproduction
- proposing and testing improvements

One implementation detail:
- the official MiniRocket transform is used directly
- for the ridge classifier, the notebook uses a modern scikit-learn compatible setup with `StandardScaler()` + `RidgeClassifierCV(...)`

## Suggested GitHub repo structure

```text
minirocket-strict-reproduction/
├── minirocket_strict_reproduction_project.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```
