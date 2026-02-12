# ♟️ Chess Game Analyzer

A full-stack web application that analyzes chess games using [Stockfish](https://stockfishchess.org/) and classifies each move (e.g., Brilliant, Blunder, etc.) similar to Chess.com. Built using **React**, **Flask**, and **Chess.com Public API**.

---

## 🚀 Features

- ♖ Upload PGN files or paste PGN directly
- 🔍 Fetch and analyze **recent games from Chess.com**
- 📈 See **accuracy scores** for both players (White & Black)
- ✅ Move classification: Best, Brilliant, Great, Good, Inaccuracy, Blunder
- ♟️ Visualize game using an interactive chessboard
- ▶️ Play through moves with "Next" and "Previous" navigation

---

## 🛠 Tech Stack

### Frontend:
- React
- react-chessboard
- Axios
- CSS Modules / Custom Styling

### Backend:
- Flask (Python)
- python-chess
- Stockfish (UCI Engine)
- Chess.com API

---

## ▶️ Running Locally (Stockfish Setup)

This repo does **not** commit the Stockfish binary (it is large). To run analysis you must provide Stockfish in one of these ways:

- Place the executable at `backend/stockfish/stockfish.exe` (Windows), or
- Set an environment variable `STOCKFISH_PATH` to the full path of your Stockfish executable.

If Stockfish is missing, the backend returns a clear error message.

### Download Stockfish

- Download Stockfish from the official site: https://stockfishchess.org/download/
- Extract it and locate the engine executable:
	- Windows: typically `stockfish.exe`
	- macOS/Linux: typically `stockfish` (you may need `chmod +x stockfish`)

### Point the Backend to Stockfish

Option A (recommended): set `STOCKFISH_PATH`

- PowerShell (Windows):
	- `$env:STOCKFISH_PATH = "C:\\path\\to\\stockfish.exe"`

- bash/zsh (macOS/Linux):
	- `export STOCKFISH_PATH="/path/to/stockfish"`
	- (optional) persist it by adding the line above to `~/.zshrc` or `~/.bashrc`

Option B: copy into the repo (Windows)

- Put the file at `backend/stockfish/stockfish.exe`
