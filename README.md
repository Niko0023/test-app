# quiz-cli

## 📋 Project Description
- **quiz-cli** is an interactive command-line quiz game for learning JavaScript.
- It provides a terminal-based quiz flow with a welcome banner, category selection, question count selection, timed/iterative question prompts, result summary, and a replay option.
- This project is aimed at developers, learners, and anyone who wants a lightweight, educational CLI experience for practicing JavaScript knowledge.

## 🚀 Setup Instructions
### Prerequisites
- **Node.js 18.0.0 or newer**
- A terminal capable of running interactive CLI apps

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Niko0023/test-app.git
   cd test-app
   ```
2. Install project metadata and prepare the Node environment:
   ```bash
   npm install
   ```
   > There are no external dependencies declared, so this step mainly ensures the project is initialized locally.

### Environment Variables
- No environment variables are required for the current project setup.

## ▶️ How to Run the Project
### Development Mode
Run the quiz directly with Node:
```bash
node index.js
```

### Production Mode
Use the provided start script:
```bash
npm start
```

### Tests
Run the built-in Node test runner:
```bash
npm test
```

### Docker
- Docker support is not included in the repository.

## ✨ Key Features
- Interactive terminal quiz experience
- JavaScript learning focus
- Category selection before starting the quiz
- Selectable number of questions
- Question/answer flow in the CLI
- Results summary at the end of the quiz
- “Play again” prompt for repeated practice
- Graceful error handling and clean shutdown
- Uses modern ES Modules and Node.js built-in APIs

## 📁 Project Structure
Current repository contents:
```text
quiz-cli/
├── index.js
├── package.json
└── .DS_Store
```

Referenced by the entry file but not present in the repository readout:
```text
quiz-cli/
├── src/
│   ├── input.js
│   ├── quiz.js
│   └── colors.js
└── data/
    └── questions.json
```

### Notes on Structure
- `index.js` is the CLI entry point and executable script.
- `src/` is expected to contain the quiz logic, input handling, and terminal colors utilities.
- `data/questions.json` is expected to store the quiz question bank.

## 🛠️ Technologies Used
- **Node.js**
- **ES Modules**
- **Built-in Node APIs**
  - `fs/promises`
  - `path`
  - `url`
- **CLI / Terminal application**
- **JSON** for quiz data storage

## 📝 License
- Licensed under the **MIT License**.
