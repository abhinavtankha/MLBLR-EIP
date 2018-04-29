Assignment Rewrite the python tutorial.
This tutorial content was contributed by [Justin Johnson](https://cs.stanford.edu/people/jcjohns/)

## Python
Python is a high-level, dynamically typed multiparadigm programming language. Python code is often said to be almost like pseudocode, since it allows you to express very powerful ideas in very few lines of code while being very readable. As an example, here is an implementation of the classic quicksort algorithm in Python:
```python
def quicksort(mlblr_in):
  if len(mlblr_in) <= 1:
    return mlblr_in
  mlblr = mlblr_in[len(mlblr_in)/2]
  eip_in = [x for x in mlblr_in if x < mlblr]
  eip = [x for x in mlblr_in if x == mlblr]
  eip_out = [x for x in mlblr_in if x > mlblr]
  return quicksort(eip_in) + eip + quicksort(eip_out)
  
  print(quicksort([3,6,8,10,1,2,1]))
  #Prints "[1, 1, 2, 3, 6, 8, 10]"
```
### Python versions
There are currently two different supported versions of Python, 2.7 and 3.5. Somewhat confusingly, Python 3.0 introduced many backwards-incompatible changes to the language, so code written for 2.7 may not work under 3.5 and vice versa. For this class all code will use Python 3.5.

You can check your Python version at the command line by running python --version.

### Basic data types
Like most languages, Python has a number of basic types including integers, floats, booleans, and strings. These data types behave in ways that are familiar from other programming languages.

#### Numbers: 
Integers and floats work as you would expect from other languages:

```python
eip = 3
print(type(eip)) # Prints "<class 'int'>"
print(eip)       # Prints "3"
print(eip + 1)   # Addition; prints "4"
print(eip - 1)   # Subtraction; prints "2"
print(eip * 2)   # Multiplication; prints "6"
print(eip ** 2)  # Exponentiation; prints "9"
eip += 1
print(eip)  # Prints "4"
eip *= 2
print(eip)  # Prints "8"
mlblr = 2.5
print(type(mlblr)) # Prints "<class 'float'>"
print(mlblr, mlblr + 1, mlblr * 2, mlblr ** 2) # Prints "2.5 3.5 5.0 6.25"

```

<type 'int'>
3
4
2
6
9
4
8
<type 'float'>
(2.5, 3.5, 5.0, 6.25)
Note that unlike many languages, Python does not have unary increment (eip++) or decrement (eip--) operators.

Python also has built-in types for complex numbers; you can find all of the details in the documentation.

**Booleans**: Python implements all of the usual operators for Boolean logic, but uses English words rather than symbols (&&, ||, etc.):
```python
eip = True
mlblr = False
print(type(eip)) # Prints "<class 'bool'>"
print(eip and mlblr) # Logical AND; prints "False"
print(eip or mlblr)  # Logical OR; prints "True"
print(not eip)   # Logical NOT; prints "False"
print(eip != mlblr)  # Logical XOR; prints "True"
```

<type 'bool'>
False
True
False
True
**Strings**: Python has great support for strings:
```python
eip_in = 'hello'    # String literals can use single quotes
mlblr = "world"    # or double quotes; it does not matter.
print(eip_in)       # Prints "hello"
print(len(eip_in))  # String length; prints "5"
eip_out = eip_in + ' ' + mlblr  # String concatenation
print(eip_out)  # prints "hello world"
mlblr_out = '%s %s %d' % (eip_in, mlblr, 12)  # sprintf style string formatting
print(mlblr_out)  # prints "hello world 12"

```
hello
5
hello world
hello world 12
String objects have a bunch of useful methods; for example:

```python
eip = "hello"
print(eip.capitalize())  # Capitalize a string; prints "Hello"
print(eip.upper())       # Convert a string to uppercase; prints "HELLO"
print(eip.rjust(7))      # Right-justify a string, padding with spaces; prints "  hello"
print(eip.center(7))     # Center a string, padding with spaces; prints " hello "
print(eip.replace('l', '(ell)'))  # Replace all instances of one substring with another;
                                # prints "he(ell)(ell)o"
print('  world '.strip())  # Strip leading and trailing whitespace; prints "world"

```
Hello
HELLO
  hello
 hello 
he(ell)(ell)o
world
You can find a list of all string methods in the documentation.

