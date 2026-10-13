# Tic-Tac-Toe App

A classic two-player Tic-Tac-Toe game built with **React** and **Vite**. Players take turns placing X and O on a 3×3 board, and the game announces the winner as soon as a line of three is completed.

## Features

- Two-player, turn-based gameplay on the same device (X always goes first)
- Automatic winner detection across all 8 winning lines (3 rows, 3 columns, 2 diagonals)
- Board locks after a win so no further moves can be made
- "Congratulations" banner showing the winning symbol
- One-click **Reset** button to start a new game
- Fast development experience with Vite and hot module replacement (HMR)

## Tech Stack

| Tool | Purpose |
| --- | --- |
| [React 19](https://react.dev/) | UI and game state (`useState`, `useRef`) |
| [Vite 6](https://vite.dev/) | Dev server and build tool |
| [ESLint 9](https://eslint.org/) | Linting, with the React Hooks and React Refresh plugins |

## Project Structure

```
Tic-Tac-Toe-App/
├── public/              # Static assets
├── src/
│   ├── assets/          # X (cross) and O (circle) icons
│   ├── components/
│   │   ├── TicTacToe.jsx   # Game board, turn logic, win check, reset
│   │   └── TicTacToe.css   # Game styling
│   ├── App.jsx          # Root component
│   └── main.jsx         # App entry point
├── index.html
├── vite.config.js
├── eslint.config.js
└── package.json
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) 18 or later
- npm (comes with Node.js)

### Installation

```bash
# Clone the repository
git clone https://github.com/Ashis2005-prog/Tic-Tac-Toe-App.git

# Move into the project folder
cd Tic-Tac-Toe-App

# Install dependencies
npm install
```

### Run in development

```bash
npm run dev
```

Then open the local URL printed in the terminal (usually `http://localhost:5173`).

### Available scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Vite development server with HMR |
| `npm run build` | Create an optimized production build in `dist/` |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint on the project |

## How to Play

1. Player **X** starts by clicking any empty square.
2. Player **O** then clicks another square, and the two players alternate.
3. The first player to place three of their symbols in a row, column, or diagonal wins.
4. Click **Reset** at any time to clear the board and start over.

## How It Works

Game state lives in `src/components/TicTacToe.jsx`:

- A 9-element array tracks which player owns each square.
- A turn counter decides whether the next move is X (even) or O (odd).
- After every move, `checkWin()` compares the board against all eight winning combinations.
- When a win is found, `won()` locks the board and updates the title with the winner's icon.
- `reset()` clears the board array, the squares, and the title.

## Possible Improvements

- Detect and announce a draw when all nine squares are filled
- Prevent overwriting a square that has already been played
- Replace direct DOM updates (`innerHTML`) with React state-driven rendering
- Add a scoreboard to track wins across games
- Add a single-player mode with a computer opponent

## Contributing

Contributions are welcome. Fork the repository, create a feature branch, and open a pull request.

## License

No license has been specified for this project yet. Add a `LICENSE` file (for example MIT) if you want others to reuse the code.

## Author

Created by [Ashis2005-prog](https://github.com/Ashis2005-prog).
