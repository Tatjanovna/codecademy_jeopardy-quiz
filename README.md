
# Jeopardy Quiz Game

This project is a Python-based Jeopardy! quiz game that uses a dataset of historical Jeopardy! questions. The game allows users to test their knowledge by answering random Jeopardy! questions. The system checks the user's answers and provides immediate feedback on whether they were correct or incorrect. Additionally, the project includes analysis tools for exploring trends in the dataset, such as how question content has evolved over time.

## Features

- **Random Question Quiz**: The game selects random questions from the Jeopardy! dataset and quizzes the user.
- **Immediate Feedback**: After each question, the user receives feedback on whether their answer was correct or incorrect.
- **Data Analysis**: 
  - Filter questions based on keywords (e.g., "King", "Computer").
  - Compare the number of questions containing certain words across different decades.
  - Compute average "difficulty" based on question value.
  - Count unique answers to specific types of questions.

## Dataset

The Jeopardy! dataset contains historical data on Jeopardy! questions, including the following columns:
- **Show Number**: The number of the episode in which the question appeared.
- **Air Date**: The date the episode aired.
- **Round**: The round of the game (Jeopardy!, Double Jeopardy!, etc.).
- **Category**: The category of the question.
- **Value**: The dollar value of the question.
- **Question**: The question text.
- **Answer**: The correct answer to the question.

## How to Run the Quiz

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/jeopardy-quiz.git
   cd jeopardy-quiz
   ```

2. Ensure you have Python installed. You can use Python 3.6+.

3. Install necessary dependencies (if any, for example, `pandas`):
   ```bash
   pip install pandas
   ```

4. Run the quiz game:
   ```bash
   python jeopardy_quiz.py
   ```

## Example Usage

```bash
Question: This "Mad" magazine artist designed its iconic Alfred E. Neuman character.
Your answer: norman mingo
Correct!

--------------------------------------------------
Question 2 of 5
Question: A sonnet consists of this many lines.
Your answer: 14
Correct!
```

## Analysis Examples

- **Find unique answers to questions containing "King"**:
  ```python
  unique_answers_king = filter_questions_and_count_unique_answers(jeopardy_data, ["King"])
  print(unique_answers_king)
  ```

- **Compare the number of questions containing "Computer" from the 1990s and 2000s**:
  ```python
  count_90s = count_questions_by_word_and_decade(jeopardy_data, "Computer", 1990, 1999)
  count_2000s = count_questions_by_word_and_decade(jeopardy_data, "Computer", 2000, 2009)
  print(f"1990s: {count_90s}, 2000s: {count_2000s}")
  ```

## Future Improvements

- Add difficulty levels based on question value.
- Implement scoring and leaderboard functionality.
- Add a timer for answering questions.
