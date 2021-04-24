## Regexp Python

Regular expression in python.

> Regular expression are a powerful feature for text processing, they match patterns in a sentence.

### 1. Special characters

> The following are special characters in regular expressions.

```
^       - matches the beginning of the sentence
$       - matches the end of the sentence
.       - matches all characters except new line
\       - escape special characters
A|B     - matches expression A or B
+       - matches at least one character
*       - matches 0 or more characters
?       - optional, matches 1 or 0 characters
{m}     - matches the expression to it's left exactly m times
{m,n}   - matches the expression to the left m to n times but not less
{m, n}? - matches the expression to it's left m times and n ignores
```

### 2. Character classes (Special Sequence)

> The following are special sequences in regular expressions

```
\w      - matches alphanumeric characters which is A-Z,a-z,0-9 and _ .
\d      - matches digits 0-9
\s      - matches white space characters \t, \n, \r.
\S      - matches none white space characters
\b      - matches the boundary at the start or end of the word that is  \w and \W.
\B      - matches where \b does not that is not word boundaries.
\A      - matches the expression to it's right at the absolute start of string wether in single or multiple line.
\Z      - Matches the expression to it's left at the absolute end of a string wether in single or multiple line.

```

### 3. Sets

> The following are sets in regular expression

```
[]      - contains a set of characters to match
[akb]   - matches a, k or b
[a-z]   - matches any character between a and z inclusively
[a\-z]  - matches a, -, or z
[a-]    - matches a or -
[-a]    - matches a
[a-z0-9]- matches characters from a to z and also numbers from 0-9
[(+*)]  - special characters becomes literal and this matches (,+, * and ).
[^ab5]  - adding ^ in the character set bracket at the beginning will exclude all the characters in the character set, so thi will match all characters except a, b or 5
```

### 4. Groups

> The following are groups in regular expression.

```
()      - Matches the expression inside the parenthesis and groups it.
(?)     - ? inside the parenthesis acts like extension notation. Its meaning depends on the character immediately to its right.
(?PAB)  -  Matches the expression AB, and it can be accessed with the group name.
(?aiLmsux) - Here, a, i, L, m, s, u, and x are flags:


a       — Matches ASCII only
i       - Ignore case
L       - Locale dependent
m       - Multi-line
s       - Matches all
u       - Unicode characters
x       - Verbose

(?:A)   - matches the expression represented by A, but unlike (?PAB), it cannot be retrieved afterwards.

(?#...) - A comment. Contents are for us to read, not for matching.

A(?=B)  - Lookahead assertion. This matches the expression A only if it is followed by B

A(?!B)  - Negative lookahead assertion. This matches the expression A only if it is not followed by B.

(?<=B)A - Positive lookbehind assertion. This matches the expression A only if B is immediately to its left. This can only matched fixed length expressions.

(?<!B)A - Negative lookbehind assertion. This matches the expression A only if B is not immediately to its left. This can only matched fixed length expressions.

(?P=name) - Matches the expression matched by an earlier group named 'name'

(...)\1   - The number 1 corresponds to the first group to be matched. If we want to match more instances of the same expression, simply use its number instead of writing out the whole expression again. We can use from 1 up to 99 such groups and their corresponding numbers.
```

### 5. Popular `re` Functions:

> The following are the popular regular expression function in python.

#### 5.1 `re.findall(A, B)`

> Matches all instances of an expression A in a string B and returns them in a list

#### 5.2 `re.search(A, B)`

> Matches the first instance of an expression A in a string B, and returns it as a re match object.

#### 5.3 `re.split(A, B)`

> Split a string B into a list using the delimiter A

#### 5.4 `re.sub(A, B, C)`

> Replace A with B in the string C.

#### 5.5 `re.match(A, B)`

> Returns the first occurrence of A in B

#### 5.7 `re.compile(A, B)`

> Flags should be used first in the expression string.

### Code Examples

The code examples are found in the `re.ipynb` file
