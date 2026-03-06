## Python Control Flow, Functions & Pandas Basics 

### Objective

The objective of this lab is to practice Python fundamentals such as string formatting, control flow, loops, and built-in functions, and to learn basic data manipulation using the Pandas library.

## Tools Used
- Python 3
- Jupyter Notebook 
- Git & GitHub
- postimg.cc

## Step-by-Step Process

1. String Formatting

Learned how to combine variables with text output.

Methods used:

- String concatenation : combining multiple strings into one using the `+` operator.

Example:
```python
  name = "Vicky"
    age = 30
    print("Hello, my name is "+ name + " and I am " + str(age) + " years old.") 
```

- F-strings : provide a more concise and readable way to format strings by embedding expressions directly within them.

Example:
```python
    name = "Vicky"
    age = 30
    print(f"Hello, my name is {name} and I am {age} years old.") 
```

- .format() method : allows for more complex string formatting by using placeholders and format specifiers.
Example:
```python
    name = "Vicky"
    age = 30
    print("Hello, my name is {} and I am {} years old.".format(name,age))
```

### Screenshot of result
![String Formatting  Output](https://i.postimg.cc/Y2z63tFG/s-formating-output.png)

2. Control Flow Statements

Control flow allows programs to make decisions based on conditions.

- If Statement : allows you to execute code conditionally based on the evaluation of an expression

Example:
``` python
    x = 10
    if x > 0 and x % 2 == 0:
    print("x is an even number")
```

- If-Else Statements : allows you to execute different code blocks based on the evaluation of a condition

Example:

``` python
x = int(input("Enter a number: "))
if x > 0 and x % 2 == 0:
    print("x is an even number")
else:
    print("x is an odd number")
```

- Nested If Statement : an if statement inside another if statement.The second condition is checked only if the first condition is true.

Example:
``` python
age = 14
if age >= 18:
    if age < 21:
        print('You are an adult, but not yet allowed to drink')
    else:
        print("You are an adult and allowed to drink")
else:
    print("You are underage")
```

### Screenshot of result
![If Statement Output](https://i.postimg.cc/j5sF8ZMv/ifstaement-output.png)

- If–Elif–Else : allows you to test multiple conditions sequentially and execute the corresponding code block of the first true condition.

Example:

```python
age = 23
if age >= 18 and age < 21:
    print('You are an adult but not allowed to drink yet')
elif age >= 18 and age >=21:
    print("You are an adult and allowed to drink")
else:
    print("you are underage")
```

### Screenshot of result
![If-else Statement Output](https://i.postimg.cc/cJ1zhF95/ifelse-output.png)

3. Loops
- For Loops

For loops are used to iterate over a sequence (such as a list, tuple, or string) and execute a block of code for each element in the sequence.

Example:

```python
list_=['apple','banana','orange','mango']
for item in list_:
    print(item)
```

### Screenshot of result
![For Loop Output](https://i.postimg.cc/Y9vMnrnd/forloop-output.png)

- While Loops

While loops repeatedly execute a block of code as long as a specified condition is True.

Example:

```python
i = 1
while i <= 5:
    print(i)
    i += 1
```

### Screenshot of result
![While Loop Output](https://i.postimg.cc/8zGvq9Vj/whileloop-output.png)


4. Lambda Functions
Lambda functions are anonymous (short) functions used for simple operations.

Example: Sorting a list of dictionaries by score.

```python
students = [
    {"name": "Natalie", "score": 87},
    {"name": "Zacharia", "score": 90}
]

sorted_students = sorted(students, key=lambda x: x["score"])
print(sorted_students)
```

Descending order:
```python
students = [
    {"name": "Natalie", "score": 87},
    {"name": "Zacharia", "score": 90}
]

sorted_students = sorted(students,key=lambda x: x['score'], reverse=True)
print(sorted_students)
```

### Screenshot of result
![Lambda Output](https://i.postimg.cc/Ls9yjRmZ/lambda-output.png)

5. Built-in Functions
Python provides powerful built-in functions to simplify tasks.

- map() : Applies a function to every element in an iterable.

Example:

```python
numbers = [1,2,3,4,5]

squared = map(lambda x: x**2, numbers)

print(list(squared))
```

- filter() : Filters elements based on a condition.

Example:

```python
numbers = [1,2,3,4,5]

evens = filter(lambda x: x % 2 == 0, numbers)

print(list(evens))
```

- reduce() : Reduces a list to a single value.

Example:

```python
from functools import reduce

numbers = [1,2,3,4,5]

product = reduce(lambda x,y: x*y, numbers)

print(product)
```

- sum()
```python
numbers = [1,2,3,4,5]
print(sum(numbers))
```

- max()

```python
numbers = [1,2,3,4,5]
print(max(numbers))
```

- min()
```python
numbers = [1,2,3,4,5]
print(min(numbers))
```
### Screenshot of result
![Map Output](https://i.postimg.cc/9F8mTXd6/map-output.png)
![Max Output](https://i.postimg.cc/rmnnjHfV/max-output.png)



### Introduction to Pandas
Pandas is a Python library used for data manipulation and analysis.
It provides powerful data structures like Series and DataFrames.

##### Pandas Data Structures

Series

A Series is a one-dimensional labeled array.

```python
import pandas as pd

data = [1,2,3,"Angel",4,5]

s = pd.Series(data)

print(s)
```

DataFrame

A DataFrame is a two-dimensional table with rows and columns.

```python
import pandas as pd

data = {
    "Name": ["John", "Alice", "Bob"],
    "Age": [30,25,35],
    "City": ["New York", "Paris", "London"]
}

df = pd.DataFrame(data)

print(df)
```

### Screenshot of result
![Dataframe Output](https://i.postimg.cc/kXz5zX2K/dataframe-output.png)

Data Manipulation

Indexing and Slicing: You can access and manipulate data in Series and DataFrame using indexing and slicing.

```python
s = pd.Series([1, 2, 3, 4, 5])
# Accessing elements in a Series
print(s[3])
```
### Screenshot of result
![Data Manipulation Output](https://i.postimg.cc/VNV1rKXM/datamanipulation-output.png)

Data Combination in Pandas

DataFrames can be combined using:

**concatenation**

- Vertical Concatenation

```python
df_1 = pd.DataFrame({'A':[4,2,6],'B':['m','n','o']})
df_2 = pd.DataFrame({'A':[45,8,9],'B':['x','y','z']})

vertical = pd.concat([df_1, df_2], axis=0)
```
### Screenshot of result
![VerticalConcat Output](https://i.postimg.cc/pdNJWH68/concat-output.png)

Horizontal Concatenation

```python
horizontal_com = pd.concat([df_1, df_2], axis=1, keys=["df_1","df_2"])
horizontal_com
```
### Screenshot of result
![HorizontalConcat Output](https://i.postimg.cc/jjgNWY8J/Horizontal-output.png)

Example with Weather Data
```python
accra = pd.DataFrame({
    "Town":["Circle","Madina","East Legon"],
    "Humidity":[32,29,34],
    "Temperature":[28,30,25]
})

kumasi = pd.DataFrame({
    "Town":["Kejetia","Amakom","Mantia"],
    "Humidity":[27,39,36],
    "Temperature":[30,26,24]
})

df_3 = pd.concat([accra, kumasi], ignore_index=True)
```

### Screenshot of result
![Weather Output](https://i.postimg.cc/FRNqKcBK/weather-output.png)


### Key Takeaways

- Python offers multiple ways to format strings such as concatenation, f-strings, and .format().
- Control flow statements allow programs to make logical decisions.
- Loops enable repeated execution of code.
- Lambda functions simplify short operations.
- Built-in functions like map(), filter(), and reduce() provide efficient data processing.
- Pandas is essential for data analysis and data manipulation.
- DataFrames can be combined using concat() vertically or horizontally.

