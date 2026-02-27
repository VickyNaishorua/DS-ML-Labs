# Python Operators & Strings

## Objective
The objective of this lab is to:
1. Understand and implement Python operators
2. Practice arithmetic, logical, bitwise, and string operations
3. Learn how binary operations work internally
4. Strengthen foundational Python programming skills

## Tools Used
- Python 3
- Jupyter Notebook 
- Git & GitHub
- postimg.cc

## Step-by-Step Process
1. Implemented arithmetic operators with sample variables.
2. Tested comparison and logical operators.
3. Practiced assignment operators.
4. Experimented with bitwise operators and converted binary to decimal.
5. Applied string methods for manipulation.
6. Documented outputs and captured screenshots.

## Commands Executed
Below are the core snippets tested during this lab:

**Arithmetic Operators**

Arithmetic operators in Python are used to perform mathematical computations on numeric data types and include addition (+), subtraction (-), multiplication (*), division (/), floor division (//), modulus (%), and exponentiation (**).

 Example:
 ```python
    x = 10
    y = 15
    print(x + y)
```
### Screenshot of result
![Arithmetic Operators Output](https://i.postimg.cc/Y9HDLj4t/arithmetic-operators.png)


**Comparison operators**

Comparison operators evaluate relationships between two values and return a Boolean output. The common operators are greater than (>), less than (<), equal to (==), not equal to (!=), greater than or equal to (>=), and less than or equal to (<=).

Example:
```python
    x = 20
    y = 7
    print(x>y)
```
### Screenshot of result
![Comparison Operators Output](https://i.postimg.cc/kXqVYCbz/comparison-operators.png)


**Logical operators**

Logical operators are used to combine conditional expressions in Python. The operators include and, or, and not, and they return True or False depending on whether the combined conditions satisfy the logical requirement.

Example:
```python
    print(x > 5 and y < 5)
```
### Screenshot of result
![Logical Operators Output](https://i.postimg.cc/GtJj0jzk/logical-operators.png)

**Assignment operators**

Assignment operators are used to assign values to variables while performing an operation at the same time. These operators include **+=, -=, *=, /=, //=, %=, and =, which modify the variable’s value and store the updated result.

Example:
```python
    x = 10
    x += 1
```
### Screenshot of result
![Assignment Operators Output](https://i.postimg.cc/Kcwf1J1h/assignment-operators.png)

**Bitwise operators**

Bitwise operators operate directly on the binary representation of integers. 
- AND (&) operator returns 1 only if both bits are 1
-  OR (|) operator returns 1 if at least one bit is 1
-  XOR (^) operator returns 1 only if the bits are different.
-  NOT (~) operator flips all bits and follows the formula ~x = -(x + 1) in Python.
-  Right Shift (>>) operator shifts bits to the right, effectively dividing the number by powers of 2
-  Left Shift (<<) operator shifts bits to the left, multiplying the number by powers of 2.

Example:
```python
    x = 10
    y = 3
    print(x & y)
```
### Screenshot of result
![Bitwise Operators Output](https://i.postimg.cc/Jnky1P88/bitwise-operators1.png)
![Bitwise Operators Output](https://i.postimg.cc/zfLvj0V7/bitwise-operators2.png)

**Membership Operators**

Checks whether a value exists in a collection:
- in
- not in

Example:
```python
    a = [1,2,3,4,5]
    print(2 in a)
```
### Screenshot of result
![Membership Operators Output](https://i.postimg.cc/CxsX2gfY/membership-operators.png)

**Identity Operators**

Checks whether two variables refer to the same object in memory:
- is
- is not

Example:
```python
    a = [1,2,3]
    b = [1,2,3]
    print(a is b)
```
### Screenshot of result
![Identity Operators Output](https://i.postimg.cc/Wzmw42vB/identity-operators.png)

**String methods**

String methods in Python are used to modify, check, and process text data. I practiced commonly used methods such as; 
- .upper() and .lower() for changing case
- .isalpha() and .isdigit() for validation checks
- .split() and .join() for text manipulation
- .replace() for modifying content
- .startswith() and .endswith() for checking string patterns.

Example
```python
    name = "ParoCyber LLC"
    print(name.upper())
```
### Screenshot of result
![Strings Operators Output](https://i.postimg.cc/d11bdx3v/strings-controlflow1.png)
![Strings Operators Output](https://i.postimg.cc/SNrHT49R/strings-controlflow2.png)
![Strings Operators Output](https://i.postimg.cc/022VNwzF/strings-controlflow3.png)

**Key Observations / Lessons Learned**
- Operators perform different types of calculations on data.
- Bitwise operators manipulate binary values directly.
- Binary numbers use powers of 2 for conversion.
- Strings are immutable but have powerful built-in methods.
- Documentation improves understanding and portfolio quality.

**Conclusion**

This lab strengthened my understanding of Python operators and improved my ability to document technical work professionally using GitHub.


