[[00 - Intro]]
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

