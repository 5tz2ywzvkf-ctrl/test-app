# Quiz CLI

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
![Node.js CI](https://img.shields.io/badge/build-passing-brightgreen)
![Version](https://img.shields.io/badge/version-1.0.0-blue)

---

## Project Overview

**Quiz CLI** is an interactive command-line quiz game designed to help users learn and test their knowledge of JavaScript, Node.js, and general programming concepts. The application demonstrates modern JavaScript (ES Modules), async/await, user input handling, file system operations, and object-oriented programming in a fun and educational way.

### Key Features

- Multiple categories (JavaScript Basics, Node.js Fundamentals, General Programming)
- Randomized questions and answer order
- Progress bar and scoring
- Explanations for each answer
- Play-again loop
- Colorful terminal output (no external dependencies)
- Fully async and modular codebase

---

## Technology Stack

- **Language:** JavaScript (ES2022, ES Modules)
- **Runtime:** Node.js (>=18.0.0)
- **Core dependencies:** None (uses only Node.js built-in modules)
- **Project Structure:** Modular (separate files for input, colors, quiz logic, and questions)

---

## Prerequisites

- **Node.js** version 18 or higher
- A terminal or command prompt that supports ANSI colors (most modern terminals do)

---

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/5tz2ywzvkf-ctrl/test-app.git
   cd test-app
   ```

2. **Install dependencies:**
   - No external dependencies are required, but you may run `npm install` to set up the project for Node.js scripts.

---

## Setup & Running the Quiz

### Start the Quiz

```bash
npm start
```
or
```bash
node index.js
```

You will be greeted with a colorful banner and prompted to select a quiz category and the number of questions.

---

## Usage Example

**Sample Session:**

```
╔══════════════════════════════════════════════════╗
║   📚 QUIZ CLI                                   ║
║   Test your programming knowledge!              ║
╚══════════════════════════════════════════════════╝

Choose a category:

  1. JavaScript Basics
  2. Node.js Fundamentals
  3. General Programming

Your choice (enter number): 1

How many questions?

  1. All questions
  2. 3 questions
  3. 5 questions

Your choice (enter number): 2

[▓▓▓░░░░░░░░░░░░░░░░░░░░░░░░░░░░] 20%
Question 1 of 3

What keyword is used to declare a constant in JavaScript?
  1. var
  2. let
  3. const
  4. define

Your choice (enter number): 3

✓ Correct!
💡 The 'const' keyword declares a block-scoped constant that cannot be reassigned.

...
```

---

## Configuration

- **No environment variables are required.**
- All quiz questions are stored in `data/questions.json`. You can add, remove, or edit categories and questions by modifying this file.

---

## File Structure

```
.
├── index.js                # Main entry point for the CLI app
├── package.json            # Project metadata and scripts
├── data/
│   └── questions.json      # All quiz questions, categories, and explanations
└── src/
    ├── colors.js           # ANSI color utilities for terminal output
    ├── input.js            # User input handling (prompts, selection, confirmation)
    └── quiz.js             # Quiz game logic (class, scoring, progress, results)
```

### File Descriptions

- **index.js**: Orchestrates the CLI flow, handles category and question selection, and manages the game loop.
- **src/colors.js**: Provides color and style functions for terminal output using ANSI codes.
- **src/input.js**: Handles all user input (prompts, selections, confirmations) using Node.js readline.
- **src/quiz.js**: Implements the Quiz class, question randomization, scoring, and result display.
- **data/questions.json**: Contains all categories and questions in a structured JSON format.

---

## Adding/Editing Questions

To add new categories or questions, edit `data/questions.json`. Each category has a `name` and an array of `questions`. Each question includes:

- `question`: The question text
- `options`: An array of possible answers
- `answer`: The index (0-based) of the correct option
- `explanation`: (Optional) Explanation shown after answering

---

## Testing

- **Manual Testing:** Run the app and try all categories and question counts.
- **Automated Testing:** (Not implemented) You can add Node.js test scripts and use the `"test"` script in `package.json` as a starting point.

---

## Deployment

No deployment is required. This is a local CLI tool. Simply clone and run as described above.

---

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes
4. Open a pull request describing your changes

Please ensure all code is modular and well-documented. For new questions, follow the format in `data/questions.json`.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Inspired by common programming quizzes and JavaScript learning resources.
- No external dependencies – 100% Node.js!

---

If you have any questions or suggestions, feel free to open an issue or pull request.
