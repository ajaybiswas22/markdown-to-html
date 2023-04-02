# Python List

## Introduction

Python provides a wonderful datatype called list. A list can store collection of objects inside it, whether it is a string, boolean, int, or even custom objects. List are denoted by square brackets []. Some of the properties of list are given below.

<ol>
<li> Lists are mutable, i.e., they can be modified.
</li>
<li> Lists are dynamic, i.e., they can expand or contract in size
</li>
<li> Lists are ordered
</li>
<li> Lists can be accessed via index.
</li>
<li> Lists are iterable
</li>
</ol>

Now let us see how can you use lists in your code

### Create a list called fruits

```python
fruits = ['Apple','Mango','Pineapple','Orange','Jackfruit']
print(fruits)
```

```
['Apple', 'Mango', 'Pineapple', 'Orange', 'Jackfruit']
```

### Access first element of a list

```python
print(fruits[0])
```

```
Apple
```

### Access last element of a list

```python
print(fruits[-1])
```

```
Jackfruit
```

### Traverse List using range()

```python
for i in range(len(fruits)):
    print(fruits[i], end=" ")
```

```
Apple Mango Pineapple Orange Jackfruit 
```

### Traverse list element wise

```python
for fruit in fruits:
    print(fruit, end=" ")
```

```
Apple Mango Pineapple Orange Jackfruit 
```

### Copying List

You will be thinking, copying list will be an easy job, but you are wrong. List cannot be copied using assignment operator. When we use assignment operator, we are actually referencing to the list instead of copying it. Following example shows this problem.

```python
A = [10,20,30,40]
B = A
B[0] = 50

print('B = ',B)
print('A = ',A)
```

```
B =  [50, 20, 30, 40]
A =  [50, 20, 30, 40]
```

Let's see id's of both the variables

```python
print('A id = ',id(A))
print('B id = ',id(B))
```

```
A id =  2003427957504
B id =  2003427957504
```

You can see that both of them have same ids. Now let's see how to copy a list.

```python
import copy
A = [10,20,30,40]
B = copy.deepcopy(A)
A = [10,20,30,40]
B[0] = 50

print('A = ', A)
print('B = ',B)

print('A id = ',id(A))
print('B id = ',id(B))
```

```
A =  [10, 20, 30, 40]
B =  [50, 20, 30, 40]
A id =  2003439916736
B id =  2003439917952
```

So let's understand what we did. We used copy library to perform deepcopy. Here, element wise copying happens, which results in creation of a new list. You can perform the same thing using a for loop.

## List Methods

### index

Returns index of first occurance of the element in the list. Raises ValueError if the element is not present.

```python
print(fruits.index('Mango'))
```

```
1
```

### remove

Removes first occurance of the element in the list. Raises ValueError if the element is not present.

```python
fruits.remove('Mango')
print(fruits)
```

```
['Apple', 'Pineapple', 'Orange', 'Jackfruit']
```

### append

The append method is used to add an element to the end of the list.

```python
A.append(5)
print(A)
```

```
[10, 20, 30, 40, 5]
```

### insert

The insert method is used to add an element at the desired position.

```python
# insert 99 at position 0
A.insert(0,99)
print(A)
```

```
[99, 10, 20, 30, 40, 5]
```

### sort

sorts a list in ascending order. The sorting is performed in-place. To sort a list in descending order, you will have to provide argument "reverse=True".

```python
# ascending order
A.sort()
print(A)
```

```
[5, 10, 20, 30, 40, 99]
```

```python
# descending order
A.sort(reverse=True)
print(A)
```

```
[99, 40, 30, 20, 10, 5]
```

### reverse

The reverse method flips the list horizontally. This is also in-place.

```python
A = [9,8,10,-1]
A.reverse()
print(A)
```

```
[-1, 10, 8, 9]
```

### extend

Lists can be merged together to form a bigger list. This is done using the extend method.

```python
A.extend(B)
print(A)
```

```
[-1, 10, 8, 9, 50, 20, 30, 40]
```

You can also merge two listst using the '+' operator.

```python
M = [2,3,4]
N = [6,7,8]
m = 0
print('M+N = ',M+N)
```

```
M+N =  [2, 3, 4, 6, 7, 8]
```
