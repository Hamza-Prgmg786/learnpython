# Welcome to Python

## Catalogue

- [Comments](#Comments)
- [Variables](#Variables)
- [Constants](#Constants)
- [Keywords](#Keywords)
- [Data_Types](#Data_Types)
- [Operators](#Operators)
- [Program_Control_Flow](#Program_Control_Flow)
- [Array](#Array)
- [Functions](#Functions)
- [Pointers](#Pointers)
- [Struct](#Struct)
- [Memory_Layout](#Memory_Layout)
- [Reference](#Reference)
- [Object_Oriented_Programming](#Object_Oriented_Programming)

## Comments

Single-line comments

```
# ...
```

Multi-line comments

```
"""
This is a comment
written in
more than just one line
"""
```

## Variables

Give a name to a space in memory.

```
variable_Name = value;

a = 10;
name = "Steve Jobs"
```

## Constants

Unchangeable data in the program.

```
To work around this, you use all capital letters to name a variable to indicate that the variable 
should be treated as a constant. For example:

Defining constant_name value;
 
# DAY = 7
```

## Keywords

Python keywords reserved and not available for re-definition or overloading.

![avatar](/python_keywords.png)

## Data_Types

A variable is a named location used to store data in the memory. 

#### 1. Integer

Python int variable requires minimum 24 bytes on 32-bit / 64-bit system.
It may vary as per hardware.
```
import sys
sys.getsizeof( int() ) # prints 24
sys.getsizeof(0) # prints 24
sys.getsizeof(1) # prints 28
sys.getsizeof(-2) # prints 28
```
It is helpful to think of variables as a container that holds data that can be changed later
in the program. 

Represent integers like 1, 10.
```
number = 10
```

#### 2. Floating point

Python int variable requires minimum 24 bytes on 32-bit / 64-bit system.
It may vary as per hardware.
```
import sys
sys.getsizeof( float() ) # prints 24
sys.getsizeof(0.0) # prints 24
```

Represent decimals like 1.23, -2.332.
```
number = 1.23
```

#### 3. String

```
a = "Hello, World!"
print(a)
```

#### 5. Boolean

Represent True and False.

```
import sys
sys.getsizeof( bool() ) # prints 24
sys.getsizeof(True) # prints 28
sys.getsizeof(False) # prints 24
```

```
print(10 > 9)
print(10 == 9)
```

```
+ - * / % ++ -- += >= || ! && ...
```

```
pre-increment/decrement: a=2; b=++a; // Do b=a first and ++a, the result is a=3; b=3;
```

```
post-increment/decrement: a=2; b=a++; // Do a++ first and b=a, the result is a=3; b=2;
```

## Program_Control_Flow

#### 1. Selection statements

If condition:
```
a = 10
b = 5
if b > a:
  ...
elif a == b:
  ...
else:
  ...
```

Conditional Operator ?:
```
c = a > b ? a : b; // a > b is true then return a, false return b.
```

Switch condition:
```
Python does not have this. 
So, to get around this, we use Python’s built-in dictionary construct to implement cases and decided what to do when a case is met. 
We can also specify what to do when none is met.
```

#### 2. Iteration statements

While loop:
```
# expression can be any condition

while expression:
  statement
 } 
```

## Array

Arrays are used to store multiple values in one single variable:
```
x = ["A", "B", "C", "D"]
```

#### 1. What is an Array

An array is a special variable, they can hold more than one value at a time.
```
x1 = "A"
x2 = "B"
x3 = "C"
x4 = "D"
```

#### 2. Accessing the elements of an Array.
```
x1 = x[0]
```

#### 3. Get the length of the array.
```
x1 = len(x)
```

#### 4. Looping Array Elements.
```
for x1 in x:
  print(x1)
```

#### 5. Adding Array Elements.
```
x.append("E")
```

#### 6. Removing Array Elements.

pop() method to remove an element from the array.
```
x.pop(1)
```

remove() method to remove an element from the array.
```
x.remove("A")
```

#### 7. Array Methods.

Python has a set of built-in methods that you can use on lists/arrays.
```
append()  -> Adds an element at the end of the list.
clear()   -> Removes all the elements from the list
copy()    -> Returns a copy of the list.
count()   -> Returns the number of elements with the specified value.
extend()  -> Add the elements of a list (or any iterable), to the end of the current list.
index()   -> Returns the index of the first element with the specified value.
insert()  -> Adds an element at the specified position.
pop()     -> Removes the element at the specified position.
remove()  -> Removes the first item with the specified value.
reverse() -> Reverses the order of the list.
sort()    -> Sorts the list.
```

## Functions

Encapsulate a piece of frequently used code to reduce repetitive use of code.
```
def add(num_1, num_2): // num_1 and num_2 are parameters
   sum = num_1 + num_2
   return sum
}

if __name__ == '__main__':
   a = 10
   b = 20
   sum = add(a, b) // a and b are arguments
}
```

#### 1. Arbitrary Arguments, *args.

if you do not know how many arguments that will be passed into your function.
Add a * before the parameter name in the function definition.
This way the function will receive a tuple of arguments, and can access the items accordingly:

```
def my_function(*children):
  print("The children are " + kids[2])

my_function("Steve", "Robert", "Sarah")
```

#### 2. Default Parameter Value.

If we call the function without argument, it uses the default value:

```
def my_function(child = "Steve"):
  print("My Name is" + child)

my_function("Sarah")
my_function("Robert")
my_function()
```

#### 3. Passing a List as an Argument.

You can send any data types of argument to a function (string, number, list, dictionary etc.).
It will be treated as the same data type inside the function.

```
def my_function(child):
  for x in child:
    print(x)

childrens = ["Steve", "Robert", "Sarah"]

my_function(childrens)
```

#### 4. Recursion.

Python also accepts function recursion, which means a defined function can call itself.

Recursion is a common mathematical and programming concept. 
It means that a function calls itself. 
This has the benefit of meaning that you can loop through data to reach a result.

```
def recursion(k):
  if (k > 0):
    result = k + recursion(k - 1)
    print(result)
  else:
    result = 0
  return result

print("\n\nRecursion")
recursion(6)
```
