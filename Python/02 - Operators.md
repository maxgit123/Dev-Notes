## Operators

Python language supports several types of operators. Here is a few of them:

### Arithmetic Operators

| Operator | Name           | Example |
|:--------:| -------------- | ------- |
|    +     | Addition       | x + y   |
|    -     | Subtraction    | x - y   |
|    *     | Multiplication | x * y   |
|    /     | Division       | x / y   |
|    %     | Modulus        | x % y   |
|    **    | Exponentiation | x ** y  |
|    //    | Floor division | x // y  |

### Assignment Operators

| Operator | Example   | Same As      |
|:--------:|:--------- |:------------ |
|    =     | x = 5     | x = 5        |
|    +=    | x += 3    | x = x + 3    |
|    -=    | x -= 3    | x = x - 3    |
|   \*=    | x \*= 3   | x = x \* 3   |
|    /=    | x /= 3    | x = x / 3    |
|    %=    | x %= 3    | x = x % 3    |
|   //=    | x //= 3   | x = x // 3   |
|  \*\*=   | x \*\*= 3 | x = x \*\* 3 |
|    &=    | x &= 3    | x = x & 3    |
|   \|=    | x \|= 3   | x = x \| 3   |
|    ^=    | x ^= 3    | x = x ^ 3    |
|   \>>=   | x >>= 3   | x = x >> 3   |
|   <<=    | x <<= 3   | x = x << 3   |

### Comparison Operators

| Operator | Name                     | Example |
|:--------:| ------------------------ | ------- |
|    ==    | Equal                    | x == y  |
|    !=    | Not equal                | x != y  |
|    \>    | Greater than             | x > y   |
|    <     | Less than                | x < y   |
|   \>=    | Greater than or equal to | x >= y  |
|    <=    | Less than or equal to    | x <= y  |

```Python
print(3 > 2)                            # True, because 3 is greater than 2
print(len('mango') == len('avocado'))   # False
print('True == False: ', True == False) # False
```

### Identity Operators

Identity operators are used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location

| Operator | Description                                            | Example    |
| -------- | ------------------------------------------------------ | ---------- |
| is       | Returns True if both variables are the same object     | x is y     |
| is not   | Returns True if both variables are not the same object | x is not y |

``` Python
print('1 is 1', 1 is 1)                   # True - because the data values are the same
print('1 is not 2', 1 is not 2)           # True - because 1 is not 2
```

### Membership Operators

Membership operators are used to test if a sequence is presented in an objec

| Operator | Description                                                                      | Example    |
| -------- | -------------------------------------------------------------------------------- | ---------- |
| in       | Returns True if a sequence with the specified value is present in the object     | x in y     |
| not in   | Returns True if a sequence with the specified value is not present in the object | x not in y |


``` Python
print('A in Asabeneh', 'A' in 'Asabeneh') # True - A found in the string
print('B in Asabeneh', 'B' in 'Asabeneh') # False - there is no uppercase B
print('coding' in 'coding for all')       # True - because coding for all has the word coding
print('a in an:', 'a' in 'an')            # True
print('4 is 2 ** 2:', 4 is 2 ** 2)        # True
```

### Logical Operators

Unlike other programming languages python uses keywords _and_, _or_ and _not_ for logical operators. Logical operators are used to combine conditional statements:

| Operator | Description                                             | Example                |
|:--------:| ------------------------------------------------------- | ---------------------- |
|   and    | Returns True if both statements are true                | x < 5 and  x < 10      |
|    or    | Returns True if one of the statements is true           | x < 5 or x < 4         |
|   not    | Reverse the result, returns False if the result is true | not (x < 5 and x < 10) |

``` Python
print(3 > 2 and 4 > 3) # True - because both statements are true
print('True and True: ', True and True)
print(3 < 2 or 4 < 3)  # False - because both statements are false
print('True or False:', True or False)
print(not 3 > 2)     # False - because 3 > 2 is true, then not True gives False
print(not True)      # False - Negation, the not operator turns true to false
print(not not False) # False
```

### Python Bitwise Operators

Bitwise operators are used to compare (binary) numbers

| Operator | Name                 | Description                                                                                             | Example |
|:--------:| -------------------- | ------------------------------------------------------------------------------------------------------- | ------- |
|    &     | AND                  | Sets each bit to 1 if both bits are 1                                                                   | x & y   |
|    \|    | OR                   | Sets each bit to 1 if one of two bits is 1                                                              | x \| y  |
|    ^     | XOR                  | Sets each bit to 1 if only one of two bits is 1                                                         | x ^ y   |
|    ~     | NOT                  | Inverts all the bits                                                                                    | ~x      |
|    <<    | Zero fill left shift | Shift left by pushing zeros in from the right and let the leftmost bits fall off                        | x << 2  |
|   \>\>   | Signed right shift   | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off | x >> 2  |

## Operator Precedence

Operator precedence describes the order in which operations are performed

|                   Operator                   | Description                                           |
|:--------------------------------------------:| ----------------------------------------------------- |
|                      ()                      | Parentheses                                           |
|                      **                      | Exponentiation                                        |
|                  +x  -x  ~x                  | Unary plus, unary minus, and bitwise NOT              |
|                 *  /  //  %                  | Multiplication, division, floor division, and modulus |
|                     +  -                     | Addition and subtraction                              |
|                    <<  >>                    | Bitwise left and right shifts                         |
|                      &                       | Bitwise AND                                           |
|                      ^                       | Bitwise XOR                                           |
|                      \|                      | Bitwise OR                                            |
| ==  !=  >  >=  <  <=  is  is not  in  not in | Comparisons, identity, and membership operators       |
|                     not                      | Logical NOT                                           |
|                     and                      | AND                                                   |
|                      or                      | OR                                                    |

