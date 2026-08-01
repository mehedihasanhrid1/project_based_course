# 📘 Python Assignment: Exam Eligibility Checker

## 🎯 Objective

Write a Python program to determine whether a student is eligible to sit for the examination based on their attendance percentage and medical condition.

---

## 📝 Problem Statement

A school has the following attendance policy for exam eligibility:

- Students **with a medical cause** must have **at least 60% attendance**.
- Students **without a medical cause** must have **at least 75% attendance**.

Create a Python program that:

1. Asks the user if they have a medical cause (`yes` or `no`).
2. Asks the user to enter their attendance percentage.
3. Determines whether the student is eligible for the exam.
4. Displays an error message if the medical cause input is invalid.

---

## 📋 Requirements

Your program must:

- Use `input()` to take user input.
- Convert the medical cause input to lowercase using `.lower()`.
- Use `if`, `elif`, and `else` statements.
- Use nested `if` statements where appropriate.
- Display the correct eligibility message.

---

## 📥 Sample Runs

### Example 1

**Input**
```text
Do you have medical cause? (yes/no): yes
Enter your attendance percentage: 70
```

**Output**
```text
You are eligible for the exam.
```

---

### Example 2

**Input**
```text
Do you have medical cause? (yes/no): yes
Enter your attendance percentage: 55
```

**Output**
```text
You are not eligible for the exam.
```

---

### Example 3

**Input**
```text
Do you have medical cause? (yes/no): no
Enter your attendance percentage: 80
```

**Output**
```text
You are eligible for the exam.
```

---

### Example 4

**Input**
```text
Do you have medical cause? (yes/no): no
Enter your attendance percentage: 70
```

**Output**
```text
You are not eligible for the exam.
```

---

### Example 5

**Input**
```text
Do you have medical cause? (yes/no): maybe
```

**Output**
```text
Invalid input!
```

---

## 💡 Hints

- Store the medical cause in a variable.
- Use `.lower()` to ignore uppercase and lowercase differences.
- Convert the attendance percentage to an integer using `int()`.
- Use nested `if` statements to check the attendance requirement based on the medical cause.

---

## ⭐ Bonus Challenge

Improve your program by validating the attendance percentage.

If the attendance entered is less than **0** or greater than **100**, display:

```text
Invalid attendance percentage!
```

instead of checking exam eligibility.

---

## 📚 Concepts Covered

- Variables
- User Input
- Type Casting (`int()`)
- String Methods (`lower()`)
- Conditional Statements (`if`, `elif`, `else`)
- Nested `if` Statements
- Comparison Operators
- Input Validation