# 💵 Python Project: Currency Note Counter

## Project Assignment

Build a Python program that asks the user to enter an amount and calculates how many notes of each denomination are needed.

The program should work with these note denominations:

- 500 Dollar Note
- 100 Dollar Note
- 50 Dollar Note
- 20 Dollar Note
- 10 Dollar Note

After calculating the available notes, the program should display the amount that remains.

---

# Step 1: Take the Amount

Ask the user to enter an amount.

Use `input()` and convert the input into an integer using `int()`.

Store the amount in a variable named:

```python
amount
```

---

# Step 2: Calculate the Number of 500 Notes

Use integer division:

```python
amount // 500
```

Store the result in:

```python
note500
```

Display:

```text
500 Dollar Note: [number of notes]
```

Then update the remaining amount using:

```python
amount %= 500
```

This keeps only the amount that could not be represented using 500-value notes.

---

# Step 3: Calculate the Number of 100 Notes

Use:

```python
amount // 100
```

Store the result in:

```python
note100
```

Display:

```text
100 Dollar Note: [number of notes]
```

Then update the remaining amount using:

```python
amount %= 100
```

---

# Step 4: Calculate the Number of 50 Notes

Use:

```python
amount // 50
```

Store the result in:

```python
note50
```

Display:

```text
50 Dollar Note: [number of notes]
```

Then update the remaining amount using:

```python
amount %= 50
```

---

# Step 5: Calculate the Number of 20 Notes

Use:

```python
amount // 20
```

Store the result in:

```python
note20
```

Display:

```text
20 Dollar Note: [number of notes]
```

Then update the remaining amount using:

```python
amount %= 20
```

---

# Step 6: Calculate the Number of 10 Notes

Use:

```python
amount // 10
```

Store the result in:

```python
note10
```

Display:

```text
10 Dollar Note: [number of notes]
```

Then update the remaining amount using:

```python
amount %= 10
```

---

# Step 7: Display the Remaining Amount

After processing all available note denominations, display:

```text
Remaining amount: [remaining amount]
```

The remaining amount will be the value that cannot be represented using the available notes.

---

# Step 8: Understand Integer Division

The operator:

```python
//
```

performs integer division.

For example:

```text
1250 // 500 = 2
```

This means the amount contains two 500-value notes.

The decimal portion is discarded.

---

# Step 9: Understand Modulus

The operator:

```python
%
```

returns the remainder.

For example:

```text
1250 % 500 = 250
```

After using two 500-value notes, 250 remains.

In the project, the shorthand:

```python
amount %= 500
```

means:

```python
amount = amount % 500
```

---

# Step 10: Understand the Complete Calculation Flow

The program should process the amount in this order:

```text
Original Amount
      ↓
500 Notes
      ↓
Remaining Amount
      ↓
100 Notes
      ↓
Remaining Amount
      ↓
50 Notes
      ↓
Remaining Amount
      ↓
20 Notes
      ↓
Remaining Amount
      ↓
10 Notes
      ↓
Final Remaining Amount
```

---

# Sample Input / Output

## Test Case 1

### Sample Input

```text
Enter the amount: 1250
```

### Expected Output

```text
500 Dollar Note: 2
100 Dollar Note: 2
50 Dollar Note: 1
20 Dollar Note: 0
10 Dollar Note: 0
Remaining amount: 0
```

---

## Test Case 2

### Sample Input

```text
Enter the amount: 786
```

### Expected Output

```text
500 Dollar Note: 1
100 Dollar Note: 2
50 Dollar Note: 1
20 Dollar Note: 1
10 Dollar Note: 1
Remaining amount: 6
```

---

## Test Case 3

### Sample Input

```text
Enter the amount: 1000
```

### Expected Output

```text
500 Dollar Note: 2
100 Dollar Note: 0
50 Dollar Note: 0
20 Dollar Note: 0
10 Dollar Note: 0
Remaining amount: 0
```

---

## Test Case 4

### Sample Input

```text
Enter the amount: 95
```

### Expected Output

```text
500 Dollar Note: 0
100 Dollar Note: 0
50 Dollar Note: 1
20 Dollar Note: 2
10 Dollar Note: 0
Remaining amount: 5
```

---

# Test Cases

| Test Case | Input Amount | 500 | 100 | 50 | 20 | 10 | Remaining |
|---|---:|---:|---:|---:|---:|---:|---:|
| 1 | 1250 | 2 | 2 | 1 | 0 | 0 | 0 |
| 2 | 786 | 1 | 2 | 1 | 1 | 1 | 6 |
| 3 | 1000 | 2 | 0 | 0 | 0 | 0 | 0 |
| 4 | 95 | 0 | 0 | 1 | 2 | 0 | 5 |
| 5 | 560 | 1 | 0 | 1 | 0 | 1 | 0 |
| 6 | 37 | 0 | 0 | 0 | 1 | 1 | 7 |

---

# Important Test Case

Test an amount that is smaller than every available note:

```text
Enter the amount: 7
```

Expected result:

```text
500 Dollar Note: 0
100 Dollar Note: 0
50 Dollar Note: 0
20 Dollar Note: 0
10 Dollar Note: 0
Remaining amount: 7
```

This confirms that the program correctly handles an amount that cannot be represented using the available denominations.

---

# Concepts Practiced

By completing this project, you will practice:

- `input()`
- `int()`
- Variables
- `print()`
- Integer division `//`
- Modulus `%`
- Assignment operators
- Remainders
- Sequential calculations
- Updating variable values
- Basic problem-solving with arithmetic

---

# Testing Checklist

Before submitting, verify:

- [ ] The program asks for the amount.
- [ ] The input is converted to an integer.
- [ ] The number of 500 notes is calculated correctly.
- [ ] The remaining amount is updated correctly.
- [ ] The number of 100 notes is calculated correctly.
- [ ] The number of 50 notes is calculated correctly.
- [ ] The number of 20 notes is calculated correctly.
- [ ] The number of 10 notes is calculated correctly.
- [ ] The final remaining amount is displayed.
- [ ] Multiple test cases have been tested.
- [ ] An amount smaller than 10 has been tested.

---

# Submission Requirements

### Python File

```text
currency_note_counter.py
```

### Screenshot

Provide a screenshot showing:

- The entered amount.
- The number of each note.
- The final remaining amount.

---

# Code Quality Requirements

Before submitting:

- [ ] Use meaningful variable names.
- [ ] Keep the calculations in the correct denomination order.
- [ ] Use `//` for finding the number of notes.
- [ ] Use `%` to calculate the remaining amount.
- [ ] Keep the output labels clear.
- [ ] Use proper indentation.
- [ ] Test the program with different amounts.

---

# Learning Objectives

After completing this project, you should understand:

- How integer division works.
- How the modulus operator works.
- How to calculate remainders.
- How to update a variable using `%=` and other assignment operators.
- How to break a larger calculation into sequential steps.
- How to use arithmetic operators to solve a real-world style problem.
- How to test a Python program using different inputs.
