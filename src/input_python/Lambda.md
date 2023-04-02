# Python Lambda

## Introduction

Lambda function is a really useful feature provided by python. A lambda function is an anonymous function, i.e., without any name. It can take any number of arguments but can have only one expression. Let's see an example below.

### Syntax

```
lambda arguments : expression
```

```python
r = 10
circle = lambda r : 3.14 * r * r
print(circle(5))
```

### Output

```
314
```

Now let's see an example with multiple arguments

```python
a = 10
b = 12
rectangle = lambda a,b : a*b
print(rectangle)
```

### Output

```
120
```
