# Python Dictionaries

## Introduction

Dictionary is a highly versatile built-in datatype provided by Python. It is used to stored data in a key-value fashion. Dictionaries are created by storing key-value pairs inside braces {}. Dictionaries used to be unordered till Python 3.6, however, from Python 3.7, they are ordered. We will be considering dictionaries as unordered as this new feature needs to be more explored.

### Dictionary Example

```python
student = {"name": "Sam", "age": 18, "hobbies": ["basketball", "football"]}
print(student)
```

```
{'name': 'Sam', 'age': 18, 'hobbies': ['basketball', 'football']}
```

Unlike lists, dictionaries are indexed by keys. Consider dictionaries similar to array, where you can access any location of the array in O(1) time complexity. This is because dictionaries use hash table to store values. The only key difference between array and dictionary is, elements of arrays can be retrieved by providing index location, whereas, values in dictionary are accessed using the key. Since the values are accessed using keys, the keys must be unique.

```python
print(student["age"])
```

```
18
```

Dictionary keys are immutable, i.e., they must be hashable. Mostly numbers and strings are used as a key, however you can use a tuple. Only thing you have to remember while using a tuple as key, is that you can only have string, number or another tuple inside it.

```python
food = {["apple"]: "tasty"}
```

```
TypeError: unhashable type: 'list'
```

```python
food = {(1,2): "mango"}
food[(1,2)]
```

```
'mango'
```

## Dictionary Methods

### get()

Returns value for key if key is in the dictionary, else default.

```python
student.get('name')
```

```
'Sam'
```

### items()

Set like object to see contents of the dictionary.

```python
student.items()
```
```
dict_items([('name', 'Sam'), ('age', 18), ('hobbies', ['basketball', 'football'])])
```

```python
for item in student.items():
    print(item)
```

```
('name', 'Sam')
('age', 18)
('hobbies', ['basketball', 'football'])
```

### clear()

Clears contents of the dictionary

```python
food.clear()
print(food)
```

```
{}
```

### pop()

Removes specified key and returns the corresponding value. If key is not found, default is returned if given, otherwise KeyError is raised.

```python
hobbies = student.pop("hobbies")
print("hobbies: ",hobbies)
print("student: ", student)
```

```
hobbies:  ['basketball', 'football']
student:  {'name': 'Sam', 'age': 18}
```
### update()

Updates value for the given key. If key is not present, then a new key-value pair is created.

```python
student.update({"name":"bob"})
print(student)
```

```
{'name': 'bob', 'age': 18}
```

```python
student.update({"height":171.0})
print(student)
```

```
{'name': 'bob', 'age': 18, 'height': 171.0}
```

### fromkeys()

Creates a dictionary from the given sequence of keys and values.

```python
# keys
candidate = {'sam', 'bob', 'sara'}
# values
votes = 0

election = dict.fromkeys(candidate, votes)
print(election)
```

```
{'bob': 0, 'sam': 0, 'sara': 0}
```

### values()

As the name specifies, values() will return all the values of the dictionary.

```python
student.values()
```

```
dict_values(['bob', 18, 171.0])
```

### copy()

Creates a shallow copy of a dictionary

```python
people = student.copy()
print(people)
```

```
{'name': 'bob', 'age': 18, 'height': 171.0}
```

