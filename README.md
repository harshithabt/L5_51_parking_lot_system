# Lab 5: Static Code Analysis – Parking Lot System

---

**Lab Repository:** [L5_51_parking_lot_system](https://github.com/harshithabt/L5_51_parking_lot_system)

**All SE Labs Repository:** [SE_Labs](https://github.com/harshithabt/SE_Labs)

Assigned application: `parking_lot_system.py`.

---

Follow the Lab 05 handout for the complete assignment requirements. This
local pack preserves the original PES assignment structure and adds the
project-specific reports and verification information.

---

## About the program

The parking lot system manages parking slots, vehicle plates, parking fees,
ticket PINs, vehicle hashes, total collections, and parking-manifest export.
The completed program preserves secure PIN generation, SHA-256 hashing, safe
JSON export, numeric surge-multiplier validation, and existing parking-lot
functionality.

## What to do

1. Run the program first and inspect its output:

   ```bash
   python parking_lot_system.py
   ```

2. Install the analysis tools:

   ```bash
   pip install pylint bandit flake8
   ```

3. Run the analysis and save the reports:

   **Note:** Generate the `before` reports using the untouched original starter implementation before making any changes. After refactoring the code, generate the `after` reports using the final implementation. The committed reports preserve the results from both stages.

```bash
   # Original source analysis
   pylint parking_lot_system.py > reports/before/pylint_report.txt
   bandit -r parking_lot_system.py > reports/before/bandit_report.txt
   flake8 parking_lot_system.py > reports/before/flake8_report.txt

   # Final refactored source analysis
   pylint parking_lot_system.py > reports/after/pylint_report.txt
   bandit -r parking_lot_system.py > reports/after/bandit_report.txt
   flake8 parking_lot_system.py > reports/after/flake8_report.txt
```

4. Document the findings in `issues.md` using this table:

   | Issue | Type | Line(s) | Description | Fix Approach |
   |-------|------|---------|-------------|--------------|
   | ... | ... | ... | ... | ... |

   Record tool-detected findings separately from manual code-review
   findings. Place high- and medium-severity issues first.

5. Fix at least four documented issues, preserve the program's behavior, and
   rerun Pylint, Bandit, and Flake8.

6. Answer the four reflection questions from the handout in `reflection.md`.
   The supplied local materials do not contain the official wording, so the
   current reflection preserves four topic-based responses without inventing
   question text.

## Project structure

```text
L5_51_parking_lot_system/
|
|-- parking_lot_system.py
|-- issues.md
|-- reflection.md
|-- README.md
|
|-- reports/
    |
    |-- before/
    |   |-- README.md
    |   |-- pylint_report.txt
    |   |-- bandit_report.txt
    |   |-- flake8_report.txt
    |
    |-- after/
        |-- README.md
        |-- pylint_report.txt
        |-- bandit_report.txt
        |-- flake8_report.txt
```

## Static Analysis Results

The original GitHub starter implementation was analysed using Pylint, Bandit, and Flake8. The reports are preserved in `reports/before/`.

### Before Refactoring

- Pylint: **4.10/10**.
- Bandit: **5 findings** (2 High, 1 Medium, 2 Low).
- Flake8: **10 violations**.

The findings included unsafe dynamic evaluation, shell command execution, weak hashing, predictable random-number generation, exception handling issues, unused imports, and formatting violations.

### After Refactoring

The final implementation was analysed again using the same tools. The reports are preserved in `reports/after/`.

- Pylint: **10.00/10**.
- Bandit: **No findings**.
- Flake8: **No violations**.

### Additional Verification

The final implementation was additionally checked through:

- Python compilation using `py_compile`.
- Focused behaviour assertions for parking, slot release, collection tracking, fee calculation, SHA-256 hashing, and PIN generation.
- Normal program execution.

All recorded checks passed.

## Deliverables

1. `parking_lot_system.py`: the cleaned implementation with at least four
   issues fixed.
2. `issues.md`: the comprehensive issue table and verification record.
3. `reflection.md`: the four reflection responses.
4. `reports/before` and `reports/after`: preserved static-analysis reports.

## Target

Aim for a Pylint score above 9.5. A perfect 10.00/10 is very good. The
final submission should have no unresolved Flake8 or Bandit findings and
should preserve the application's behavior.

Be ready to explain the bugs found, the distinction between inherited fixes
and local tool findings, and the verification performed.

---

## Lab 05 Deliverables

The complete Lab05 submission, including the refactored source code, issue documentation, reflection responses, and before/after static analysis reports, is maintained in the `Lab05/` folder of the main [SE_Labs repository](https://github.com/harshithabt/SE_Labs).

The original assignment repository and the individual Lab05 repository are also maintained separately for reference.

- **Individual Lab Repository:** [L5_51_parking_lot_system](https://github.com/harshithabt/L5_51_parking_lot_system)
- **Main SE Labs Repository:** [SE_Labs](https://github.com/harshithabt/SE_Labs)

---

## Author

**Harshitha B.T. – PES1UG24AM118 (AIML-B Section)**

**Course:** Software Engineering Laboratory

---
