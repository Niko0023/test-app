# quiz-cli

Interactive command-line quiz game for learning JavaScript.

## Features
- Interactive terminal-based quiz experience
- Category selection before starting a quiz
- Question count selection for each session
- Score tracking and final results summary
- Replay prompt to play another round
- ES Modules-based Node.js application
- Uses built-in Node.js APIs for file handling and path resolution

## Requirements
- **Node.js 18.0.0 or newer**
- A terminal capable of running Node.js CLI apps

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Niko0023/test-app.git
   cd test-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Make sure the quiz data and referenced source files are present in the repository:
   - `data/questions.json`
   - `src/input.js`
   - `src/quiz.js`
   - `src/colors.js`

   > The repository snapshot confirms `index.js` and `package.json` at the top level, and `index.js` references the files above.

## Usage
Start the quiz with:

```bash
npm start
```

You can also run the entry point directly:

```bash
node index.js
```

### Typical flow
1. Show the CLI banner
2. Load quiz questions
3. Choose a category
4. Choose how many questions to answer
5. Run the quiz
6. Show results
7. Prompt to play again

## Available scripts
- `npm start` — Runs the application with `node index.js`
- `npm test` — Runs the Node.js test runner with `node --test`

## Project structure
Based on the repository snapshot and the code references in `index.js`, the project is organized roughly like this:

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
- `index.js` is the main CLI entry point and includes a shebang for direct execution.
- `src/` likely contains input handling, quiz logic, and terminal color helpers.
- `data/questions.json` stores the quiz question set.

## How it works
The app is a Node.js CLI quiz game built with ES Modules.

### Runtime flow
- **Banner**: The app starts by displaying a banner or intro.
- **Load questions**: Questions are loaded from `data/questions.json`.
- **Category selection**: The user chooses a quiz category.
- **Question count**: The user chooses how many questions to answer.
- **Quiz loop**: Questions are presented one by one and answers are checked.
- **Results**: The final score and results are displayed.
- **Replay prompt**: The user can start a new round or exit.

### Implementation notes
- The entry point uses built-in Node.js modules such as:
  - `fs/promises`
  - `path`
  - `url`
- The app references helper modules in `src/` for input handling, quiz logic, and colors.

## Testing
Run tests with:

```bash
npm test
```

This uses Node’s built-in test runner. Any tests added to the project should be compatible with `node --test`.

## License
This project is licensed under the **MIT License**.

## Contributing or next steps
If you want to extend the project, good next steps could include:
- Adding more quiz categories and questions
- Improving input validation and error handling
- Expanding automated test coverage
- Adding difficulty levels or timed questions
- Supporting custom question sets

If you contribute, keep the codebase aligned with the existing Node.js 18+ and ES Modules setup.
