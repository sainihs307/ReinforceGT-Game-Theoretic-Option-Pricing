# Reinforced Game Theory

A small collection of Python scripts implementing core game theory concepts: checking for pure-strategy Nash equilibria and computing best responses in two-player games.

## Contents

- `Assgn1_240318_Daksh Saijwal.py` — Checks whether a given strategy profile in a 2x2 Prisoner's Dilemma-style game (Cooperate/Defect) is a Pure Nash Equilibrium. Takes user input, looks up payoffs from a fixed payoff matrix, and verifies that neither player can unilaterally improve their payoff by deviating.
- `Assgn2_240318_Daksh_Saijwal.py` — Computes the set of best-response actions for a given player against a fixed opponent action, using a payoff matrix supplied in nested-dictionary form.

## Requirements

- Python 3

No external dependencies are required.

## Usage

### Pure Nash Equilibrium checker

```bash
python "Assgn1_240318_Daksh Saijwal.py"
```

You'll be prompted to enter a strategy profile, e.g.:

```
Enter strategy profile(eg. C D): C C
```

The script reports whether the entered profile is a Pure Nash Equilibrium under the built-in payoff matrix:

| | C | D |
|---|---|---|
| **C** | (3, 3) | (0, 5) |
| **D** | (5, 0) | (1, 1) |

### Best response calculator

`Assgn2_240318_Daksh_Saijwal.py` defines a `bestResponse(payoff_matrix, player, opponent_action)` function rather than a standalone script. Import it and call it with a payoff matrix in the form:

```python
payoff_matrix = {
    "A": {"X": (3, 3), "Y": (0, 5)},
    "B": {"X": (5, 0), "Y": (1, 1)},
}

bestResponse(payoff_matrix, player=1, opponent_action="X")
```

It returns the set of actions that maximize the specified player's payoff given the opponent's fixed action.

## Background

These scripts were written as course assignments applying foundational game theory concepts — Nash equilibria and best-response analysis — in code.
