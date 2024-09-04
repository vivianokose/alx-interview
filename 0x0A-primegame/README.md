---

# 0x0A. Prime Game

## Overview

**Prime Game** is a mathematical game designed for two players. The game is based on selecting prime numbers from a list of integers. The players take turns choosing primes, and the game continues until there are no primes left that can be selected. The player who cannot make a move loses the game.

## Rules

1. **Game Setup**:
   - The game starts with a list of integers ranging from 1 to `n`.

2. **Prime Selection**:
   - Players take turns selecting a prime number from the list.
   - Once a prime is selected, all its multiples are removed from the list.

3. **Winning Condition**:
   - The game continues until no more primes can be selected.
   - The player who cannot make a valid move loses the game.

## Implementation

The game is implemented using Python. The key functionalities include:

- **Prime Checking**: A function to check if a number is prime.
- **Prime Selection**: A function to handle the selection of primes and removal of their multiples.
- **Game Loop**: A loop to alternate between players, executing moves until the game ends.
