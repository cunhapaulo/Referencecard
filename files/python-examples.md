Python language reference
- [Definitions of Python Language](https://github.com/cunhapaulo/ReferenceCard/wiki/Python)

# 1. Index

- [1. Index](#1-index)
- [2. Data Structures](#2-data-structures)
  - [2.1. List](#21-list)
    - [2.1.1. Getting a List from Another List with Slices:](#211-getting-a-list-from-another-list-with-slices)
    - [2.1.2. Program](#212-program)
    - [2.1.3. The `in` and `not in` Operators:](#213-the-in-and-not-in-operators)
    - [2.1.4. The Multiple Assignment Trick](#214-the-multiple-assignment-trick)
    - [2.1.5. Using the `enumerate()` Function with Lists:](#215-using-the-enumerate-function-with-lists)
    - [2.1.6. Using the `random.choice()` and `random.shuffle()` Functions with Lists:](#216-using-the-randomchoice-and-randomshuffle-functions-with-lists)
    - [2.1.7. Finding a Value in a List with the `index()` Method:](#217-finding-a-value-in-a-list-with-the-index-method)
    - [2.1.8. Adding Values to Lists with the `append()` and `insert()` Methods:](#218-adding-values-to-lists-with-the-append-and-insert-methods)
    - [2.1.9. Removing Values from Lists with the `remove()` Method:](#219-removing-values-from-lists-with-the-remove-method)
    - [2.1.10. Sorting the Values in a List with the `sort()` Method:](#2110-sorting-the-values-in-a-list-with-the-sort-method)
    - [2.1.11. Reversing the Values in a List with the `reverse()` Method:](#2111-reversing-the-values-in-a-list-with-the-reverse-method)
      - [Program:](#program)
  - [2.2. `Dictionary`](#22-dictionary)
  - [2.3. `Tuple `](#23-tuple-)
  - [2.4. Converting Types with the list() and tuple() Functions:](#24-converting-types-with-the-list-and-tuple-functions)
- [3. Special Uses](#3-special-uses)
  - [3.1. Working with PDF and Word Documents](#31-working-with-pdf-and-word-documents)
  - [3.2. Working with CSV Files and JSON Data](#32-working-with-csv-files-and-json-data)
  - [3.3. Pattern Matching with Regular Expressions](#33-pattern-matching-with-regular-expressions)
  - [3.4. Reading and Writing Files](#34-reading-and-writing-files)
  - [3.5. Organizing Files](#35-organizing-files)
  - [3.6. Web Scraping](#36-web-scraping)
  - [3.7. Working with Excel Spreadsheets](#37-working-with-excel-spreadsheets)
  - [3.8. Generalities](#38-generalities)

# 2. Data Structures

## 2.1. List 

![image](https://github.com/cunhapaulo/ReferenceCard/assets/28146759/15fbe08c-7a1a-4dec-9724-890590b5b898)

- Python will give you an `IndexError` error message if you use an index that exceeds the number of values in your list value.

### 2.1.1. Getting a List from Another List with Slices:

![image](https://github.com/cunhapaulo/ReferenceCard/assets/28146759/68ae06e8-76a5-4f98-9b51-3243341315bb)

- Getting a List’s Length with the `len()` Function
- List Concatenation and List Replication with `+`
- Removing Values from Lists with `del` Statements

```python
    >>> spam = ['cat', 'bat', 'rat', 'elephant']
    >>> del spam[2]
    >>> spam
    ['cat', 'bat', 'elephant']
    >>> del spam[2]
    >>> spam
    ['cat', 'bat']
```

### 2.1.2. Program

```python
catNames = []

while True:
    print('Enter the name of cat ' + str(len(catNames) + 1) +
          ' (Or enter nothing to stop.):')
    name = input()
    if name == '':
        break
    catNames = catNames + [name]  list concatenation

print('The cat names are:')
for name in catNames:
    print(' ' + name)
```

### 2.1.3. The `in` and `not in` Operators:

```python
    myPets = ['Zophie', 'Pooka', 'Fat-tail']
    print('Enter a pet name:')
    name = input()
    if name not in myPets:
        print('I do not have a pet named ' + name)
    else:
        print(name + ' is my pet.')
```

### 2.1.4. The Multiple Assignment Trick

```python
    >>> cat = ['fat', 'gray', 'loud']
    >>> size, color, disposition = cat
```

### 2.1.5. Using the `enumerate()` Function with Lists:

Instead of using the range(len(someList)) technique with a for loop to obtain 
the integer index of the items in the list, you can call the `enumerate()` function instead.

```
>>> supplies = ['pens', 'staplers', 'flamethrowers', 'binders']
>>> for index, item in enumerate(supplies):
... print('Index ' + str(index) + ' in supplies is: ' + item)
Index 0 in supplies is: pens
Index 1 in supplies is: staplers
Index 2 in supplies is: flamethrowers
Index 3 in supplies is: binders
```

Instead of using the range(len(someList)) technique with a for loop to obtain
the integer index of the items in the list, you can call the enumerate() function
instead. On each iteration of the loop, enumerate() will return two
values: the index of the item in the list, and the item in the list itself.

### 2.1.6. Using the `random.choice()` and `random.shuffle()` Functions with Lists:

```python
>>> import random
>>> pets = ['Dog', 'Cat', 'Moose']
>>> random.choice(pets)
'Dog'
>>> random.choice(pets)
'Cat'
>>> random.choice(pets)
'Cat'

------------------------------------------------------

>>> import random
>>> people = ['Alice', 'Bob', 'Carol', 'David']
>>> random.shuffle(people)
>>> people
['Carol', 'David', 'Alice', 'Bob']
>>> random.shuffle(people)
>>> people
['Alice', 'David', 'Bob', 'Carol']
```

### 2.1.7. Finding a Value in a List with the `index()` Method:

```
>>> spam = ['hello', 'hi', 'howdy', 'heyas']
>>> spam.index('hello')
0
>>> spam.index('heyas')
3
>>> spam.index('howdy howdy howdy')
Traceback (most recent call last):
File "<pyshell#31>", line 1, in <module>
spam.index('howdy howdy howdy')
ValueError: 'howdy howdy howdy' is not in list
```
**Important**: When there are duplicates of the value in the list, the index of its first
appearance is returned.

### 2.1.8. Adding Values to Lists with the `append()` and `insert()` Methods:

```
>>> spam = ['cat', 'dog', 'bat']
>>> spam.append('moose')
>>> spam
['cat', 'dog', 'bat', 'moose']

------------------------------------------------

>>> spam = ['cat', 'dog', 'bat']
>>> spam.insert(1, 'chicken')
>>> spam
['cat', 'chicken', 'dog', 'bat']
```

### 2.1.9. Removing Values from Lists with the `remove()` Method:

```
>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam.remove('bat')
>>> spam
['cat', 'rat', 'elephant']

-------------------------------------------------

>>> spam = ['cat', 'bat', 'rat', 'elephant']
>>> spam.remove('chicken')
Traceback (most recent call last):
File "<pyshell#11>", line 1, in <module>
spam.remove('chicken')
ValueError: list.remove(x): x not in list

-------------------------------------------------

>>> spam = ['cat', 'bat', 'rat', 'cat', 'hat', 'cat']
>>> spam.remove('cat')
>>> spam
['bat', 'rat', 'cat', 'hat', 'cat']
```  

### 2.1.10. Sorting the Values in a List with the `sort()` Method:
```
>>> spam = [2, 5, 3.14, 1, -7]
>>> spam.sort()
>>> spam
[-7, 1, 2, 3.14, 5]
>>> spam = ['ants', 'cats', 'dogs', 'badgers', 'elephants']
>>> spam.sort()
>>> spam
['ants', 'badgers', 'cats', 'dogs', 'elephants']

-------------------------------------------------

>>> spam.sort(reverse=True)
>>> spam
['elephants', 'dogs', 'cats', 'badgers', 'ants']

-------------------------------------------------

>>> spam = [1, 3, 2, 4, 'Alice', 'Bob']
>>> spam.sort()
Traceback (most recent call last):
File "<pyshell#70>", line 1, in <module>
spam.sort()
TypeError: '<' not supported between instances of 'str' and 'int'

-------------------------------------------------

>>> spam = ['Alice', 'ants', 'Bob', 'badgers', 'Carol', 'cats']
>>> spam.sort()
>>> spam
['Alice', 'Bob', 'Carol', 'ants', 'badgers', 'cats']

-------------------------------------------------

>>> spam = ['a', 'z', 'A', 'Z']
>>> spam.sort(key=str.lower)
>>> spam
['a', 'A', 'z', 'Z']

```


### 2.1.11. Reversing the Values in a List with the `reverse()` Method:

```
>>> spam = ['cat', 'dog', 'moose']
>>> spam.reverse()
>>> spam
['moose', 'dog', 'cat']
```

#### Program:

```python
import random

 EXCEPTIONS TO INDENTATION RULES IN PYTHON
messages = ['It is certain',
    'It is decidedly so',
    'Yes definitely',
    'Reply hazy try again',
    'Ask again later',
    'Concentrate and ask again',
    'My reply is no',

print(messages[random.randint(0, len(messages) - 1)])

```

```
>>> name = 'Zophie'


>>> name[0]
'Z'
>>> name[-2]
'i'
>>> name[0:4]
'Zoph'
>>> 'Zo' in name
True
>>> 'z' in name
False
>>> 'p' not in name
False

>>> for i in name:
... print('* * * ' + i + ' * * *')

* * * Z * * *
* * * o * * *
* * * p * * *
* * * h * * *
* * * i * * *
* * * e * * *
```


##  2.2. `Dictionary`

```python
import pprint
import os

allGuests = {
    'Alice': {'apples': 5, 'pretzels': 12},
    'Bob': {'ham sandwiches': 3, 'apples': 2},
    'Carol': {'cups': 3, 'apple pies': 1}
}


def totalBrought(guests, item):

    numBrought = 0

    for k, v in guests.items():
         pprint.pprint(k)
         pprint.pprint(v)
        numBrought += v.get(item, 0)
    return numBrought


os.system("cls")

print('Number of things being brought:')
print(' - Apples ' + str(totalBrought(allGuests, 'apples')))
print(' - Cups ' + str(totalBrought(allGuests, 'cups')))
print(' - Cakes ' + str(totalBrought(allGuests, 'cakes')))
print(' - Ham Sandwiches ' + str(totalBrought(allGuests, 'ham sandwiches')))
print(' - Apple Pies ' + str(totalBrought(allGuests, 'apple pies')))

```

- Result:

```
Number of things being brought:
- Apples 7
- Cups 3
- Cakes 0
- Ham Sandwiches 3
- Apple Pies 1
```


## 2.3. `Tuple `

The tuple data type is almost identical to the list data type, except in two ways.
First, tuples are typed with parentheses, ( and ), instead of square brackets,
[ and ]. For example, enter the following into the interactive shell:

```
>>> eggs = ('hello', 42, 0.5)
>>> eggs[0]
'hello'
>>> eggs[1:3]
(42, 0.5)
>>> len(eggs)
3
```
But the main way that tuples are different from lists is that tuples, like
strings, are **immutable**. Tuples cannot have their values modified, appended,
or removed. Enter the following into the interactive shell, and look at the
TypeError error message:

```
>>> eggs = ('hello', 42, 0.5)
>>> eggs[1] = 99
Traceback (most recent call last):
File "<pyshell#5>", line 1, in <module>
eggs[1] = 99
TypeError: 'tuple' object does not support item assignment
```

## 2.4. Converting Types with the list() and tuple() Functions:

Just like how `str(42)` will return '42', the string representation of the integer
`42`, the functions `list()` and `tuple()` will return list and tuple versions of the
values passed to them: 

```
>>> tuple(['cat', 'dog', 5])
('cat', 'dog', 5)
>>> list(('cat', 'dog', 5))
['cat', 'dog', 5]
```

- Important:
```
>>> list("This is a Program")
['T', 'h', 'i', 's', ' ', 'i', 's', ' ', 'a', ' ', 'P', 'r', 'o', 'g', 'r', 'a', 'm']
```
Converting a tuple to a list is handy if you need a mutable version of a
tuple value.


# 3. Special Uses

## 3.1. Working with PDF and Word Documents
## 3.2. Working with CSV Files and JSON Data
## 3.3. Pattern Matching with Regular Expressions
## 3.4. Reading and Writing Files
## 3.5. Organizing Files
## 3.6. Web Scraping
## 3.7. Working with Excel Spreadsheets
## 3.8. Generalities

