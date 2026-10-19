# Day 26: Python Coding Challenge Set – Strings & Tuples

A set of five beginner-friendly Python challenges focused on working with **strings** and **tuples**, using loops, indexing, slicing, and built-in string methods. Part of a daily data analytics learning challenge.

## Files

| File | Description |
|------|-------------|
| `Day26_Coding_Challenge.pdf` | Problem statements for all five challenges |
| `Day-26-Data-analytics-challenge-python.ipynb` | Jupyter Notebook with solutions and outputs |

## Challenges & Solutions

| # | Challenge | Scenario | Input | Output |
|---|-----------|----------|-------|--------|
| 1 | Find Longest Student Name | Find the longest name in a tuple | `("Anu", "Ravikumar", "Jo")` | `Ravikumar` |
| 2 | Join Subjects into Single String | Display subjects in a UI | `("Math", "Science", "English")` | `MathScienceEnglish` |
| 3 | Reverse Each Student Name | Data masking requirement | `("Anu", "Ravi")` | `('unA', 'ivaR')` |
| 4 | Count Vowels in Each Name | Analyze student names | `("Anu", "Ravi", "Sireesha")` | `[2, 2, 4]` |
| 5 | Convert Tuple to Uppercase | Prepare report header | `("python", "sql", "power bi")` | `('PYTHON', 'SQL', 'POWER BI')` |

## Approach

1. **Longest name** – Collect the length of every name in a list, then use `max()` and `.index()` to look up the matching name in the tuple.
2. **Join subjects** – Loop through the tuple and concatenate each item onto an empty string.
3. **Reverse names** – Reverse each string with slicing (`i[::-1]`), store results in a list, and convert back to a tuple (tuples are immutable).
4. **Count vowels** – Use a nested loop; for each name, check every character against a tuple of vowels (upper and lower case) and count matches.
5. **Uppercase** – Apply `.upper()` to each item, collect in a list, then convert back to a tuple.

## Concepts Covered

- Tuple immutability and rebuilding tuples from lists
- Looping over tuples and strings
- String slicing and reversal (`[::-1]`)
- Built-in functions: `len()`, `max()`, `tuple()`
- String methods: `.upper()`, `.append()` on lists, `.index()`
- Membership testing with `in`
- Nested loops

## How to Run

1. Install Python 3.9+ and Jupyter:
   ```bash
   pip install notebook
   ```
2. Launch Jupyter from the project folder:
   ```bash
   jupyter notebook
   ```
3. Open `Day-26-Data-analytics-challenge-python.ipynb` and run the cells in order (**Cell → Run All**).

## Notes & Possible Improvements

- **Challenge 2:** The current output has no separator. Using `", ".join(subjects)` would give a more UI-friendly `Math, Science, English`.
- **Challenge 4:** The notebook adds an extra name (`"Sireesha"`) to the original input for testing. The original input `("Anu", "Ravi")` gives `[2, 2]`. Using `j.lower() in "aeiou"` would simplify the vowel check.
- **Challenge 5:** The title says "Uppercase String" but the solution outputs a tuple. To get a single string, use `", ".join(courses).upper()` → `PYTHON, SQL, POWER BI`.
- **Challenge 1:** Can be shortened to `max(students, key=len)`.
- Several solutions could be written as one-liners with list comprehensions, e.g. `tuple(s[::-1] for s in students)`.

## Environment

- Python 3.9.12
- Jupyter Notebook (ipykernel)
