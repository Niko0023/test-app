# quiz-cli

## 📋 Project Description
`quiz-cli` is an interactive command-line quiz game designed to help users learn JavaScript in a fun, engaging way.

- **What it does:** Presents quiz questions in the terminal, lets the user choose a category and number of questions, collects answers, and displays the final results.
- **Main purpose and goals:** Provide a lightweight educational CLI experience for practicing JavaScript knowledge.
- **Target audience:** Beginners learning JavaScript, students, and developers who enjoy terminal-based games and quizzes.

## 🚀 Setup Instructions

### Prerequisites
- **Node.js 18.0.0 or higher**
- A terminal/shell environment

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Niko0023/test-app.git
   ```
2. Go to the project directory:
   ```bash
   cd test-app
   ```
3. Install dependencies:
   ```bash
   npm install
   ```

> This project currently has no declared external dependencies, but running `npm install` will still prepare the project environment and generate a lockfile if needed.

### Environment Variables
- No environment variables are currently required.

## ▶️ How to Run the Project

### Development / Local Run
Start the application with:

```bash
npm start
```

This runs:

```bash
node index.js
```

### Test Run
Run the test suite with:

```bash
npm test
```

This executes:

```bash
node --test
```

### Production Use
Since this is a CLI application, “production” usage is the same as running the main entry point:

```bash
node index.js
```

### Docker
- No Docker configuration is currently provided.

## ✨ Key Features
- Interactive command-line quiz experience
- JavaScript learning focus
- Category selection
- Configurable number of questions
- Step-by-step question flow with answer collection
- Score/result display at the end of the quiz
- Option to play again
- Clean error handling for a smoother terminal experience
- ESM-based CLI entry point with executable shebang support

## 📁 Project Structure

```text
.
├── index.js
├── package.json
└── (referenced but not currently shown in repository listing)
    ├── src/
    │   ├── input.js
    │   ├── quiz.js
    │   └── colors.js
    └── data/
        └── questions.json
```

### Structure Notes
- **`index.js`**: Main CLI entry point. Coordinates the app flow.
- **`package.json`**: Project metadata, scripts, module type, and Node version requirement.
- **`src/`**: Referenced by the entry point for input handling, quiz logic, and terminal colors.
- **`data/questions.json`**: Referenced as the quiz question source.

## 🛠️ Technologies Used
- **Node.js**
- **JavaScript (ES Modules)**
- **`fs/promises`** for file access
- **`url`** and **`path`** for module/file path handling
- **Node’s built-in test runner** (`node --test`)

## 📝 License
This project is licensed under the **MIT License**.