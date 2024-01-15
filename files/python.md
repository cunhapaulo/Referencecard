## 1. Data Types


There are four collection data types in the Python programming language:

|       Nome       |             Exemplo             | Odered | Indexed | Changeable | Duplicates |
| :--------------: | :------------------------------ | :----: | :-----: | :--------: | :--------: |
|       **`List`** | `["a", "b", "c"]`               |  yes   |   yes   |    yes     |    yes     |
| **`Dictionary`** | `{'nome': 'John', 'idade': 30}` |  yes   |   yes   |    yes     |     no     |
|      **`Tuple`** | `(1, 'dois', 3.0)`              |  yes   |   yes   |     no     |    yes     |
|        **`Set`** | `{"apple", "banana", "cherry"}` |   no   |   no    |     no     |     no     |


## 2. **Listas** 
   Em Python, as listas são representadas por colchetes (`[]`). Elas são estruturas de dados **mutáveis**, o que significa que você pode modificar, adicionar ou remover elementos. As listas podem conter uma variedade de tipos de dados, incluindo números, strings e até mesmo outras listas.

   Exemplo:
   ```python
   minha_lista = [1, 2, 'três', [4, 5]]
   ```

Algumas das principais funções e métodos disponíveis em Python para trabalhar com listas. Esta lista não é exaustiva, mas abrange muitas das operações comuns. Aqui estão elas:

1. **Funções básicas:**
   - `len(lista)`: Retorna o comprimento da lista.
   - `max(lista)`: Retorna o elemento com o valor máximo na lista.
   - `min(lista)`: Retorna o elemento com o valor mínimo na lista.
   - `sum(lista)`: Retorna a soma de todos os elementos da lista.

2. **Métodos de modificação:**
   - `lista.append(elemento)`: Adiciona um elemento ao final da lista.
   - `lista.extend(iterável)`: Adiciona os elementos do iterável ao final da lista.
   - `lista.insert(posição, elemento)`: Insere um elemento em uma posição específica.
   - `lista.remove(elemento)`: Remove a primeira ocorrência do elemento na lista.
   - `lista.pop([índice])`: Remove e retorna o elemento na posição especificada (ou o último, se nenhum índice for fornecido).
   - `lista.clear()`: Remove todos os elementos da lista.

3. **Métodos de pesquisa:**
   - `lista.index(elemento)`: Retorna o índice da primeira ocorrência do elemento.
   - `elemento in lista`: Retorna `True` se o elemento estiver na lista, caso contrário, `False`.
   - `lista.count(elemento)`: Retorna o número de ocorrências do elemento na lista.

4. **Métodos de ordenação:**
   - `lista.sort()`: Ordena os elementos da lista in-place.
   - `lista.sort(key=str.lower)`: Ordena minúsculas primeiro.
   - `sorted(lista)`: Retorna uma nova lista ordenada, sem modificar a original.

5. **Métodos de cópia:**
   - `nova_lista = lista.copy()`: Cria uma cópia rasa da lista.
   - `nova_lista = list(lista)`: Cria uma nova lista com os mesmos elementos.

6. **Métodos de fatiamento e manipulação:**
   - `lista[start:stop]`: Retorna uma sublista a partir do índice `start` até `stop-1`.
   - `lista[start:stop:step]`: Retorna uma sublista com um passo específico.

Estas são apenas algumas das funções e métodos disponíveis para listas em Python. A linguagem é rica em recursos, permitindo uma manipulação versátil de estruturas de dados. Se precisar de mais detalhes sobre algum método específico ou tiver outras dúvidas, fique à vontade para perguntar!

## 3. **Dicionários:** `{'nome': 'John', 'idade': 30, 'cidade': 'Example'}`
   Dicionários em Python são representados por chaves (`{}`). Eles são estruturas de dados que armazenam pares chave-valor, permitindo que você associe um valor a uma chave específica. Dicionários são úteis para mapear informações de forma eficiente.

   Exemplo:
   ```python
   meu_dicionario = {'nome': 'John', 'idade': 30, 'cidade': 'Example'}
   ```

Algumas das principais funções e métodos disponíveis em Python para trabalhar com dicionários. Aqui estão elas:

1. **Operações básicas:**
   - `len(dicionario)`: Retorna o número de itens no dicionário.
   - `chave in dicionario`: Retorna `True` se a chave estiver presente no dicionário, caso contrário, `False`.
   - `dicionario.keys()`: Retorna uma lista de todas as chaves no dicionário.
   - `dicionario.values()`: Retorna uma lista de todos os valores no dicionário.
   - `dicionario.items()`: Retorna uma lista de tuplas (chave, valor) para cada item no dicionário.

2. **Métodos de modificação:**
   - `dicionario[chave] = valor`: Adiciona ou atualiza um item no dicionário.
   - `dicionario.update(dicionario2)`: Adiciona os itens de `dicionario2` ao dicionário.
   - `dicionario.pop(chave)`: Remove e retorna o valor associado à chave.
   - `dicionario.popitem()`: Remove e retorna o último par chave-valor inserido.
   - `dicionario.clear()`: Remove todos os itens do dicionário.

3. **Acesso seguro a valores:**
   - `dicionario.get(chave)`: Retorna o valor associado à chave, ou `None` se a chave não existir.
   - `dicionario.setdefault(chave, valor_padrao)`: Retorna o valor associado à chave, adicionando a chave com um valor padrão se não existir.

4. **Cópias e Views:**
   - `novo_dicionario = dicionario.copy()`: Cria uma cópia rasa do dicionário.
   - `nova_view_chaves = dicionario.keys()`: Retorna uma visão (view) das chaves no dicionário.
   - `nova_view_valores = dicionario.values()`: Retorna uma visão dos valores no dicionário.
   - `nova_view_itens = dicionario.items()`: Retorna uma visão dos pares chave-valor no dicionário.

Estas são apenas algumas das funções e métodos disponíveis para dicionários em Python. A linguagem oferece uma ampla gama de funcionalidades para manipulação eficiente de dicionários. Se precisar de mais detalhes sobre algum método específico ou tiver outras dúvidas, sinta-se à vontade para perguntar!

##  4. **Tuplas:** `(1, 'dois', 3.0)`
   As tuplas são representadas por parênteses (`()`). Ao contrário das listas, **as tuplas são imutáveis**, ou seja, após criadas, seus elementos não podem ser alterados. Elas são geralmente utilizadas para armazenar coleções de dados relacionados.

   Exemplo:
   ```python
   minha_tupla = (1, 'dois', 3.0)
   ```

Olá [User], vou listar exaustivamente algumas das principais funções e operações disponíveis em Python para trabalhar com tuplas. Assim como com as listas, esta lista não é exaustiva, mas abrange muitas das operações comuns. Aqui estão elas:

1. **Funções básicas:**
   - `len(tupla)`: Retorna o número de elementos na tupla.
   - `max(tupla)`: Retorna o elemento com o valor máximo na tupla.
   - `min(tupla)`: Retorna o elemento com o valor mínimo na tupla.
   - `sum(tupla)`: Retorna a soma de todos os elementos da tupla.

2. **Operações básicas:**
   - `tupla1 + tupla2`: Concatenação de tuplas.
   - `tupla * n`: Repete a tupla `n` vezes.

3. **Operações de pesquisa:**
   - `elemento in tupla`: Retorna `True` se o elemento estiver na tupla, caso contrário, `False`.
   - `tupla.index(elemento)`: Retorna o índice da primeira ocorrência do elemento.

4. **Desempacotamento de tupla:**
   - `(var1, var2, var3) = tupla`: Desempacota os elementos da tupla nas variáveis correspondentes.

5. **Métodos de contagem:**
   - `tupla.count(elemento)`: Retorna o número de ocorrências do elemento na tupla.

6. **Slicing (fatiamento):**
   - `tupla[start:stop]`: Retorna uma sub-tupla a partir do índice `start` até `stop-1`.
   - `tupla[start:stop:step]`: Retorna uma sub-tupla com um passo específico.

7. **Função `tuple()`:**
   - `nova_tupla = tuple(iterável)`: Converte um iterável (lista, string, etc.) em uma tupla.

Tuplas em Python **são imutáveis**, então as operações que modificam a estrutura da tupla, como adição ou remoção de elementos, não estão disponíveis. No entanto, as operações de pesquisa e manipulação de elementos são similares às das listas.

Se precisar de mais detalhes sobre algum método específico ou tiver outras dúvidas, fique à vontade para perguntar!


### 4.1. Percorrer itens de uma lista []:

```python
import pprint
import os

# ------------------------------------------------------------------------
# 
# 
# ------------------------------------------------------------------------
studentList = {"Paulo":  {"Tópicos de Filosofia Contemporânea": 10.0,
                          "Lógica II": 8.5,
                          "Ética II": 8.5,
                          "Filosofia Política II": 9.0},
               "Felipe": {"Tópicos de Filosofia Contemporânea": 6.5,
                          "Lógica II": 7.5,
                          "Tópicos de Filosofia Antiga": 7.5,
                          "Filosofia Moderna I": 7.5,
                          "Filosofia Política II": 5.0},
               "Mara":   {"Tópicos de Filosofia Contemporânea": 5.0,
                          "Lógica II": 5.5,
                          "Filosofia Política II": 5.0},
               "Moises": {"Tópicos de Filosofia Contemporânea": 5.0,
                          "Lógica II": 5.5,
                          "Metodologia da Pesquisa Filosófica I": 5.0,
                          "Filosofia da Linguagem": 5.0},
               }

# ------------------------------------------------------------------------
#
#
# ------------------------------------------------------------------------
def disciplinesList(enrollment):

    tempList = []

    # Extract all discipline names without repetition
    for student, disciplinList in enrollment.items():
        for disciplineName, grades in disciplinList.items():
            if disciplineName not in tempList:
                tempList.append(disciplineName)

    tempList.sort()
    return tempList

```



### 4.2. List 

![image](https://github.com/cunhapaulo/ReferenceCard/assets/28146759/15fbe08c-7a1a-4dec-9724-890590b5b898)

- Python will give you an `IndexError` error message if you use an index that exceeds the number of values in your list value.

#### 4.2.1. Getting a List from Another List with Slices:

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

#### 4.2.2. Program

```python
catNames = []

while True:
    print('Enter the name of cat ' + str(len(catNames) + 1) +
          ' (Or enter nothing to stop.):')
    name = input()
    if name == '':
        break
    catNames = catNames + [name] # list concatenation

print('The cat names are:')
for name in catNames:
    print(' ' + name)
```

#### 4.2.3. The `in` and `not in` Operators:

```python
    myPets = ['Zophie', 'Pooka', 'Fat-tail']
    print('Enter a pet name:')
    name = input()
    if name not in myPets:
        print('I do not have a pet named ' + name)
    else:
        print(name + ' is my pet.')
```

#### 4.2.4. The Multiple Assignment Trick

```python
    >>> cat = ['fat', 'gray', 'loud']
    >>> size, color, disposition = cat
```

#### 4.2.5. Using the `enumerate()` Function with Lists:

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

#### 4.2.6. Using the `random.choice()` and `random.shuffle()` Functions with Lists:

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

#### 4.2.7. Finding a Value in a List with the `index()` Method:

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

#### 4.2.8. Adding Values to Lists with the `append()` and `insert()` Methods:

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

#### 4.2.9. Removing Values from Lists with the `remove()` Method:

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

- Sorting the Values in a List with the `sort()` Method:
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


#### 4.2.10. Reversing the Values in a List with the `reverse()` Method:

```
>>> spam = ['cat', 'dog', 'moose']
>>> spam.reverse()
>>> spam
['moose', 'dog', 'cat']
```

- Program:

```python
import random

# EXCEPTIONS TO INDENTATION RULES IN PYTHON
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


###  4.3. `Dictionary`

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
        # pprint.pprint(k)
        # pprint.pprint(v)
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

### 4.4. `Tuple `

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

### 4.5. Converting Types with the list() and tuple() Functions:

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

## 5. Working with PDF and Word Documents

## 6. Working with CSV Files and JSON Data

## 7. Pattern Matching with Regular Expressions

## 8. Reading and Writing Files

## 9. Organizing Files

## 10. Web Scraping

## 11. Working with Excel Spreadsheets

## 12. Generalities

### 12.1. Strings:

```python
    myName = input()
    nameLength = len(myName) # length of a string
    print("Seu nome é " + myName + " que tem " + str(nameLength) + " caracteres."

    # str(54), int('54'), float('54.0')
```

### 12.2. Operators:

|  Op   |     Description     |
| :---: | :------------------ |
|  ==   | equal to            |
|  !=   | not equal to        |
|   <   | lower than          |
|   >   | greater than        |
|  <=   | lower or equal to   |
|  >=   | greater or equal to |
| True  | true                |
| False | false               |
|  not  | not                 |
|  and  | and                 |
|  or   | or                  |

### 12.3. Flow control statements

#### 12.3.1. `if` statement:

```python
# If statement
if name == 'Alice':
    print('Hi, Alice.')


# If Else statement:
if name == 'Alice':
    print('Hi, Alice.')
else:
    print('Hello, stranger.')


# Elif statement:
if name == 'Alice':
    print('Hi, Alice.')
elif age < 12:
    print('You are not Alice, kiddo.')
elif age > 100:
    print('You are not Alice, grannie.')
elif age > 2000:
    print('Unlike you, Alice is not an undead, immortal vampire.')
else:
    print('You are neither Alice nor a little kid.')
```

#### 12.3.2. `while` statement:

```python
# While loop statement
while True:
    print("Please, type you name.")
    name = input()
    if name != "Billy":
        continue
    print(Welcome back, Billy. Type your password")
    password = input()
    if password == "swordfish":
        break
print("Access granted.")

```

```python
name = ''
while not name:
    print('Enter your name:')
    name = input()
print('How many guests will you have?')
numOfGuests = int(input())
if numOfGuests:
    print('Be sure to have enough room for all your guests.')
print('Done')
```

#### 12.3.3. `for` statement:

**Observation**: `break` and `continue` allowed.

```python

print('My name is')
for i in range(5):
    print('Jimmy Five Times (' + str(i) + ')')

for i in range(0, 10, 2):  # 0 - start; 10 - end; 2 - step
    print(i)

for i in range(5, -1, -1):
    print(i)
```

### 12.4. Importing Modules:

```python
import random, sys, os, math

for i in range(5):
    print(random.randint(1, 10))
```

### 12.5. Ending a Program Early with the `sys.exit()` Function:

```python
import sys

while True:
    print('Type exit to exit.')
    response = input()
    if response == 'exit':
        sys.exit()
    print('You typed ' + response + '.')
```

### 12.6. A small program

```python

# This is a guess the number game.

import random

secretNumber = random.randint(1, 20)
print('I am thinking of a number between 1 and 20.')

# Ask the player to guess 6 times.
for guessesTaken in range(1, 7):
    print('Take a guess.')
    guess = int(input())

    if guess < secretNumber:
        print('Your guess is too low.')
    elif guess > secretNumber:
        print('Your guess is too high.')
    else:
        break # This condition is the correct guess!

if guess == secretNumber:
    print('Good job! You guessed my number in ' + str(guessesTaken) + 'guesses!')
else:
    print('Nope. The number I was thinking of was ' + str(secretNumber))
```

### 12.7. Exception handling:

```python
import time, sys

indent = 0 # How many spaces to indent.
indentIncreasing = True # Whether the indentation is increasing or not.

try:
    while True: # The main program loop.
        print(' ' * indent, end='')
        print('********')
        time.sleep(0.1) # Pause for 1/10 of a second.

        if indentIncreasing:
            # Increase the number of spaces:
            indent = indent + 1
            if indent == 10:
                # Change direction:
                indentIncreasing = False
        else:
            # Decrease the number of spaces:
            indent = indent - 1
            if indent == 0:
                # Change direction:
                indentIncreasing = True

except KeyboardInterrupt:
    sys.exit()
```
