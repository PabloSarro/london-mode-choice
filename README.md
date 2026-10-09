# london-mode-choice

Discrete choice models of transport mode choice (walk, cycle, public transport, car) in the London metropolitan area, built on the London Passenger Mode Choice (LPMC) data for the EPFL course *Mathematical Modeling of Behavior*.

The models are developed step by step, from a simple multinomial logit up to nested, cross-nested and mixture models. They are then used to compute market shares and to evaluate pricing scenarios.

## Repository structure

- `data/`: the group's LPMC sample (`lpmc09.dat`). Read-only.
- `src/assignment.ipynb`: model specification, estimation and tests.
- `PRESENTATION.md`: presentation notes.
- `info/`: course material and the assignment description.

## Installation

Requires Python 3.12.

```bash
python3.12 -m venv MMoB
source MMoB/bin/activate
pip install -r requirements.txt
python -m ipykernel install --user --name mmb --display-name "MMB"
```

## Running

Open `src/assignment.ipynb` in Jupyter or VS Code, select the **MMB** kernel and run all cells.

You can also run the notebook headless (from `src/`):

```bash
cd src
jupyter nbconvert --to notebook --execute --inplace assignment.ipynb
```
