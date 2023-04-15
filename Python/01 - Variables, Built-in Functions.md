## Built in functions

Built-in functions are globally available for your use that mean you can make use of the built-in functions without importing or configuring. List of Built-in functions: [python documentation](https://docs.python.org/3.11/library/functions.html)

``` Python
print('Hello, World!')  # it prints the text value Hello, World!
len('Hello, World!')    # it counts the number of characters including space
type('Hello, World!')   # it checks the data type
str(10)    # it converts number to string
int('10')  # it converts to number
float (10) # it converts integer to decimal
input('Enter your name:') # it takes user input
```

```Python
min(20, 30, 40, 50)   # gives the minimun value
max(20, 30, 40, 50)   # gives the maximum value
min([20, 30, 40, 50]) # it takes list as an argument and return min
max([20, 30, 40, 50]) # it takes list as an argument and return max
sum([20, 30, 40, 50]) # it takes only list as an argument and return the sum
```

## Variables

Mnemonic variables are recommended to use in many programming languages. A mnemonic variable is a variable name that can be easily remembered and associated.
Python developers use snake case (snake_case) variable naming convention.

Python variable name rules

-   A variable name must start with a letter or the underscore character.
-   A variable name cannot start with a number.
-   A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ ).
-   Variable names are case-sensitive (firstname, Firstname, FirstName and FIRSTNAME) are different variables).

Let us se valid variable names:

```Python
firstname
age
country
last_name
capital_city
_if # if we want to use reserved word as a variable
year_2021
year2021
current_year_2021
birth_year
num1
```

Invalid variables names:

```Python
first-name
first@name
first$name
num-1
1num
```

Print function takes unlimited number of arguments. Example:

```Python
print('Hello',',','World','!') # it can take multiple arguments, four arguments have been passed
```

Print and also find the length of the variables declared. Example:

```Python
first_name = 'Asabeneh'
is_married = True
skills = ['HTML', 'CSS', 'JS', 'React', 'Python']
person_info = {
   'firstname':'Asabeneh',
   'lastname':'Yetayeh',
   'country':'Finland',
   'city':'Helsinki'
}

# Printing the values stored in the variables

print('First name:', first_name)
print('First name length:', len(first_name))
print('Married: ', is_married)
print('Skills: ', skills)
print('Person information: ', person_info)
```

### Declaring Multiple Variable in a Line

Multiple variables can also be declared in one line:

```Python
first_name, last_name, country, age, is_married = 'Asabeneh', 'Yetayeh', 'Helsink', 250, True

print(first_name, last_name, country, age, is_married)
```

Getting user input using the _input()_ built-in function. Let us assign the data we get from a user into first_name and age variables. Example:

``` Python
first_name = input('What is your name: ')
print(first_name)
```

## Data Types

Casting: Converting one data type to another data type.

```Python
gravity = '9.81'

print('num_int: ', int(float(gravity)))      # 9
print('num_float: ', float(gravity))         # 9.81
gravity_to_list = list(gravity)
print(gravity_to_list)                       # ['9', '.', '8', '1']
```