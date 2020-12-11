# leet-python-guide
Python study guide driven through LeetCode (see solutions)

## Basics
First, let's begin with an overview of basic things that can be done in Python. If you're savvy, skip this section :) 

### Hello World
Do I need to say more?
```
print("Hello World!")
```

### Variables, Assignment, Types
Let's print my favorite color and its type.
```
favorite_color = "red"
print(favorite_color, "is a", type(favorite_color))
```

### Operations
Here's a simple example to compute the area of a circle using an approximation of pi.

By the way, the operator ** is exponentiation :)

```
pi = 3.14159
radius = 3
area = pi * r ** 2
print("The area of this circle is", area)
print("The area has a type", type(area), "!")
```

Some lesser known operations for you math whizzes out there ;)
```
a = 5
b = 2
print(a // b, "= 2")  # This is floor division
print(a % b, "= 1")   # This is modulus
print(-a, "= -5")     # This is negation
```

Note: Python follow PEMDAS - Parentheses, Exponents, Multiplication/Division, Addition/Subtraction when carrying out operations.

### Built-in Functions
These are functions that are always available (much power, much wow):
```
best_prime = max(2,3,5)
print("The best prime is", best_prime)
```

*print* and *type* are also considered built-in functions just in case you didn't know!

Here's a list of some more [built-in functions](https://docs.python.org/3/library/functions.html#built-in-functions)!

## Functions

We have already used a few built-functions from the previous example, but what if we want to define our own cool function?

Here's a cool function that does some cool math and returns a cool number:
```
def cool_func(a, b):
  cool_num = (a**2 + b**2) # cool math
  return pow(cool_num, 0.5)
```

We can call our cool function like so:
```
print(cool_func(3,4))
```

### Help
~~If you ever~~ Once you get stuck coding, you can request some *help* from your function!

```
help(print)
```

Here's the output:
```
Help on built-in function print in module builtins:

print(...)
    print(value, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
    
    Prints the values to a stream, or to sys.stdout by default.
    Optional keyword arguments:
    file:  a file-like object (stream); defaults to the current sys.stdout.
    sep:   string inserted between values, default a space.
    end:   string appended after the last value, default a newline.
    flush: whether to forcibly flush the stream.
```

Or use stackoverflow or whatever...

### Docstrings
These are used to provide some basic documentation to your functions:

```
def cool_func(a, b):
  """Return a cool_num from any two numbers a and b.
  
  >>> cool_func(3,4)
  5.0
  """
  cool_num = (a**2 + b**2) # cool math
  return pow(cool_num, 0.5)
```

The docstring shows up when we request help!

```
help(cool_func)
```

Here's the output:
```
Help on function cool_func in module __main__:

cool_func(a, b)
    Return a cool_num from any two numbers a and b.
    
    >>> cool_func(3,4)
    5.0
```

### Function Inception
You can pass functions to functions and then you can pass those functions to functions and then you can pass those functions to functions of functions and then you can...

I think you get the point.

```
def mult_by_self(x):
  return x*x

def call(fn, num):
  return fn(num)

def call_ception(fn, num):
  return fn(fn(num))
```

Here we pass *mult_by_self* and a number using *call*
```
print(call(mult_by_self, 5), "= 25")
```

Now towards call_ception:
```
print(call_ception(mult_by_self, 5), "= 625")
```

## Booleans and Conditionals
Pretty straightfoward, but here's a quick example.

```
x = True
print(x)
print(type(x))

if x:
  print("I am true!")
else:
  print("I am false!")
```

Here's the output:

```
>>> True
>>> <class 'bool'>
>>> I am true!
```