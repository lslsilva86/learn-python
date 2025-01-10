## User-Defined Functions in Python

In this lecture, we explored how to create and use **user-defined functions** in Python. These are essential for modularizing code, improving reusability, and simplifying complex problems.

---

#### **1. What are User-Defined Functions?**

- Functions that are created by developers to solve specific problems.
- Help modularize code by breaking it into smaller, reusable pieces.

---

#### **2. Function Syntax**

```python
def function_name(parameters):
    # Function body
    return result  # Optional
```

- **`def`**: Keyword to define a function.
- **Function Name**: Should follow Python naming conventions.
- **Parameters**: Inputs to the function (optional).
- **Return Statement**: Returns a value to the caller (optional).

---

#### **3. Example 1: Sum of Integers from 1 to `n`**

- We defined a function `sum_n(n)` to calculate the sum of integers from 1 to `n` using the formula:
  \[
  \text{Sum} = \frac{n \times (n + 1)}{2}
  \]

**Function Definition**:

```python
def sum_n(n):
    return n * (n + 1) // 2
```

**Usage**:

```python
print(sum_n(10))  # Output: 55
```

---

#### **4. Example 2: Sum of Integers in a Range**

- The function `sum_range(lower_bound, upper_bound)` calculates the sum of integers between two numbers using the `sum_n()` function.

**Logic**:
\[
\text{Sum (range)} = \text{Sum (1 to upper bound)} - \text{Sum (1 to lower bound - 1)}
\]

**Function Definition**:

```python
def sum_range(lower_bound, upper_bound):
    return sum_n(upper_bound) - sum_n(lower_bound - 1)
```

**Usage**:

```python
print(sum_range(5, 10))  # Output: 45
```

---

#### **5. Important Concepts**

- **Input Handling**:
  Use the `input()` function to accept user input, and typecast it to the required type:

  ```python
  n = int(input("Enter a number: "))
  ```

- **Return Values**:
  - Functions in Python always return a value.
  - If no `return` statement is specified, the function returns `None` by default.

**Example**:

```python
def no_return_function():
    pass

print(no_return_function())  # Output: None
```

---

#### **6. Modularization and Reusability**

- By defining **`sum_n()`**, we reused it in **`sum_range()`**, demonstrating how small functions can work together to solve more complex problems.

---

#### **7. Summary of Key Points**

- **Define Functions**: Use the `def` keyword.
- **Arguments**: Pass inputs to functions for flexibility.
- **Return Values**: Use `return` to send data back to the caller.
- **Reusability**: Functions allow code reuse and cleaner design.

---

#### **8. Next Steps**

We will expand on this foundation by exploring:

1. **Default Arguments**: Allowing functions to have optional parameters.
2. **Keyword Arguments**: Specifying arguments by name.
3. **Anonymous Functions**: Using `lambda` expressions for small, inline functions.
4. **Advanced Use Cases**: Such as recursive functions and higher-order functions.
