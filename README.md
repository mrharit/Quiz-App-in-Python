

# 🧠 Quiz App in Python  
### Mini Project 4 (Command-Line)

---

## 📌 Project Overview

The **Quiz App** is a simple command-line Python application that presents multiple‑choice questions, accepts user input (A/B/C/D), checks answers, and displays the final score.

This mini project is perfect for practicing:
- **Control flow** (loops, conditionals)
- **User input handling**
- **Data structures** (lists & dictionaries)

---

## 🎯 Objectives

- Display a set of multiple-choice questions
- Accept user responses in a friendly way (A/B/C/D)
- Validate answers and update the score
- Show a final score summary

---

## 🛠️ Tech Stack

- **Python 3.x**
- Built-in only (no external libraries)

---

## ▶️ How to Run

1. Save the code as `quiz_app.py` (or use your preferred filename).
2. Open a terminal in the same folder.
3. Run:

```bash
python quiz_app.py
````

4.  Type your answer for each question (A/B/C/D) and press **Enter**.

***

## 🧪 Example Run

    Q1: What is the capital of France?
    A) Berlin
    B) Madrid
    C) Paris
    D) Rome
    Your answer(A/B/C/D): c
    Correct!

    Q2: What is 2 + 2?
    A) 3
    B) 4
    C) 5
    D) 6
    Your answer(A/B/C/D): b
    Correct!

    Q3: What is the largest planet in our solar system?
    A) Earth
    B) Jupiter
    C) Saturn
    D) Mars
    Your answer(A/B/C/D): a

    Q4: Who wrote 'Hamlet'?
    A) Charles Dickens
    B) Mark Twain
    C) William Shakespeare
    D) Jane Austen
    Your answer(A/B/C/D): c
    Correct!

    Your final score is 3/4

***

## 🧩 How It Works

*   Questions are stored as a list of dictionaries (each with `question`, `options`, `answer`).
*   The program loops through each question:
    *   Prints the question & options
    *   Takes the user’s input (`A/B/C/D`) and normalizes it to uppercase
    *   Compares the first character of the correct answer (e.g., `"C) ..."` → `"C"`)
*   Tallies the score and prints a final summary.

***

## 🛠️ Customization

### 1) Add or Edit Questions

Append to the `questions` list using the same structure:

```python
{
  "question": "Which language is known as the language of the web?",
  "options": ["A) Python", "B) C++", "C) JavaScript", "D) Java"],
  "answer": "C) JavaScript"
}
```

### 2) Shuffle Questions

To randomize the order:

```python
import random
random.shuffle(questions)
```

### 3) Validate Inputs

You can enforce valid inputs with a simple loop:

```python
while True:
    user_answer = input("Your answer (A/B/C/D): ").strip().upper()
    if user_answer in {"A", "B", "C", "D"}:
        break
    print("Please enter A, B, C, or D.")
```

### 4) Load Questions from JSON (Optional)

Store questions in `questions.json` and load them:

```python
import json
with open("questions.json", "r", encoding="utf-8") as f:
    questions = json.load(f)
```

***

## ✅ Features

*   Clean, beginner-friendly CLI
*   Case-insensitive answers (a/A both work)
*   Easily extensible question bank
*   No external dependencies

***

## 🚀 Future Enhancements

*   Track **percentage score** and **pass/fail** status
*   Show **explanations** for each answer
*   Add a **timer per question** or total time
*   Difficulty levels and **question categories**
*   Persist **high scores** to a file

***

## 📁 Project Structure (Suggested)

    quiz-app/
    ├─ quiz_app.py
    ├─ README.md
    └─ questions.json   # (optional)

***

## 📄 License

This project is intended for **educational and learning purposes**.

***

## 👤 Author

**Aakash Harit**  
Python Mini Projects | Command-Line Applications

***



