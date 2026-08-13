# 🧮 Python Project: Simple Calculator

## Project Assignment

Build a simple Python calculator that asks the user for two numbers and performs four basic mathematical operations:

- Addition
- Subtraction
- Multiplication
- Division

The program should display the result of each operation clearly.

---

## Step 1: Take the First Number

Ask the user to enter the first number.

Use `input()` and convert the entered value into an integer using `int()`.

Store the value in:

```python
a
```

---

## Step 2: Take the Second Number

Ask the user to enter the second number.

Convert the input into an integer and store it in:

```python
b
```

---

## Step 3: Perform Addition

Calculate:

```python
a + b
```

Display the result using the label:

```text
Addition:
```

---

## Step 4: Perform Subtraction

Calculate:

```python
a - b
```

Display the result using the label:

```text
Subtraction:
```

---

## Step 5: Perform Multiplication

Calculate:

```python
a * b
```

Display the result using the label:

```text
Multiplication:
```

---

## Step 6: Perform Division

Calculate:

```python
a / b
```

Display the result using the label:

```text
Division:
```

---

# Sample Input / Output

## Test Case 1

### Sample Input

```text
Enter first number: 10
Enter second number: 5
```

### Expected Output

```text
Addition: 15
Subtraction: 5
Multiplication: 50
Division: 2.0
```

---

## Test Case 2

### Sample Input

```text
Enter first number: 20
Enter second number: 4
```

### Expected Output

```text
Addition: 24
Subtraction: 16
Multiplication: 80
Division: 5.0
```

---

## Test Case 3

### Sample Input

```text
Enter first number: 7
Enter second number: 3
```

### Expected Output

```text
Addition: 10
Subtraction: 4
Multiplication: 21
Division: 2.3333333333333335
```

---

# Test Cases

| Test Case | First Number | Second Number | Addition | Subtraction | Multiplication | Division |
|---|---:|---:|---:|---:|---:|---:|
| 1 | 10 | 5 | 15 | 5 | 50 | 2.0 |
| 2 | 20 | 4 | 24 | 16 | 80 | 5.0 |
| 3 | 7 | 3 | 10 | 4 | 21 | 2.333... |
| 4 | 8 | 2 | 10 | 6 | 16 | 4.0 |
| 5 | 15 | 3 | 18 | 12 | 45 | 5.0 |

---

# Important Test Case

Test the program with:

```text
Enter first number: 10
Enter second number: 0
```

Observe what happens when the program tries to divide by zero.

For this version of the project, simply observe the behavior. Handling division by zero can be added as an improvement later.

---

# Concepts Practiced

By completing this project, you will practice:

- `input()`
- `int()`
- Variables
- `print()`
- Addition operator `+`
- Subtraction operator `-`
- Multiplication operator `*`
- Division operator `/`
- Basic arithmetic
- Basic Python input and output

---

# Testing Checklist

Before submitting, verify:

- [ ] The program asks for the first number.
- [ ] The program asks for the second number.
- [ ] Both inputs are converted to integers.
- [ ] Addition works correctly.
- [ ] Subtraction works correctly.
- [ ] Multiplication works correctly.
- [ ] Division works correctly.
- [ ] Each result has the correct label.
- [ ] Multiple test cases have been checked.
- [ ] Division by zero behavior has been observed.

---

# Submission Requirements

### Python File

```text
simple_calculator.py
```

### Screenshot

Provide a screenshot showing:

- The two numbers entered.
- Addition result.
- Subtraction result.
- Multiplication result.
- Division result.

---

# Learning Objectives

After completing this project, you should understand:

- How to take user input in Python.
- How to convert input into integers.
- How to store values in variables.
- How to perform basic arithmetic operations.
- How to display calculated results.
- How to test a simple Python program using different inputs.
