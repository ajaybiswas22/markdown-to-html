# Python Yield

## Introduction

Yield keyword works similarly like return statement, however unlike return statement which ends the current function and return the result, it returns a generator object without stopping the ongoing function execution. First let's see how return statement works, then we will see what yield does.

```python

def func():
    nums = [1,2,3,4]
    for num in nums:
        return num
    return 5
    
x = func()
print(x)
```

```
1
```

Now let's see the output of yield

```python
def func():
    nums = [1,2,3,4]
    for num in nums:
        yield num
    yield 5
    
x = func()
print(x)
for item in x:
    print(item) 
```

```
<generator object func at 0x2af8fd05e9e0>
1
2
3
4
5
```
