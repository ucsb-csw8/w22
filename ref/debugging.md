---
layout: home
title: 🐛&nbsp;&nbsp; Debugging 
parent: References
nav_order: 3
seo:
  type: Resource
  name: Debugging scenarios and solutions
---

# 🐛 Debugging scenarios and solutions
The majority of this cases were provided by the students of previouse qarters. You are wellcome to contribute your errors as well.


## Case 1. `print`
*   Correct line of code: `print("Hello, World")`

### Syntax error
*   Error #1: `SyntaxError: unexpected EOF while parsing`
*   Erroneous code:
```py
print('Hello, World'
```
*   **Cause**:  Missing a closing parenthesis `)`.

### EOL
*   Error #2: `EOL while scanning string literal`
*   Erroneous code:
```py
print('Hello, World)
```
or
```py
print('Hello, World")
```
*   **Cause**:   Missing a **closing** quotation mark or a mismatched quotation mark (incorrectly placed quotation can also cause it).

### Syntax error
*   Error #3: `SyntaxError: invalid syntax`
*   Erroneous code:
```py
print(Hello World')
print'Hello World  
print(Hello World) # see also Error 4
```

*   **Cause**:   Missing **opening** quotation mark or **opening** parenthesis or quotations around the text.

### Name Error
*   Error #4: `NameError: name 'Print' is not defined`
*   Erroneous code:
```py
Print('Hello, World')
```

*   **Cause**:   In this case, an accidentally capitalized name of the function. Generally, this error happens when a function name or a variable name is misspelled or have not been properly defined.

This error can also be caused if there is a **single word** (or comma-separated words) inside the `print` that needed to be displayed as the literal text but does not include quotation marks around it (similar to Error #3).

*   Erroneous code: 
```
print(Hello)
print(Hello, World)
```

generates the same error (`NameError: name 'Hello' is not defined`), since Python is now looking for a variable called `Hello`, since it doesn’t know that we just forgot to put quotation marks around the text.

### Syntax error
*   Error #5: `SyntaxError: unmatched ')'`
*   Erroneous code:
```py
print('Hello, World'))
```

*   **Cause**:  an extra **closing** parenthesis `)` that does not have a matching **opening** paren `(`.

### Strange print results
*   Error #6: Function Address gets printed - `<function function_name at 0x....> `
*   Erroneous code:
```py
def area(radius):
    return 3.14 * radius * radius
    
radius = float(input())
print(f"Circle has area {area} inches squared.")
```
*   **Cause**:  Calling function without the parameters in brackets ( ). For example, area function should be called as - **area(radius)**

## Case 2. Dictionary
*   Correct code: 
```py
dict1 = {"A":1, "B":2, "C":3}
print(dict1["A"])
```
### NameError
*   Error #1: `NameError: name 'A' is not defined`
*   Erroneous code:
```py
dict1 = {"A":1, "B":2, "C":3}
print(dict1[A])
```
*   **Cause**:  Missing quotation marks (" ") when calling a key from dictionary.


## Case 4. `print` with indents
*   Correct code: 
```py
print("Hello world!")
print("What a nice day!")
```
### Indentation Error
*   Error #1: `IndentationError: unexpected indent`
*   Erroneous code:
```py
print("Hello world!")
    print("What a nice day!")
```
*   **Cause**:   Indented even though it is not necessary. 


## Case 5. Function definitions
*   Correct code: 
```py
def first_name(old_name, new_name):
```
### Syntax Error
*   Error #1: `SyntaxError: invalid syntax`
*   Erroneous code:
```py
def first_name(old_name, new_name)
```
*   **Cause**:   Missing a colon in the end.

***Instructor note:*** Look for simular errors in `for ... :` and `if ...:` and `while ... :` lines :) Or any block indent required lines (when next line will be with block indent) They always go together - `:` and following block indent.

## Case 6. Tricky f-strings
*   Correct code: 
```py
print(f'Number of {legs:b}')
```
### Syntax Error
*   Error #1: `SyntaxError: invalid syntax`
*   Erroneous code:
```py
print(f'Number of {legs:b')
```
*   **Cause**:   Did not end f-string argument with a ‘}’



## Case 6. String concatenation
*   Correct code: 
```py
num = 6
print("I would like " + str(num) + " tacos please.")
```
### Type Error
*   Error #1: `TypeError`
*   Erroneous code:
```py
num = 6
print("I would like " + num + " tacos please.")
```
*   **Cause**:    You can only concatenate a string, not an interger type with a string. 


## Case 7. Variables inside the functions
*   Correct code: 
```py
def vol(height):
  if height == 3:
    lenght = 2
    return lenght
  else:
    lenght = 4
    return lenght

if __name__ == "__main__":
  provided_height = input()
  num = vol(provided_height)
  print(num)
```
### Name Error
*   Error #1: `name 'lenght' is not definded.`
*   Erroneous code:
```py
def vol(lenght):
  if height == 3:
    lenght = 2
    return lenght
  else:
    lenght = 4
    return lenght

if __name__ == "__main__":
  provided_height = input()
  num = vol(provided_height)
  print(num)
```
*   **Cause**:    I should use the NAME which appeared in the IF branch as Argument Name.


## Case 8. Float or intreger conversion?
*   Correct code: 
```py
current_year = '1792'
current_year = int(current_year)
print(current_year)
```
or 
```py
current_year = '1792.99'
current_year = float(current_year)
print(current_year)
```
### ValueError
*   Error #1: `ValueError: invalid literal for int() with base 10: '1792.99'`
*   Erroneous code:
```py
current_year = '1792.99'
current_year = int(current_year)
print(current_year)
```
*   **Cause**:   If you do want to pass a string representation of a float to an int,  you need to convert to a float first, then to an integer.


---

#### Acknowledgement

Developed by Yekaterina Kharitonova with assistance from students and course mentors.
Students that provided examples above:
- Ruopu Bai
- Hanwen Zhang
- Natalya Rodriguez
- James McNeice
- Francisco Silva
- Mu Niu

{: .fs-2 }
