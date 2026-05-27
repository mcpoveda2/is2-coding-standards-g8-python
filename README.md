# loan-eligibility-python

Loan eligibility calculator for a cooperativa de ahorro y crédito. Computes whether a member is eligible for a loan and at what rate, based on income, debt, employment, and savings history.

## Linter

**Tool:** Pylint 4.0.5  
**Rule profile:** Default ruleset (all checkers enabled — conventions, refactoring, warnings, errors)  
**HTML report:** generated with `pylint-report`

```bash
pylint src/loan/eligibility.py --output-format=json > pylint-out.json
python -m pylint_report pylint-out.json --html-file reports/initial.html
```

## Setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Run the tests

```bash
pytest
```

## Use it from the CLI

```bash
python -m loan.cli --income 1200 --debt 320 --tenure-months 18 --age 34 --savings-balance 850
```
