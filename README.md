# quiz-cli

An interactive command-line quiz game for learning JavaScript and other programming fundamentals.

## Overview

**quiz-cli** is a Node.js terminal application that lets you choose a quiz category, pick how many questions to answer, and then play through an interactive multiple-choice quiz. It uses modern JavaScript features such as ES modules, async/await, and class-based design to provide a simple but polished CLI experience.

The app loads quiz questions from a JSON file, guides the user through category and question-count selection, and then displays a results summary at the end of each round. It is designed to be run directly from the command line.

## Features

- Interactive terminal-based quiz flow
- Category selection from a questions dataset
- Choose between all questions, 3 questions, or 5 questions when available
- Result summary after each quiz round
- Play-again loop for repeated sessions
- ANSI-colored terminal output for a better user experience
- Built with ES modules and modern Node.js APIs

## Requirements

- Node.js **18.0.0** or later
- A terminal that supports standard ANSI escape sequences

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/Niko0023/test-app.git
cd test-app
npm install
```

> This project does not declare any external npm dependencies, but running `npm install` will still create a local lockfile and prepare the project for standard Node.js workflows.

## Usage

### Start the quiz

```bash
npm start
```

Or run the entry file directly:

```bash
node index.js
```

### What you will see

1. A welcome banner in the terminal
2. A category picker
3. A question-count picker
4. One question at a time
5. A final score/results screen
6. A prompt to play again

## Example Interaction

```text
📚 QUIZ CLI
Test your programming knowledge!

Choose a category:
1) JavaScript Basics
2) ...

How many questions?
1) All questions
2) 3 questions
3) 5 questions

Starting quiz...
Select your answer by entering the number.
```

## Configuration

The quiz content is loaded from a JSON file at runtime:

- `data/questions.json`

The entry script reads the file using Node's filesystem API and expects the JSON to contain a `categories` object. Each category should include:

- a display `name`
- a `questions` array

### Expected data shape

```json
{
  "categories": {
    "category-id": {
      "name": "Category Name",
      "questions": [
        {
          "question": "Question text",
          "options": ["A", "B", "C", "D"],
          "answer": 0
        }
      ]
    }
  }
}
```

## Scripts

From `package.json`:

- `npm start` - Runs the quiz application with Node.js
- `npm test` - Executes Node's built-in test runner (`node --test`)

## File Structure

```text
.
├── index.js
├── package.json
├── README.md
└── .DS_Store
```

> Note: The repository snapshot available for analysis only exposes the files above. The runtime imports in `index.js` reference `src/input.js`, `src/quiz.js`, `src/colors.js`, and `data/questions.json`, so those files are expected to exist in the complete project, even though they were not present in the indexed file listing provided here.

## Entry Point

The application entry point is:

- `index.js`

It performs the following tasks:

- loads the quiz data
- displays the banner
- handles category and question-count selection
- runs the quiz loop
- shows results
- prompts to play again

## Dependencies

### Runtime

- No external npm packages are declared in `package.json`
- Uses built-in Node.js modules:
  - `node:fs/promises`
  - `node:url`
  - `node:path`

### Project Imports

The main script imports local modules:

- `./src/input.js`
- `./src/quiz.js`
- `./src/colors.js`

## Implementation Notes

- The project uses the ES module system (`"type": "module"` in `package.json`)
- The application is implemented as a CLI and includes a shebang (`#!/usr/bin/env node`)
- Error handling is centralized in the main async function, which logs the error and exits with a non-zero status code
- The quiz questions are sliced based on the selected question count before being passed into the quiz engine

## Contributing

If you add or restore the missing `src/` and `data/` files, make sure to keep the JSON schema and local imports aligned with `index.js`.

## License

MIT
