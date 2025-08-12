Of course. Here is the Markdown code containing all of your original Python code snippets, organized with headers for clarity.

# Python Code Snippets Reference

-----

## Print Statements

```python
#print
print('4.5', 56.7, 'Hello world') #we get space with commas
print("Hello")

print("Helloworld", 75, end='|') #by deafult end = '\n'
print("This will not be printed in the new line")
```

-----

## Variables and User Input

```python
#variables
hello_world = "Hello World" #snake case

#user input
# name = input('Name: ') #default string
# print(name)
```

-----

## Arithmetic Operations

```python
#arithmatic operations
a1 = 10
a2 = 5

print(a1/a2) #float by default
print(a1//a2) #integer division

# num = int(input('Number: ')) #type conversion to int
# print(num-2)
```

-----

## String Methods

```python
#string methods
print(hello_world.upper())
print(hello_world.lower())
# print(hello_world.count()) #wrong requires an argument
print(hello_world.count('or')) #count the occurances of 'or'
print(type(hello_world)) #type of the variable
print(hello_world.upper().count('L'))
print(len(hello_world))
```

```python
s = "Hello World"

print(s.upper())        # Converts all characters to uppercase: 'HELLO WORLD'
print(s.lower())        # Converts all characters to lowercase: 'hello world'
print(s.title())        # Capitalizes first letter of each word: 'Hello World'
print(s.capitalize())   # Capitalizes first letter of the string: 'Hello world'
print(s.strip())        # Removes leading/trailing whitespace
print(s.lstrip())       # Removes leading (left) whitespace
print(s.rstrip())       # Removes trailing (right) whitespace
print(s.replace("World", "Python"))  # Replaces substring: 'Hello Python'
print(s.split())        # Splits string into list by whitespace: ['Hello', 'World']
print(s.split('o'))     # Splits string at each 'o': ['Hell', ' W', 'rld']
print(s.join(['A', 'B', 'C']))  # Joins list with string as separator: 'AHello WorldBHello WorldC'
print(s.find('o'))      # Returns index of first occurrence of 'o': 4
print(s.rfind('o'))     # Returns index of last occurrence of 'o': 7
print(s.count('l'))     # Counts occurrences of 'l': 3
print(s.startswith('He'))  # Checks if string starts with 'He': True
print(s.endswith('ld'))    # Checks if string ends with 'ld': True
print(s.isalpha())      # Checks if all chars are alphabetic: False (space present)
print(s.isdigit())      # Checks if all chars are digits: False
print(s.isalnum())      # Checks if all chars are alphanumeric: False (space present)
print(len(s))           # Returns length of string: 11
```

-----

## Arithmetic on Strings

```python
#arthmatic on string
x = 'Hello'
y = 'World'

# Concatenation
print(x + y)        # Output: HelloWorld
print(x + ' ' + y)  # Output: Hello World

# Repetition
print(x * 3)        # Output: HelloHelloHello

# Invalid operations (will cause errors)
# print(x - y)      # Error
# print(x / 2)      # Error

print('ab'>'ad')
```

-----

## Conditional Statements

```python
#conditional statements
# or and not

x = int(input("X: "))

if x==5:
    print("Matched 5")
elif x==10:
    print("Matched 10")
else:
    print("didn't match")
```

-----

## Lists

```python
#lists are mutable
list1 = [4,5, "Hello"] #can store any type
```

```python
# Creating a list
my_list = [1, 2, 3, 4, 5] #my_list is pointing to the list

# Properties
print(len(my_list))        # Number of elements in the list
print(type(my_list))       # <class 'list'>

# Indexing and Slicing
print(my_list[0])          # First element: 1
print(my_list[-1])         # Last element: 5
print(my_list[1:3])        # Slice from index 1 to 2: [2, 3]

# List Methods
my_list.append(6)          # Adds 6 at the end
my_list.insert(2, 10)      # Inserts 10 at index 2
my_list.extend([7, 8])     # Adds multiple elements at the end

print(my_list.pop())       # Removes and returns last element (8)
print(my_list.pop(1))      # Removes and returns element at index 1 (2)
my_list.remove(10)         # Removes first occurrence of 10

my_list.clear()            # Removes all elements

my_list = [1, 2, 3, 2, 4, 2]
print(my_list.count(2))    # Counts occurrences of 2: 3
print(my_list.index(3))    # Returns index of first occurrence of 3: 2

my_list.reverse()          # Reverses the list in place
my_list.sort()             # Sorts the list in ascending order

# Copying
copy_list = my_list.copy() # Returns a shallow copy of the list

# Concatenation and Repetition
print(my_list + [9, 10])   # Concatenates lists
print(my_list * 2)         # Repeats the list

# Membership
print(3 in my_list)        # Checks if 3 is in the list: True

# Iteration
for item in my_list:
    print(item)

# List Comprehension
squared = [x**2 for x in my_list]  # Creates a new list with squares

# Nested Lists
nested = [[1, 2], [3, 4]]
print(nested[0][1])        # Accesses 2

# Unpacking
a, b, c, d, e, f = my_list # Assigns elements to variables (lengths must match)
```

```python
a = [1, 2, 3, 4, 5]
b = a[:]         # b is a shallow copy of a

s = "Hello"
t = s[:]         # t is a shallow copy of s

print(b)         # [1, 2, 3, 4, 5]
print(t)         # Hello

#for reverse [::-1]
```

```python
import copy

original = [[1, 2], [3, 4]]
deep_copied = copy.deepcopy(original)

# Now, changes to deep_copied do NOT affect original
deep_copied[0][0] = 99
print(original)      # Output: [[1, 2], [3, 4]]
print(deep_copied)   # Output: [[99, 2], [3, 4]]
```

-----

## Tuples

```python
#tuple
# Creating a tuple
tup = (1, 2, 3, 4, 5)
single = (42,)         # Single-element tuple (note the comma)

# Properties
print(len(tup))        # Number of elements in the tuple
print(type(tup))       # <class 'tuple'>

# Indexing and Slicing
print(tup[0])          # First element: 1
print(tup[-1])         # Last element: 5
print(tup[1:3])        # Slice from index 1 to 2: (2, 3)

# Tuple Methods
print(tup.count(2))    # Counts occurrences of 2: 1
print(tup.index(3))    # Returns index of first occurrence of 3: 2

# Concatenation and Repetition
print(tup + (6, 7))    # Concatenates tuples: (1, 2, 3, 4, 5, 6, 7)
print(tup * 2)         # Repeats the tuple: (1, 2, 3, 4, 5, 1, 2, 3, 4, 5)

# Membership
print(3 in tup)        # Checks if 3 is in the tuple: True

# Iteration
for item in tup:
    print(item)

# Tuple unpacking
a, b, c, d, e = tup    # Assigns elements to variables

# Nested tuples
nested = ((1, 2), (3, 4))
print(nested[0][1])    # Accesses 2

# Slicing (shallow copy)
tup2 = tup[:]          # tup2 is a shallow copy of tup

# Immutability
# tup[0] = 10          # Error! Tuples are immutable

# Conversion
lst = list(tup)        # Convert tuple to list
new_tup = tuple(lst)   # Convert list to tuple

# Tuple with mixed types
mixed = (1, "hello", 3.14, [1, 2])

# Single-element tuple
single = (42,)         # Must have a comma

# Tuple packing and unpacking
packed = 1, 2, 3       # Packing: creates a tuple (1, 2, 3)
x, y, z = packed       # Unpacking

# Nested unpacking
tup3 = (1, (2, 3))
a, (b, c) = tup3       # a=1, b=2, c=3
```

```python
a = [1, 2, 3]
b = ['x', 'y', 'z']
zipped = zip(a, b)
print(list(zipped))  # [(1, 'x'), (2, 'y'), (3, 'z')]
```

-----

## Loops

```python
#Loops
# Basic for loop over a list
my_list = [10, 20, 30]
for item in my_list:
    print(item)

# For loop with range (0 to 4)
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4

# For loop with range(start, stop, step)
for i in range(1, 10, 2):
    print(i)  # 1, 3, 5, 7, 9

# Looping with index: range(len(list))
for i in range(len(my_list)):
    print(f"Index {i}, Value {my_list[i]}")

# Using enumerate to get index and value
for idx, val in enumerate(my_list):
    print(f"Index {idx}, Value {val}")

# Looping over a string
s = "hello"
for char in s:
    print(char)

# Looping over a tuple
tup = (1, 2, 3)
for item in tup:
    print(item)

# Looping over a dictionary
d = {'a': 1, 'b': 2}
for key in d:
    print(key, d[key])  # key and value

for key, value in d.items():
    print(key, value)   # key and value

# While loop
count = 0
while count < 3:
    print(count)
    count += 1

# Infinite loop (use with caution)
# while True:
#     print("This will run forever")

# Loop with break and continue
for i in range(5):
    if i == 3:
        break           # Exit the loop
    if i == 1:
        continue        # Skip the rest of this iteration
    print(i)

# else with loops (runs if loop wasn't broken)
for i in range(3):
    print(i)
else:
    print("Loop finished without break")

# List comprehension (compact for loop)
squares = [x**2 for x in range(5)]  # [0, 1, 4, 9, 16]

# Useful functions
print(list(range(5)))               # [0, 1, 2, 3, 4]
print(list(enumerate(['a', 'b'])))  # [(0, 'a'), (1, 'b')]
print(reversed([1, 2, 3]))          # <list_reverseiterator object>
print(list(reversed([1, 2, 3])))    # [3, 2, 1]
print(sorted([3, 1, 2]))            # [1, 2, 3]
```

-----

## Slicing

```python
# Slice
# Basic slicing: sequence[start:stop]
a = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

print(a[2:5])      # [2, 3, 4]   (from index 2 up to, but not including, 5)
print(a[:4])       # [0, 1, 2, 3] (from start up to index 4)
print(a[6:])       # [6, 7, 8, 9] (from index 6 to end)
print(a[:])        # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9] (entire list, shallow copy)

# Slicing with step: sequence[start:stop:step]
print(a[1:8:2])    # [1, 3, 5, 7] (from index 1 to 7, step 2)
print(a[::2])      # [0, 2, 4, 6, 8] (every second element)
print(a[::-1])     # [9, 8, 7, 6, 5, 4, 3, 2, 1, 0] (reversed list)
print(a[5:2:-1])   # [5, 4, 3] (from index 5 down to 3, step -1)

# Negative indices
print(a[-3:])      # [7, 8, 9] (last 3 elements)
print(a[:-3])      # [0, 1, 2, 3, 4, 5, 6] (all except last 3)

# Slicing strings and tuples works the same way
s = "Hello, World!"
print(s[7:12])     # 'World'
print(s[::-1])     # '!dlroW ,olleH'

t = (10, 20, 30, 40, 50)
print(t[1:4])      # (20, 30, 40)

# Assigning to slices (lists only, not strings/tuples)
a[2:5] = [100, 101, 102]
print(a)           # [0, 1, 100, 101, 102, 5, 6, 7, 8, 9]

# Deleting with slices
del a[2:5]
print(a)           # [0, 1, 5, 6, 7, 8, 9]

# Copying a list
b = a[:]           # Shallow copy of a

# Advanced: slice object
sl = slice(2, 8, 2)
# The next line will error because list 'a' has been modified and is too short.
# The comment below shows the expected output if 'a' was [0, 1, 5, 6, 7, 8, 9]
# print(a[sl])       # [5, 7, 9] (if a is [0, 1, 5, 6, 7, 8, 9])

# Summary of slice syntax:
# sequence[start:stop:step]
# - start: index to begin (inclusive, default 0)
# - stop: index to end (exclusive, default end of sequence)
# - step: increment (default 1, can be negative for reverse)
```

-----

## Sets

```python
#Sets
# Creating a set
s = {1, 2, 3}
empty_set = set()           # Note: {} creates an empty dict, not a set

# Properties
print(len(s))               # Number of elements in the set
print(type(s))              # <class 'set'>

# Adding elements
s.add(4)                    # Adds 4 to the set
s.update([5, 6])            # Adds multiple elements

# Removing elements
s.remove(2)                 # Removes 2, raises KeyError if not found
s.discard(10)               # Removes 10 if present, does nothing if not
s.pop()                     # Removes and returns an arbitrary element
s.clear()                   # Removes all elements

# The set 's' is now empty, so the next line will error
# print(3 in s)               # True if 3 is in the set

# Set operations
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)                # Union: {1, 2, 3, 4, 5}
print(a.union(b))           # Union using method

print(a & b)                # Intersection: {3}
print(a.intersection(b))    # Intersection using method

print(a - b)                # Difference: {1, 2}
print(a.difference(b))      # Difference using method

print(a ^ b)                # Symmetric difference: {1, 2, 4, 5}
print(a.symmetric_difference(b))

# Subset and superset
print(a <= b)               # Subset: False
print(a.issubset(b))        # Subset using method
print(a >= b)               # Superset: False
print(a.issuperset(b))      # Superset using method

# Disjoint
print(a.isdisjoint(b))      # True if no common elements

# Copying
c = a.copy()                # Shallow copy

# Iteration
# Re-initializing set 's' for iteration example
s = {10, 20, 30}
for item in s:
    print(item)

# Set comprehension
squared = {x**2 for x in range(5)}  # {0, 1, 4, 9, 16}

# Conversion
lst = list(s)               # Convert set to list
tup = tuple(s)              # Convert set to tuple

# Frozen set (immutable set)
fs = frozenset([1, 2, 3])
# fs.add(4)                 # Error! frozenset is immutable

# Note: Sets are unordered, mutable, and do not allow duplicates.
```

-----

## Dictionaries

```python
#Dictionaries
# Creating a dictionary
d = {'a': 1, 'b': 2, 'c': 3}
empty_dict = {}                 # Empty dictionary
d2 = dict(x=10, y=20)           # Using dict constructor

# Properties
print(len(d))                   # Number of key-value pairs
print(type(d))                  # <class 'dict'>

# Accessing values
print(d['a'])                   # Access value by key: 1
# print(d['z'])                # KeyError if key not found
print(d.get('z'))               # Returns None if key not found
print(d.get('z', 0))            # Returns 0 if key not found

# Adding/Updating values
d['d'] = 4                      # Adds new key-value pair
d['a'] = 100                    # Updates value for key 'a'

# Removing items
d.pop('b')                      # Removes key 'b' and returns its value
# d.pop('z')                   # KeyError if key not found
d.pop('z', None)                # Returns None if key not found
del d['c']                      # Deletes key 'c'
# del d['z']                   # KeyError if key not found
d.clear()                       # Removes all items

# The dictionary 'd' is now empty
# Membership
print('a' in d)                 # True if 'a' is a key in d

# Iteration
# Re-initializing 'd' for iteration examples
d = {'name': 'Bob', 'age': 30}
for key in d:
    print(key, d[key])          # Iterates over keys

for value in d.values():
    print(value)                # Iterates over values

for key, value in d.items():
    print(key, value)           # Iterates over key-value pairs

# Dictionary methods
d = {'a': 1, 'b': 2, 'c': 3}
print(d.keys())                 # dict_keys(['a', 'b', 'c'])
print(d.values())               # dict_values([1, 2, 3])
print(d.items())                # dict_items([('a', 1), ('b', 2), ('c', 3)])

d2 = d.copy()                   # Shallow copy
d.update({'d': 4, 'e': 5})      # Adds/updates multiple key-value pairs

# Set default value if key not present
d.setdefault('f', 0)            # Adds 'f':0 if not present, returns value

# Dictionary comprehension
squares = {x: x**2 for x in range(5)}  # {0:0, 1:1, 2:4, 3:9, 4:16}

# Nested dictionaries
nested = {'outer': {'inner': 42}}
print(nested['outer']['inner'])        # 42

# Conversion
keys = ['a', 'b', 'c']
values = [1, 2, 3]
d3 = dict(zip(keys, values))           # {'a': 1, 'b': 2, 'c': 3}

# Unpacking (Python 3.5+)
# d4 = {**d, **{'g': 7}}                 # Merge two dicts

# Note: Dictionaries are unordered (ordered since Python 3.7), mutable, and keys must be unique and immutable.
```

-----

## Comprehensions

```python
# --- Comprehensions ---

# List comprehension
squares = [x**2 for x in range(5)]           # [0, 1, 4, 9, 16]
evens = [x for x in range(10) if x % 2 == 0] # [0, 2, 4, 6, 8]

# Set comprehension
unique = {char for char in "hello"}          # {'h', 'e', 'l', 'o'}

# Dictionary comprehension
squares_dict = {x: x**2 for x in range(5)}   # {0:0, 1:1, 2:4, 3:9, 4:16}

# Nested comprehension
matrix = [[i*j for j in range(3)] for i in range(3)]  # [[0, 0, 0], [0, 1, 2], [0, 2, 4]]
```

-----

## Functions

```python
# --- Functions ---

def greet(name):
    print("Hello,", name)

greet("Alice")  # Hello, Alice

def add(a, b):
    return a + b

result = add(2, 3)  # 5

def power(x, y=2):  # Default argument
    return x ** y

print(power(3))     # 9
print(power(3, 3))  # 27
```

-----

## \*args and \*\*kwargs

```python
# --- *args and **kwargs ---

def my_sum(*args):
    print(args)         # args is a tuple of all positional arguments
    return sum(args)

print(my_sum(1, 2, 3)) # 6

def print_info(**kwargs):
    print(kwargs)       # kwargs is a dict of all keyword arguments

print_info(name="Alice", age=25)
# {'name': 'Alice', 'age': 25}

def demo(a, b=2, *args, **kwargs):
    print(a, b, args, kwargs)

demo(1, 3, 4, 5, x=10, y=20)
# 1 3 (4, 5) {'x': 10, 'y': 20}

# Unpacking with * and **
nums = [1, 2, 3]
print(*nums)  # 1 2 3

d = {'name': 'Bob', 'age': 30}
print_info(**d)  # {'name': 'Bob', 'age': 30}
```

-----

## Exception Handling

```python
# ---- Exception Handling ----

# Basic try-except
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")

# Catching multiple exceptions
try:
    a = int("abc")
except (ValueError, TypeError):
    print("Invalid conversion or type!")

# Catching all exceptions (not recommended for most cases)
# The function risky_code() is not defined, so this will cause an error
# try:
#     risky_code()
# except Exception as e:
#     print("An error occurred:", e)

# Using else (runs if no exception occurs)
try:
    num = int(input("Enter a number: "))
except ValueError:
    print("That's not a number!")
else:
    print("You entered:", num)

# Using finally (always runs, even if exception occurs)
try:
    f = open("file.txt")
except FileNotFoundError:
    print("File not found.")
else:
    print("File opened successfully.")
    f.close() # Important to close the file
finally:
    print("This runs no matter what (cleanup, closing files, etc.)")

# Raising exceptions manually
def divide(a, b):
    if b == 0:
        raise ZeroDivisionError("You can't divide by zero!")
    return a / b

# Custom exception
class MyError(Exception):
    pass # Function does nothing (yet)

try:
    raise MyError("Something went wrong!")
except MyError as e:
    print("Caught custom exception:", e)
```

-----

## Lambda, Map, and Filter

```python
# --- Lambda Functions ---

# Basic lambda (anonymous function)
add = lambda x, y: x + y
print(add(2, 3))           # 5

# Used for short, one-line functions
square = lambda x: x**2
print(square(4))           # 16

# Lambda with no arguments
hello = lambda: "Hello!"
print(hello())             # Hello!

# Lambda inside sort (custom key)
words = ['apple', 'banana', 'kiwi']
words.sort(key=lambda w: len(w))
print(words)               # ['kiwi', 'apple', 'banana']

# --- map() ---

# map(function, iterable) applies function to each item
nums = [1, 2, 3, 4]
squared = list(map(lambda x: x**2, nums))
print(squared)             # [1, 4, 9, 16]

# map with built-in function
str_nums = list(map(str, nums))
print(str_nums)            # ['1', '2', '3', '4']

# --- filter() ---

# filter(function, iterable) keeps items where function returns True
even = list(filter(lambda x: x % 2 == 0, nums))
print(even)                # [2, 4]

# filter with built-in function
non_empty = list(filter(None, ["", "hello", None, "world"]))
print(non_empty)           # ['hello', 'world']

# --- Combined Example ---

# Get squares of even numbers
nums = [1, 2, 3, 4, 5]
even_squares = list(map(lambda x: x**2, filter(lambda x: x % 2 == 0, nums)))
print(even_squares)        # [4, 16]
```

-----

## F-Strings

```python
# f-strings
# Basic usage
name = "Alice"
age = 25
print(f"My name is {name} and I am {age} years old.")
# Output: My name is Alice and I am 25 years old.

# Expressions inside f-strings
print(f"Next year, I will be {age + 1}.")
# Output: Next year, I will be 26.

# Formatting numbers
pi = 3.14159
print(f"Pi rounded to 2 decimals: {pi:.2f}")
# Output: Pi rounded to 2 decimals: 3.14

# Padding and alignment
print(f"|{name:>10}|")   # Right align: |     Alice|
print(f"|{name:<10}|")   # Left align:  |Alice     |
print(f"|{name:^10}|")   # Center:      |  Alice   |

# Using dictionaries
person = {'name': 'Bob', 'age': 30}
print(f"{person['name']} is {person['age']} years old.")
# Output: Bob is 30 years old.

# Using function calls
def greet(name):
    return f"Hello, {name}!"

print(f"{greet('Charlie')}")
# Output: Hello, Charlie!

# Nested f-strings
value = 7
print(f"Value is {f'{value:04d}'}")
# Output: Value is 0007

# Raw f-strings (for paths, etc.)
path = r"C:\Users\Alice"
print(f"Path: {path}")
# Output: Path: C:\Users\Alice

# Using !r for repr()
print(f"Debug: {name!r}")
# Output: Debug: 'Alice'
```

-----

## File I/O

```python
# --- Opening and Closing Files ---

# Create dummy files for the example to run without errors
with open('example.txt', 'w') as f:
    f.write("This is a sample file.\nLine 2.\n")
with open('log.txt', 'w') as f:
    f.write("Log started.\n")

# Open a file for reading (default mode is 'r')
f = open('example.txt', 'r')

# Open a file for writing (creates or overwrites)
f_out = open('output.txt', 'w')

# Open a file for appending (creates if not exists)
f_log = open('log.txt', 'a')

# Always close the file when done
f.close()
f_out.close()
f_log.close()

# --- Reading Files ---

f = open('example.txt', 'r')
content = f.read()           # Reads entire file as a string
print(content)
f.close()

f = open('example.txt', 'r')
lines = f.readlines()        # Reads all lines into a list
print(lines)
f.close()

f = open('example.txt', 'r')
line = f.readline()          # Reads one line at a time
print(line)
f.close()

# --- Writing Files ---

f = open('output.txt', 'w')
f.write("Hello, World!\n")   # Writes a string to the file
f.writelines(['Line 1\n', 'Line 2\n'])  # Writes a list of strings
f.close()

# --- Using with statement (auto-closes file) ---

with open('example.txt', 'r') as f:
    for line in f:
        print(line.strip())  # Reads file line by line

with open('output.txt', 'w') as f:
    f.write("Written using with statement.\n")

# --- File Modes ---
# 'r'  : read (default)
# 'w'  : write (truncate)
# 'a'  : append
# 'x'  : create (fail if exists)
# 'b'  : binary mode (e.g., 'rb', 'wb')
# 't'  : text mode (default, e.g., 'rt', 'wt')
# '+'  : read and write (e.g., 'r+', 'w+')

# --- Checking if file exists ---
import os
print(os.path.exists('example.txt'))  # True if file exists

# --- Reading/Writing binary files ---
# Create a dummy binary file for the example
with open('image.png', 'wb') as f:
    f.write(b'\x89PNG\r\n\x1a\n')

with open('image.png', 'rb') as f:
    data = f.read()

with open('copy.png', 'wb') as f:
    f.write(data)

# --- Exception Handling with Files ---
try:
    with open('nofile.txt', 'r') as f:
        data = f.read()
except FileNotFoundError:
    print("File not found!")

# --- Useful methods ---
# f.read([size])      # Reads size bytes (or all if not specified)
# f.readline()        # Reads one line
# f.readlines()       # Reads all lines into a list
# f.write(string)     # Writes string
# f.writelines(list)  # Writes list of strings
# f.seek(offset)      # Moves file pointer to offset
# f.tell()            # Returns current file pointer position

with open('example.txt', 'r') as f:
    data = f.read()      # OK: inside the block
    print(data)          # OK: inside the block

# Here, f is already closed and cannot be used
# print(f.read())       # Error! File is closed
```
