
# Python Data Structures 

## Objective
This README provides an overview of the most common Python data structures: **Lists, Tuples, and Dictionaries**, along with their commonly used methods and examples.

## Tools Used
- Python 3
- Jupyter Notebook 
- Git & GitHub
- Postimg.cc

## Step-by-Step Process
1. Created examples of lists, tuples, and dictionaries in a Jupyter Notebook.
2. Applied common methods to manipulate and access data.
3. Demonstrated indexing for sequences (lists/tuples) and key access for dictionaries.
4. Troubleshot and resolved errors encountered during execution.
5. Ran all cells to verify correct outputs.
6. Captured screenshots of the results and uploaded them via postimg.cc, with links attached in the screenshots section.
7. Added explanations using Markdown headings and captions.

## Commands Executed
Below are the core snippets tested during this lab:

## 1. Lists

Lists are **ordered collections** of items in Python. They are **mutable**, meaning their elements can be modified after creation.  

### Creating a List
```python
my_list = [1, 2, 3, 4, 5]
```

### Lists can also be created using the list() constructor:
```python
my_list = list([1, 2, 3, 4, 5])
```

## Common List Methods

append() – Adds an element to the end of the list
```python
my_list.append(6)
print(my_list)  # [1, 2, 3, 4, 5, 6]
```
## Screenshot of result
![List append Output](https://i.postimg.cc/KYTm5dFg/list-append.png)

extend() – Adds multiple elements from another list
```python
my_list.extend([7, 8, 9, 10])
print(my_list)  # [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
## Screenshot of result
![List extend Output](https://i.postimg.cc/J4y7nygd/list-extend.png)


insert() – Inserts an element at a specific position
```python
my_list.insert(1, 1)
print(my_list)  # [1, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
## Screenshot of result
![List insert Output](https://i.postimg.cc/hPGgYJcm/list-insert.png)

remove() – Removes the first occurrence of a value
```python
my_list.remove(1)
print(my_list)  # [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
## Screenshot of result
![List remove Output](https://i.postimg.cc/G2rnxtqS/list-remove.png)

pop() – Removes and returns an element at a given index (default: last element)
```python
popped_element = my_list.pop(5)
print(popped_element)  # 6
print(my_list)         # [1, 2, 3, 4, 5, 7, 8, 9, 10]
```
## Screenshot of result
![List pop Output](https://i.postimg.cc/rsZ6TJMd/list-pop.png)

index() – Returns the index of the first occurrence of a value
```python
index = my_list.index(10)
print(index)  # 8
```
## Screenshot of result
![List index Output](https://i.postimg.cc/LsKcmhKx/list-index.png)

count() – Returns the number of occurrences of a value
```python
count = my_list.count(9)
print(count)  # 1
```
## Screenshot of result
![List count Output](https://i.postimg.cc/zBp6wjLt/list-count.png)

sort() – Sorts the list in ascending order
```python
my_list.sort()
print(my_list)  # [1, 2, 3, 4, 5, 7, 8, 9, 10]
```
## Screenshot of result
![List sort Output](https://i.postimg.cc/0ym4XxMv/list-sort.png)

reverse() – Reverses the order of elements
```python
my_list.reverse()
print(my_list)  # [10, 9, 8, 7, 5, 4, 3, 2, 1]
```
## Screenshot of result
![List reverse Output](https://i.postimg.cc/Ls3bRTVK/list-reverse.png)

## 2. Tuples

Tuples are similar to lists but are immutable — their elements cannot be changed after creation.

### Creating a Tuple
```python
my_tuple = ('milk', 'sugar', 'cinnamon', 'oats', 'sugar')
```

### Tuple Methods

count() – Returns how many times a value appears
```python
count = my_tuple.count('sugar')
print(count)  # 2
```

index() – Returns the index of the first occurrence of a value
```python
index = my_tuple.index('oats')
```
Indexing – Access an element using its position
```python
print(my_tuple[2])  # cinnamon
```

## Screenshot of result
![Tuple Output](https://i.postimg.cc/prpGftMn/tuple-output.png)


## 3. Dictionaries

Dictionaries are unordered collections of key-value pairs. They are mutable and useful for storing data with unique keys.

## Creating a Dictionary
```python
my_dict = {'name':'Vicky','age':29,'city':'Nairobi'}
# or using constructor
my_dict = dict(name='Vicky', age=29, city='Nairobi')
```
### Dictionary Methods

get() – Returns the value for a specified key
```python
age = my_dict.get('age')
print(age)  # 29
```

Indexing – Access value using the key
```python
age = my_dict['age']
print(age)  # 29
```

items() – Returns key-value pairs
```python
items = my_dict.items()
print(items)  # dict_items([('name', 'Vicky'), ('age', 29), ('city', 'Nairobi')])
```

keys() – Returns all keys
```python
keys = my_dict.keys()
print(keys)  # dict_keys(['name', 'age', 'city'])
```
## Screenshot of result
![Dictionary Output](https://i.postimg.cc/WpHf2t0m/dictionary-output.png)

values() – Returns all values
```python
values = my_dict.values()
print(values)  # dict_values(['Vicky', 29, 'Nairobi'])
```

update() – Updates the dictionary with new key-value pairs
```python
my_dict.update({'age':30, 'gender':'female', 'country':'Kenya'})
print(my_dict)
# {'name': 'Vicky', 'age': 30, 'city': 'Nairobi', 'gender': 'female', 'country': 'Kenya'}
```
## Screenshot of result
![Values Output](https://i.postimg.cc/nh8RD5RF/values-output.png)

## Key Observations / Lessons Learned
- Lists are mutable and versatile: can store, modify, add, and remove items.
- Tuples are immutable: elements cannot change; good for constant data.
- Dictionaries provide key-value mapping: access values via keys, not positions.
- Indexing differences: Lists/Tuples use numeric indexes; dictionaries use keys.
- Notebook presentation: Use headings, code blocks, and relative paths for screenshots to ensure clarity on GitHub.
