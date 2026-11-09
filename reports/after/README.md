# Final Parking Lot System - After Code Analysis

---

## Overview

This folder contains the static code analysis reports generated after refactoring and improving the original Parking Lot System implementation for Lab 5 - Static Code Analysis.

The final implementation was analysed using **Pylint, Bandit and Flake8** to evaluate code quality, security and coding-standard compliance.

## Analysed Source File

- `parking_lot_system.py` — Refactored Parking Lot System implementation.

## Tools Used

| Tool | Purpose |
|---|---|
| Pylint | Identifies programming errors, code-quality issues, naming violations and maintainability concerns. |
| Bandit | Detects potential security vulnerabilities in Python code. |
| Flake8 | Checks Python code style, formatting and programming errors. |

## Analysis Commands

The following commands were used to generate the reports:

```bash
pylint parking_lot_system.py > reports/after/pylint_report.txt
bandit -r parking_lot_system.py > reports/after/bandit_report.txt
flake8 parking_lot_system.py > reports/after/flake8_report.txt
```

## Final Analysis Results

The refactored implementation was verified against the three static-analysis tools.

| Tool | Final Result |
|---|---|
| Pylint | 10.00/10 |
| Bandit | No security findings |
| Flake8 | No violations |

## Improvements Achieved

The refactoring addressed the identified code-quality and security concerns, including:

- Improved naming conventions and code documentation.
- Removed unsafe dynamic expression evaluation.
- Replaced weak MD5 hashing with SHA-256.
- Used cryptographically secure random generation for ticket PINs.
- Removed shell command execution.
- Replaced broad exception handling.
- Eliminated mutable default arguments.
- Improved input validation and resource management.
- Improved code organisation, type hints and maintainability.

## Report Files

- `pylint_report.txt` — Final Pylint analysis output.
- `bandit_report.txt` — Final Bandit security analysis output.
- `flake8_report.txt` — Final Flake8 analysis output.

## Conclusion

The final implementation achieved a Pylint score of 10.00/10, with no Bandit security findings and no Flake8 violations. These results demonstrate the improvements made to the original Parking Lot System through static code analysis and refactoring.

---
