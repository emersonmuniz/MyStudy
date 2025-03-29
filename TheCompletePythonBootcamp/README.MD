# The Complete Python Bootcamp

Platform: Udemy

Page: [https://www.udemy.com/course/complete-python-bootcamp/](https://www.udemy.com/course/complete-python-bootcamp/learn/lecture/9388518#overview)

Instructor: Jose Portilla

> This is my notes learning, it's for my 51 years old memory. It's not a course and not pretend to be. Just my notes. I really recommend to buy the course.
> 

***Note***: I'm trying to learn English too. So, sorry for any mistakes.

The official Python Notebook is on GitHub: https://github.com/Pierian-Data/Complete-Python-3-Bootcamp

---

**Table of Contents**

---

## Python Objects and Data Structure Basics

### **Python Data Types**

| **Name** | **Types** | **Description** |
| --- | --- | --- |
| Integers | int | 3, 300, 200 |
| Floating Point | float | 2.3, 4.6, 100.0 |
| Strings | str | “hello”, “word”, “test” |
| Lists | list | [10, “hello”, 200.3] |
| Dictionaries | dict | { "code":”2020”, “name":”Bob”} |
| Tuples | tup | (10, “hello”, 100.2) |
| Sets | set | {”a", “b”, “c”} |
| Bolleans | bool | T (true), F (false) |

---

### Arithmetic (Basic)

```python
# Addition
2+2
# Output: 4

# Subtraction
3-1
# Output: 2

# Multiplication
3*3
# Output: 9

# Division
5/2
# Output: 2.5

# Floor Division
7//3
# Output: 2
# The operador // truncates the decimal without rounding.

# Modulo
10%3
# Output: 1
# Remainder of ( 3*3=9, 10-9=1 )

# Powers
2**4
# Output: 16

# Order of Operations in Python
2+20*10+5
# Output: 207
# Always use ( )
(2+20) * (10+5)
# Output: 330
```

---

### Variables Assignments

Python use ***Dynamic*** ***Variables.***

**Pros**: Easy to work and faster

**Cons**: Mat result in unexpected bugs, need check using type()

**Note**: I prefer not use dynamic variables.

```python
# To assing use single equals sign to a object name
my_sons = 2
my_sons = ['Luiz', 'Thiago']

# Rules to name variable
# Can't start with a number (Ex: 1point = 1, Use: point1 = 1 _)
# There can be no space, use _ instead. ( Ex: doc num = 2, Use: doc_num = 2 )
# Can't use these symbols: :'",<>/?|\()!@#$%^&*~-+
# Can't use specian meaning in Python like "list"
# Avoid use single characters ( Who never used i in to loop? )

# Use object names easy to track the code
my_income = 1000
tax_rate = 0.1 # 0.1 represent direct 10% ( 10/100 )
my_taxes = my_income * tax_rate 
# Output: 100, Who like to pay taxes ?

# Best practice (PEP8), use lowercase with underscores

# You can check the variable type
my_age = 51
type( my_age ) # Output: int
```

---

### Strings

Use strings to record text information, like name.

```python
# Single quote
'Emerson'
'Emerson Muniz'

# Double quotes
"Emerson"
"Emerson Muniz"

# This create an error
'I'm tired'
# Output: SyntaxError

# The correct use
"I'm tired"

# Print strings
print( 'Emerson Muniz' )
# Output: Emerson Muniz

# \n is the scape character
print( "Emerson \n Muniz")
# Output: Emerson
#           Muniz

```

**Length**:

```python
len("Emerson Muniz")
# Output: 13
```

**Indexing**:

String index is like array. Normal and reverse.

```python
s = "Emerson Muniz"
# Like array start in 0, position 0=E, 1=m...

# Slicing Strings [starts:stop:step]

# Return position 0
s[0]
# Output: E
s[2]
# Output: e
s[1:]
# Output: merson Muniz
s[:3]
# Output: Eme
s[:]
# Output: Emerson Muniz
s[-1]
# Output: z
s[:-1]
# Output: Emerson Muni
s[::2]
# Output: EesnMnz
s[::-1]
# Output: zinuM nosremE
```

**Concatenating strings:**

```python
# Using +
s + ' from Brazil'
# Output: Emerson Muniz from Brazil

s
# Output: Emerson Muniz

# Reassign
s = s + ' from Brazil'
# Output: Emerson Muniz from Brazil

s
# Output: Emerson Muniz from Brazil

# Creating Repetition
letters = 'EM '
letters*10
# Output: EM EM EM EM EM EM EM EM EM EM
```

**String methods:**

```python
s
# Output: Emerson Muniz from Brazil

# Upper case
s.upper()
# Output: EMERSON MUNIZ FROM BRAZIL

# Lower case
s.lower()
# Output: emerson jose from brazil

# Split
s.split()
# Output: ['Emerson', 'Muniz', 'from', 'Brazil']

# Split by a specific element
s.split('f')
# Output: ['Emerson Muniz ', 'rom Brazil']

```

Print Formatting:

```python
'Insert another string using brackets: {}'.format(' Just it' )
# Output: 'Insert another string using brackets:  Just it'

# Number is number, string is string
3 + 3
# Output: 6
'3' + '3'
# Output: 33

# Formating in sequence
print('Emerson likes {}, {} and {}.'.format('beer', 'whiskey', 'barbecue'))
# Output: Emerson likes beer, whiskey and barbecue.

# Formating using position. First position 0.
print('Emerson likes {2}, {0} and {1}.'.format('beer', 'whiskey', 'barbecue'))
# Output: Emerson likes barbecue, beer and whiskey.

# Using name object instead sequence number.
print('Emerson likes {c}, {b} and {b}.'.format(a='beer', b='whiskey', c='barbecue'))
# Output: Emerson likes barbecue, whiskey and whiskey.
# Yah.. I prefer Whiskey ;)

# Float formating
x = 1000/700
print('The result was {}'.format(x))
# Result: The result was 1.4285714285714286
print('The result was {r:1.3f}'.format(r=x))
# Output: The result was 1.429
print('The result was {r:10.3f}'.format(r=x))
# Output: The result was      1.429
print('The result was {r:3.2f}'.format(r=x))
# Output: The result was 1.43
	
# Using variables
name = 'Emerson'
age = 51
print("Hello, my name is {name} and I'm {age} years old")
# Output: Hello, my name is Emerson and I'm 51 years old

```