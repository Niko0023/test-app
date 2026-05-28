# quiz-cli

## Overview
**quiz-cli** is an interactive command-line quiz game for learning JavaScript. It runs entirely in the terminal and guides the player through category selection, question count selection, the quiz itself, and a results screen with replay support.

This project is aimed at:
- JavaScript learners
- Developers who enjoy lightweight CLI games
- Anyone looking for a quick terminal-based quiz experience

## Features
- Interactive CLI quiz experience
- Category selection before starting a quiz
- Adjustable number of questions per session
- Quiz loop with score tracking
- Results summary at the end of each round
- Replay prompt to start another round
- Terminal color support for better readability
- Built with modern Node.js ES Modules

## Requirements
- **Node.js 18.0.0 or newer**
- A terminal that supports standard CLI input/output

## Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd quiz-cli
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Ensure the quiz data and helper modules referenced by the app are available:
   - `data/questions.json`
   - `src/input.js`
   - `src/quiz.js`
   - `src/colors.js`

   The entry point `index.js` references these paths directly, so the project should include them for the app to run correctly.

## Usage
Start the quiz game with:

```bash
npm start
```

Or run the entry point directly:

```bash
node index.js
```

### What to expect
- Select a quiz category
- Choose how many questions you want to answer
- Answer each question in the terminal
- View your final results
- Choose whether to play again

## Scripts
- **`npm start`** — Runs the app using `node index.js`
- **`npm test`** — Runs the Node.js test runner via `node --test`

## Project Structure
The repository snapshot shows the top-level entry files, and the main script references additional project assets:

```text
quiz-cli/
├── index.js
├── package.json
├── src/
│   ├── input.js
│   ├── quiz.js
│   └── colors.js
└── data/
    └── questions.json
```

### Notes
- `index.js` is the main CLI entry point and includes the shebang for direct execution.
- `src/` contains the app’s logic and terminal helpers.
- `data/` stores the quiz question bank.

## How It Works
1. **Startup**
   - The CLI is launched from `index.js`.
   - It uses built-in Node.js modules such as `fs/promises`, `path`, and `url`.

2. **Load Questions**
   - Quiz questions are read from `data/questions.json`.

3. **User Interaction**
   - The app prompts the user to choose a category and the number of questions.

4. **Quiz Loop**
   - Questions are presented one by one.
   - Answers are checked and the score is updated.

5. **Results**
   - At the end, the app displays the result summary.

6. **Replay / Cleanup**
   - The user can choose to play again.
   - Input handling and session cleanup are performed before exit.

## Testing
Run the test suite with:

```bash
npm test
```

This uses Node’s built-in test runner, so tests should be written using the standard `node:test` APIs.

## License
This project is licensed under the **MIT License**.
