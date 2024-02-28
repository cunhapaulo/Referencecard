# Python

## Interesting sites about REGEXP:

- [Site para testar `RegExp` para Phyton](https://pythex.org/)
- [Regexone](https://regexone.com/)
- [Regex Classes](https://regexlearn.com/)
  - [Regex Classes 101](https://regexlearn.com/learn/regex101)

## Código Python para usar regexp:

```python

import re

def main():

    # creates an regexp operator with the proper pattern
    # ATTENTION: use an raw string begining with 'r'

    cepREGEXP = re.compile(r"((\d{2})[.]*(\d{3})-(\d{3}\b))")

    # captures the result of pattern matching

    result = cepREGEXP.search("Na minha cidade o CEP é 66.040-100 ou 66050-520")

    # uses patterns found

    print(f"1. First CEP found: {result.group()}")
    print(f"2. First CEP found: {result.groups()}")

    # Finds all ucurrences

    results = cepREGEXP.findall("Na minha cidade o CEP é 66.040-100 ou 66050-520")

    for cep in results:
        print(f"> CEP found: {cep}")

if __name__ == "__main__":
    # calls the main funtion
    main()

```

- RESULT:

```
1.First CEP found: 66.040-100
2.First CEP found: ('66.040-100', '66', '040', '100')
> CEP found: ('66.040-100', '66', '040', '100')
> CEP found: ('66050-520', '66', '050', '520')
```

## Modelos de Expressões Regulares

|        Item         |               REGEXP               |                     Exemplo(s)                      |                            Parte(s)                            |
| :-----------------: | :--------------------------------: | :-------------------------------------------------: | :------------------------------------------------------------: |
| Endereço de e-mail  | `([\w\-.]+)@([\w\-]+\.\w+\.?\w*)`  |             `paulo.cunha.doc@gmail.com`             |               `(paulo.cunha.doc)`, `(gmail.com)`               |
|   CEP brasileiro    |   `(\d{2})[.]*(\d{3})-(\d{3}\b)`   |             `66050-520` ou `66.050-520`             |           `(66050)`, `(520)` ou `(66.050)`, `(520)`            |
| Telefone brasileiro | `([\(\d{2}\)]*) (\d{5})-(\d{4}\b)` |          `(91) 98113-5678` ou `98113-5678`          | `((91))`, `(98113)`, `(5678)` ou `(empty)` `(98113)`, `(5678)` |
|   Data dd/mm/yyyy   |    `\d{1,2}\/\d{1,2}\/\d{2,4}`     |                    `31/12/2023`                     |                          `31/12/2023`                          |
|   Data dd/mm/yyyy   | `(\d{1,2})\/(\d{1,2})\/(\d{2,4})`  |                    `31/12/2023`                     |                    `(31)`, `(12)`, `(2023)`                    |
| Números Americanos  |  `^-?\d+(,\d+)*(\.\d+(e\d+)?)?$`   | `3.14529`, `-255.34`, `1.9e10`, `123,340.00`, `128` |                                                                |
| Funções Python | `def\s+(\w+)\((.*)\):` | `def transverse_check(directory, pattern="*"):` | |
|        URIs         |  `^(\w+)://([\w\-\.]+)(:(\d+))?`   |                    figure below                     |                          figure below                          


![URI´s reached by regexp above](https://github.com/cunhapaulo/ReferenceCard/assets/28146759/498f777b-1ce4-411e-9d8e-3516300abdbc)


## Lookarounds

| Type                | Expression |   Example    | Result                         |
| :------------------ | :--------: | :----------: | :----------------------------- |
| Positive Lookahead  |   `(?=)`   | `\d+(?=PM)`  | Date: 4 Aug `3`PM              |
| Negative Lookahead  |   `(?!)`   | `\d+(?!PM)`  | Date: `4` Aug 3PM              |
| Positive Lookbehind |  `(?<=)`   | `(?<=\$)\d+` | Product Code: 1064 Price: $`5` |
| Negative Lookbehind |  `(?<!)`   | `(?<!\$)\d+` | Product Code: `1064` Price: $5 |

## Symbols

|   Symbol   | Use                               |
| :--------: | :-------------------------------- |
|    `.`     | any                               |
|    `?`     | optional (0 or 1)                 |
|    `^`     | not                               |
| `[a-zA-Z]` | range of character                |
|    `{}`    | repetition                        |
|   `{n}`    | n-occurences                      |
|  `{m,n}`   | from m to n occurences            |
|  `{m,n}?`  | from m to n occurences, the least |
|    `\`     | Escape character                  |
|    `^`     | begin of string                   |
|    `$`     | end of string                     |
|    `()`    | capture group                     |
|    `*`     | 0 or more                         |
|    `+`     | 1 or more                         |

## Classes of Characters

| Shorthand character class | Represents                                                                                            |
| :-----------------------: | :---------------------------------------------------------------------------------------------------- |
|           `\d`            | Any numeric digit from 0 to 9.                                                                        |
|           `\D`            | Any character that is NOT a numeric digit from 0 to 9.                                                |
|           `\w`            | Any letter, numeric digit, or the underscore character. Think of this as matching “word” characters.) |
|           `\W`            | Any character that is NOT a letter, numeric digit, or the underscore character.                       |
|           `\s`            | Any space, tab, or newline character. (Think of this as matching “space” characters.)                 |
|           `\S`            | Any character that is NOT a space, tab, or newline.                                                   |

## Special Sequences

|   item   | Description                                               |
| :------: | --------------------------------------------------------- |
|   `\A`   | start of string                                           |
|   `\b`   | matches empty string at word boundary (between \w and \W) |
|   `\B`   | matches empty string NOT at word boundary                 |
|   `\d`   | digit                                                     |
|   `\D`   | non-digit                                                 |
|   `\s`   | whitespace: `[ \t\n\r\f\v]`                               |
|   `\S`   | non-whitespace                                            |
|   `\w`   | alphanumeric: [0-9a-zA-Z_]                                |
|   `\W`   | non-alphanumeric                                          |
|   `\Z`   | end of string                                             |
| `\g<id>` | matches a previously defined group                        |
