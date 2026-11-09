# Original Parking Lot System - Before Code Analysis

---

## Source

**status:** Original, unmodified assignment starter code
This is the starter application provided for Lab 5 - Static Code Analysis.

**Original repository:**  
https://github.com/SETAPESU26/L5_51_parking_lot_system

**Assigned file:** `parking_lot_system.py`

## About the Program

The application demonstrates a basic parking lot management system. It manages parking slots, vehicle registration, parking fee calculation, vehicle hashing, ticket PIN generation, and parking manifest export.

## Original Implementation

The starter program contains the initial implementation supplied for the assignment, before our code-quality and security improvements.

The original source includes the following areas for inspection:

- Parking slot management and collection tracking.
- Vehicle parking and slot release operations.
- Parking fee calculation using a surge expression.
- Vehicle hash generation.
- Ticket PIN generation.
- Parking manifest export.
- Available parking slot summary.
- Main demonstration function.

## Initial Source Characteristics

The original implementation uses:
- Global mutable collection state.
- A mutable default argument for entry logs.
- Broad exception handling.
- Dynamic expression evaluation using `eval()`.
- MD5 hashing.
- `random.randint()` for ticket PIN generation.
- Shell command execution using `os.system()`.
- A hard-coded barrier secret.
- Manual file opening and closing.
- Inconsistent function naming and limited input validation.

These are part of the original starter implementation and are examined during the static code analysis and manual code review.

## Purpose

This folder represents the original assignment baseline. It is retained for reference and comparison with the final refactored implementation.

---
