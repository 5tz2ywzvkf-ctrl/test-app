# Quiz CLI

## Description

**Quiz CLI** is an interactive command-line quiz game designed to help users learn and test their JavaScript programming knowledge. The application demonstrates modern Node.js features such as ES Modules, async/await, file system operations, user input handling, and object-oriented programming concepts. It is ideal for both beginners and experienced developers who want to reinforce their JavaScript skills in a fun and engaging way.

## Features

- Interactive command-line interface (CLI) for a smooth quiz experience
- Multiple quiz categories and question sets (easily extendable)
- Selectable number of questions per session
- Real-time scoring and progress bar
- Detailed results and review of incorrect answers
- Colorful terminal output using ANSI escape codes (no external dependencies)
- Robust error handling and user input validation
- Fully modular, clean, and extensible codebase

## Project Structure

```
quiz-cli/
├── data/
│   └── questions.json        # Quiz questions and categories (JSON format)
├── src/
│   ├── colors.js             # Terminal color utilities
│   ├── input.js              # User input and CLI utilities
│   └── quiz.js               # Core quiz game logic
├── index.js                  # Main entry point for the CLI application
├── package.json              # Project metadata and dependencies
└── README.md                 # Project documentation
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v18.0.0 or higher

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd quiz-cli
   ```

2. **Install dependencies:**
   > No external dependencies are required. All modules used are built-in Node.js modules.

3. **Ensure you have a valid `questions.json` file in the `data/` directory.**
   - The file should be structured with categories and questions (see below for an example).

### Running the Application

Start the quiz game by running:

```bash
npm start
```
or
```bash
node index.js
```

Follow the on-screen prompts to select a quiz category, choose the number of questions, and answer each question. Your score and a review of incorrect answers will be displayed at the end of the quiz.

---

## Example `questions.json` Structure

```json
{
  "categories": {
    "js-basics": {
      "name": "JavaScript Basics",
      "questions": [
        {
          "question": "What is the output of `console.log(typeof null)`?",
          "options": ["'object'", "'null'", "'undefined'", "'number'"],
          "answer": 0,
          "explanation": "In JavaScript, `typeof null` returns 'object' due to legacy reasons."
        }
        // Add more questions here...
      ]
    }
    // Add more categories here...
  }
}
```

---

## Extending the Quiz

- **Add new categories or questions:** Edit the `data/questions.json` file to include more categories and questions.
- **Customize terminal colors or quiz logic:** Modify the files in the `src/` directory for advanced customization.

## License

This project is licensed under the MIT License.

---

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve the quiz or add new features.

---

## Acknowledgments

- Inspired by the need for fun, interactive ways to learn JavaScript.
- Utilizes only Node.js built-in modules for maximum portability.

