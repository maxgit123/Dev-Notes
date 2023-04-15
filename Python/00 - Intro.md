[Download page](https://www.python.org/downloads/)

To check if python is installed write the following command on your device terminal.

```Shell
python --version
```

### Python Indentation

An indentation is a white space in a text. Indentation in many languages is used to increase code readability, however Python uses indentation to create block of codes. In other programming languages curly brackets are used to create blocks of codes instead of indentation. One of the common bugs when writing python code is wrong indentation.

### Comments

``` Python
# this is a python comment, because it starts with a hash (#) symbol
```

``` Python
''' This is multiline comment
multiline comment takes multiple lines.
python is eating the world
'''
```

### Operators

``` Python
print(2 + 3)             # Adition (+)
print(3 - 1)             # Subtraction (-)
print(2 * 3)             # Multiplication (*)
print(3 / 2)             # Division (/)
print(3 % 2)             # Modulus (%)
print(3 // 2)            # Floor division (//)
print(3 ** 2)            # Exponential (**)
```

### Data types

#### Number

-   Integer: Integer (negative, zero and positive) numbers. Example: ... -3, -2, -1, 0, 1, 2, 3 ...
-   Float: Decimal number. Example: ... -3.5, -2.25, -1.0, 0.0, 1.1, 2.2, 3.5 ...
-   Complex. Example: 1 + j, 2 + 4j

#### String

A collection of one or more characters under a single or double quote. If a string is more than one sentence then we use a triple quote.

``` Python
'Python'
'I love learn'
'I\'m enjoying the first day of 30DaysOfPython Challenge'
'''When the
strin is
too long'''
```

#### Booleans

A boolean data type is either a True or False value. T and F should be always uppercase.

``` Python
print(True)
print(False)
```

#### List

Python list is an ordered collection which allows to store different data type items. A list is similar to an array in JavaScript.

Example:

``` Python
# All are the same data types
[0, 1, 2, 3, 4, 5]  # A list of numbers
['Banana', 'Orange', 'Mango', 'Avocado'] # A list of strings (fruits)
['Finland','Estonia', 'Sweden','Norway'] # A list of strings (countries)
# Different data types in the list
['Banana', 10, False, 9.81] # string, integer, boolean and float
```

#### Dictionary

A Python dictionary object is an unordered collection of data in a key value pair format.

Example:

``` Python
{
'first_name':'Asabeneh',
'last_name':'Yetayeh',
'country':'Finland', 
'age':250, 
'is_married':True,
'skills':['JS', 'React', 'Node', 'Python']
}
```

#### Tuple

A tuple is an ordered collection of different data types like list but tuples can not be modified once they are created. **They are immutable.**

Example:

``` Python
('Asabeneh', 'Pawel', 'Brook', 'Abraham', 'Lidiya') # Names
('Earth', 'Jupiter', 'Neptune', 'Mars', 'Venus', 'Saturn', 'Uranus', 'Mercury') # planets
```

#### Set

A set is a collection of data types similar to list and tuple. Unlike list and tuple, set is not an ordered collection of items. Like in Mathematics, set in Python stores only unique items.

In later sections, we will go in detail about each and every Python data type.

Example:

``` Python
{2, 4, 3, 5}
{3.14, 9.81, 2.7} # Order is not important in set
```

### Checking Data types

To check the data type of certain data/variable we use the **type** function.

``` Python
print(type(10))          # Int
print(type(3.14))        # Float
print(type(1 + 3j))      # Complex
print(type('Asabeneh'))  # String
print(type(True))        # Boolean
print(type([1, 2, 3]))   # List
print(type({'name':'Asabeneh'})) # Dictionary
type((2,3,4,5))          # Tuple
type({9.8, 3.14, 2.7})   # Set
```

