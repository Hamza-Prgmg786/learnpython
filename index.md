# Welcome to Python

## Catalogue

- [Comments](#Comments)
- [Variables](#Variables)
- [Constants](#Constants)
- [Keywords](#Keywords)
- [Data_Types](#Data_Types)
- [Data_Input](#Data_Input)
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
