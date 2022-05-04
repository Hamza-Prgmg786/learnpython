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

Python does not have this.
So, to get around this, we use Python’s built-in dictionary construct to implement cases and decided what to do when a case is met.
We can also specify what to do when none is met.



