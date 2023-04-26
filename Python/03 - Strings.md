[[Dev-Notes/Python/00 - Intro]]
[[01 - Variables, Built-in Functions]]
[[02 - Operators]]

## Strings

Text is a string data type. Any data type written as text is a string. Any data under single, double or triple quote are strings.

``` Python
letter = 'P'                # A string could be a single character or a bunch of texts
print(letter)               # P
greeting = 'Hello, World!'  # String could be made using a single or double quote,"Hello, World!"
print(greeting)             # Hello, World!
```

Multiline string is created by using triple single (''') or triple double quotes (""")

``` Python
multiline_string = '''I am a teacher and enjoy teaching.
I didn't find anything as rewarding as empowering people.
That is why I created 30 days of python.'''
print(multiline_string)
```

### String Concatenation

``` Python
first_name = 'Asabeneh'
last_name = 'Yetayeh'
space = ' '
full_name = first_name + space + last_name
print(full_name) # Asabeneh Yetayeh
```

### Escape Sequences in Strings

In Python and other programming languages \ followed by a character is an escape sequence.

| Code | Result           |
|:----:| ---------------- |
|  \n  | New line         |
|  \r  | Carriage Return  |
|  \t  | Tab space        |
|  \b  | Backspace        |
|  \f  | Form Feed        |
| \\\  | Back slash       |
| \\'  | Single quote (') |
| \\"  | Double quote (") |
| \ooo | Octal value      |
| \xhh | Hex value        |

### String formatting

#### Old Style String Formatting (% Operator)

In Python there are many ways of formatting strings. The "%" operator is used to format a set of variables enclosed in a "tuple" (a fixed size list), together with a format string, which contains normal text together with "argument specifiers", special symbols like "%s", "%d", "%f", "%.number of digitsf".

-   %s - String (or any object with a string representation, like numbers)
-   %d - Integers
-   %f - Floating point numbers
-   "%.number of digitsf" - Floating point numbers with fixed precision

``` Python
# Strings only
first_name = 'Asabeneh'
last_name = 'Yetayeh'
language = 'Python'
formated_string = 'I am %s %s. I teach %s' %(first_name, last_name, language)
print(formated_string)

# Strings  and numbers
radius = 10
pi = 3.14
area = pi * radius ** 2
formated_string = 'The area of circle with a radius %d is %.2f' %(radius, area) # 2 refers the 2 significant digits after the point

python_libraries = ['Django', 'Flask', 'NumPy', 'Matplotlib','Pandas']
formated_string = 'The following are python libraries:%s' % (python_libraries)
print(formated_string) # "The following are python libraries:['Django', 'Flask', 'NumPy', 'Matplotlib','Pandas']"
```

#### New Style String Formatting (str.format)

This formatting is introduced in Python version 3

``` Python
first_name = 'Asabeneh'
last_name = 'Yetayeh'
language = 'Python'
formated_string = 'I am {} {}. I teach {}'.format(first_name, last_name, language)
print(formated_string)

a = 4
b = 3

print('{} + {} = {}'.format(a, b, a + b)
print('{} / {} = {:.2f}'.format(a, b, a / b)) # limits it to two digits after decimal
```

#### String Interpolation / f-Strings (Python 3.6+)

Another new string formatting is string interpolation, f-strings. Strings start with f and we can inject the data in their corresponding positions

``` Python
a = 4
b = 3
print(f'{a} + {b} = {a + b}')
print(f'{a} / {b} = {a / b:.2f}')
```

### Python Strings as Sequences of Characters

``` Python
language = 'Python'
a,b,c,d,e,f = language # unpacking sequence characters into variables
print(a) # P
print(b) # y
print(c) # t
print(d) # h
print(e) # o
print(f) # n
```

#### Accessing Characters in Strings by Index

``` Python
language = 'Python'
first_letter = language[0]
print(first_letter) # P
last_index = len(language) - 1
last_letter = language[last_index]
print(last_letter) # n
```

If we want to start from right end we can use negative indexing. -1 is the last index

``` Python
language = 'Python'
last_letter = language[-1]
print(last_letter) # n
second_last = language[-2]
print(second_last) # o
```

#### Slicing Python Strings

In python we can slice strings into substrings

``` Python
language = 'Python'
first_three = language[0:3] # starts at zero index and up to 3 but not include 3
print(first_three) #Pyt
last_three = language[3:6]
print(last_three) # hon
# Another way
last_three = language[-3:]
print(last_three)   # hon
last_three = language[3:]
print(last_three)   # hon
```

#### Skipping Characters While Slicing

It is possible to skip characters while slicing by passing step argument to slice method.

``` Python
language = 'Python'
pto = language[0:6:2] #
print(pto) # Pto
```

#### Reversing a String

We can easily reverse strings in python

``` Python
greeting = 'Hello, World!'
print(greeting[::-1]) # !dlroW ,olleH
```

### String Methods

