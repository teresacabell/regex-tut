# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

This is the regular expression (RegEx) search pattern used to find HEX values. 

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

A HEX value is preceded by a hash (#) and contains a six digit code. This code defines an exact color and is used to ensure accuracy and regularity of the display from computer to computer. 

## Table of Contents

- [Summary](#summary)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)
- [Author](#author)

## Regex Components

### *Anchors*

Anchors identify positions of characters, rather than specific characters. Anchors include `^` and `$`.

/` ^ `#?([a-f0-9]{6}|[a-f0-9]{3})`$`/

The highlighted characters indicate the anchors in this expression. The `/` fixes the boundaries of the search pattern. 

Applying `^` indicates the beginning of the search pattern. This means that the expression will match any string that fulfills the search parameters indicated after the `^`. 

The use of `$` matches a string that ends with the search parameters found just before it. 

### *Quantifiers*

Quantifiers function as the main building blocks. To find a match in a given string, we need to understand how many instances of characters or other expressions are needed. Quantifiers include `*`, `+`, `?` and `{}`.

/^#`?`([a-f0-9]`{6}`|[a-f0-9]`{3}`)$/

Question marks are used to look for zero or one of the character proceeding in a string for a match. The `?` in this expression indicates that the we are looking for a string that has at zero or one hashes (#) at the beginning. This will ensure that we don't miss any matches because in some documentations, the string may not contain a hash.

The brackets are used to show many times the proceeding characters must be repeated for a match. The `{6}` indicates that we are looking for six matches of the proceeding characters within the string. The `{3}` indicates only 3 matches. 

### *OR Operator*

OR operators indicate that a match must include either the proceeding or preceeding expression in the string to satisfy the search parameters. OR operators include `|` or `[]`.

/^#?([a-f0-9]{6}`|`[a-f0-9]{3})$/

Using our understanding of quantifiers, `|` here shows that we are looking for an expression that has either 6 or 3 of the requested characters [a-f0-9].

### *Character Classes*

Character classes can be used to tell the regex engine to only look for certain characters. The character classes are confined in this expression by square brackets ([]). 

/^#?(`[a-f0-9]`{6}|`[a-f0-9]`{3})$/

In this example we are searching for the same types of character classes `a-f0-9` on either side of the OR operator covered above. These characters `a-f` indicate we are looking for letters a through f. `0-9` represents digits 0 to 9.

### *Grouping and Capturing*

Grouping and capturing includes `()`. This part of the expression captures a part of the string with the values contained within the parenthesis. 

/^#?`([a-f0-9]{6}|[a-f0-9]{3})`$/

Using the knowledge from above sections, in this example, we are telling the engine to capture any combination of either 6 or 3 characters from letters a-f or numbers 0-9.

### *Bracket Expressions*

Bracket expressions use `[]` to tell the engine to look for any character in the square brackets. 

/^#?(`[a-f0-9]`{6}|`[a-f0-9]`{3})$/

In this example we are looking for the characters a-f or 0-9.

### *Greedy and Lazy Match*

/^#`?`([a-f0-9]`{6}`|[a-f0-9]`{3}`)$/

Greedy quantifiers match as many characters as possible. Lazy quantifiers match as few characters as possible. Greedy quantifiers include `?`, `*`, `+`, and `{}`. Lazy quantifiers include `??`, `*?`, `+?`, and `{}?`. 

In this RegEx expression we have only greedy quantifiers. This means that we want our engine to search for as many possible characters in the string. 

## Author

This README.md was created by Teresa Schwirtlich, a full-stack developer student through The University of Texas at Austin Coding Bootcamp. 

Check out my GitHub at: https://github.com/teresacabell
