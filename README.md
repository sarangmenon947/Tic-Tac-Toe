# Tic Tac Toe

A simple two-player Tic Tac Toe game for the terminal, written in C.

---

## Features

- Two-player turn-based gameplay (Player X vs Player O)
- Input validation — rejects out-of-range and already-occupied cells
- Automatic win detection across rows, columns, and diagonals
- Draw detection when the board is full
- Clean, readable board printed after every move

---

## Getting Started

### Prerequisites

- A C compiler such as `gcc` or `clang`

### Build

```bash
gcc -o tictactoe tictactoe.c
```

### Run

```bash
./tictactoe
```

---

## How to Play

1. The game starts with **Player X**.
2. On each turn, enter your move as two numbers separated by a space:
   ```
   Player X, enter your move (row and column: 1-3 1-3): 2 3
   ```
   - The first number is the **row** (1–3, top to bottom).
   - The second number is the **column** (1–3, left to right).
3. Players alternate turns until one player wins or the game ends in a draw.

### Board Layout

```
 1 | 2 | 3   ← columns
---|---|---
 4 | 5 | 6
---|---|---
 7 | 8 | 9
```

Positions are addressed by (row, column) — for example, the centre cell is `2 2`.

---

## Game Rules

| Condition | Outcome |
|-----------|---------|
| A player fills an entire row | That player wins |
| A player fills an entire column | That player wins |
| A player fills either diagonal | That player wins |
| All 9 cells are filled with no winner | Draw |

---

## Code Structure

| Function | Description |
|----------|-------------|
| `initializeBoard()` | Fills the 3×3 board with blank spaces |
| `printBoard()` | Renders the current board state to stdout |
| `isWin()` | Checks whether the current player has won |
| `isDraw()` | Returns true when no empty cells remain |
| `switchPlayer()` | Toggles the active player between X and O |
| `playGame()` | Main game loop — handles input, validation, and end conditions |
| `main()` | Entry point — initialises the board and starts the game |

---

## Example Session

```
 X |   |  
---|---|---
   | X |  
---|---|---
   |   | X

Player X wins!
```
