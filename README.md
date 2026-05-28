# Quiz CLI

An interactive command-line quiz game for learning JavaScript.

## Overview

Quiz CLI is a Node.js terminal application that lets users:

- choose a quiz category
- choose how many questions to answer
- take the quiz interactively in the terminal
- review their results
- play again

## Project Structure

```text
.
├── index.js
└── package.json
```

## Technologies Used

- **Node.js**
- **JavaScript (ES Modules)**
- **Node built-in `fs/promises` API**
- **Command-line terminal interaction**
- **Async/await**

## Requirements

- Node.js 18 or newer

## Available Scripts

### Start the app

```bash
npm start
```

Runs the quiz CLI.

### Run tests

```bash
npm test
```

Runs Node's built-in test runner.

## Entry Point

The application starts in `index.js`.

It loads quiz questions from:

- `data/questions.json`

And references these local modules:

- `src/input.js`
- `src/quiz.js`
- `src/colors.js`

## Notes

The repository currently contains only the main entry file and package metadata in the visible tree. The entry point references additional source files and data files that are not present in the listed repository contents.

## License

MIT
