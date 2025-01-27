---
title: regexp
category: Others
layout: 2017/sheet
weight: -1
authors:
  - github: rizqyhi
updated: 2019-03-24
description: |
  Basic cheatsheets for regular expression
---

##

{: .-three-column}

### Character classes

| Pattern | Description                    |
| ------- | ------------------------------ |
| `.`     | Any character, except newline  |
| `\w`    | Word                           |
| `\d`    | Digit                          |
| `\s`    | Whitespace                     |
| `\W`    | Not word                       |
| `\D`    | Not digit                      |
| `\S`    | Not whitespace                 |
| `[abc]` | Any of a, b, or c              |
| `[a-e]` | Characters between `a` and `e` |
| `[1-9]` | Digit between `1` and `9`      |

### Anchors

| Pattern | Description      |
| ------- | ---------------- |
| `^abc`  | Start with `abc` |
| `abc$`  | End with `abc`   |

### Escaped characters

| Pattern    | Description                            |
| ---------- | -------------------------------------- |
| `\. \* \\` | Escape special character used by regex |
| `\t`       | Tab                                    |
| `\n`       | Newline                                |
| `\r`       | Carriage return                        |

### Groups

| Pattern | Description   |
| ------- | ------------- |
| `(abc)` | Capture group |

### Quantifiers

| Pattern  | Description           |
| -------- | --------------------- |
| `a*`     | Match 0 or more       |
| `a+`     | Match 1 or more       |
| `a?`     | Match 0 or 1          |
| `a{5}`   | Match exactly 5       |
| `a{,3}`  | Match up to 3         |
| `a{3,}`  | Match 3 or more       |
| `a{1,3}` | Match between 1 and 3 |

### Multiple Possibilities
| Pattern | Description                                                    |
| ------- | -------------------------------------------------------------- |
| `\|`    | To search for multiple patterns for example `/yes\|no\|maybe/` |

### Lazy Matching
| Pattern | Description                                                            |
| ------- | ---------------------------------------------------------------------- |
| `?`     | Finds the smallest part of the string that satisfies the regex pattern |

### +ve and -ve Lookahead
| Pattern | Description                                                                                                                   |
| ------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `?=`    | Positive Lookahead `(?=...)` : will look to make sure the element in the search pattern is there, but won't actually match it |
| `?!`    | Negative Lookahead `(?!...)` : will look to make sure the element in the search pattern is not there                          |

### RegExp Related Functions
| Function     | Description                                                                                                                         |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| `.test()`    | Testing : <br /> `/Hello/.test('Hello World!') // returns true` while <br /> `/Greetings/.test('Hello World!') // returns false`    |
| `.match()`   | Matching : <br /> `'Hello World!'.match(/World/) // returns 'World'` while <br /> `'Hello World!'.match(/Greetings/) // returns []` |
| `.replace()` | Repalacing : <br /> `'The Sky is White'.replace(/White/, "Blue")` <br /> `// returns 'The Sky is Blue'`                             |

### RegExp Flags
| Flags | Description                                                                                            |
| ----- | ------------------------------------------------------------------------------------------------------ |
| `i`   | Ignore Case : <br /> `let regexp = /igNoreCase/i;` <br /> `regexp.test('IgNoReCaSe') // returns true`  |
| `g`   | Match Multiple : <br /> `let regexp = /l/g;` <br /> `'Hello World!'.match(regexp) // returns [l,l,l]'` |
| `m`   | Multi Line Mode : <br /> adds the newline character `\n` to the regexp result when found               |
