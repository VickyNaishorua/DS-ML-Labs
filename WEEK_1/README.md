# Lab 1: Python Fundamentals - Variables and Data Types

## Objective
To understand how data is stored and categorized in Python, specifically focusing on variable assignment and the primary built-in data types (Numeric, Sequence, Mapping).

## Tools Used
- Python 3
-  Jupyter Notebook 
- Git & GitHub
- postimg.cc

## Step-by-Step Process
1. **Variable Assignment:** Created labels to store integers and strings in memory.
2. **Numeric Exploration:** Identified the differences between `int`, `float`, and `complex` numbers.
3. **Collection Handling:** Created ordered sequences (Lists,Tuples,Range) and practiced accessing data via keys in Mappings (Dictionaries).
4. **Type Verification:** Used the `type()` function to confirm the class of various objects.

## Commands Executed
Below are the core snippets tested during this lab:

```python
# Numeric Types
x = 2        # int
y = 3.14     # float
z = 2 + 3j   # complex

# Sequence Types
list_ = [1, 2, 3, 4, 5]
tuple_ = (1, 2, 3, 4, 5)
range_ = range(1,5)

# Mapping (Dictionary)
Kenya = {'Riftvalley':'Narok', 'Western':'KisumuDala'}
print(Kenya['Western'])

```

## Screenshots of Results
- **Variables Output:** ![Variables Output](https://i.postimg.cc/dQkcRRVX/variables-output.png)
- **Types Output:** ![Types Output](https://i.postimg.cc/Y980162m/data-types-output.png)

## Key Observations / Lessons Learned
- **Mutability:** Lists can be changed after creation, while tuples are immutable.  
- **Key-Value Logic:** Dictionaries (Mappings) are highly efficient for looking up data without needing to know the index.  
- **Naming Conventions:** Used underscores (e.g., `list_`) to avoid shadowing Python's built-in function names.
- Python code can be enclosed in triple backticks for execution, and closing the block allows normal text to resume.


