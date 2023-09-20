# Regex code to match HTML tag.

This tutorial is intended for utilizing Regular Expressions (Regex) to match HTML tags. Employing Regex in this manner constitutes a precise pattern search. The subsequent tutorial will illustrate the practical application of an HTML Tag Regex search.

## Summary

In this tutorial, we will dissect and elucidate each component of the following Regular Expression pattern: /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/. Our aim is to enhance the comprehension of the readers of this document regarding the application of this technology in extracting information from diverse formats.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Author](#author)
- [Reference Links](#reference-links)

## Regex Components

### Anchors
This code employs two distinct anchors: the ^ caret anchor and the $ dollar anchor. In this instance, the caret anchor is employed at the code's outset, signifying that the expression must commence matching at the start of the string. Additionally, you have the flexibility to append specific text for matching as necessary. Conversely, the dollar anchor, being utilized at the expression's conclusion, mandates that the pattern match the string's conclusion. Similar to the caret anchor, you can also append specific text for matching purposes. The interpretation of these anchors hinges on their respective positions.

### Quantifiers
([a-z]+): In this instance, when employing the plus sign quantifier, it signifies that the pattern will match one or more occurrences of lowercase letters ranging from 'a' to 'z'. These letters are not restricted to just one occurrence; they can repeat multiple times.

([^<]+)*: When utilizing the asterisk sign quantifier in this example, it indicates that the pattern will match one or more instances of characters, excluding the less than symbol.

(\s+\/>): In this code snippet, the placement of the plus sign quantifier indicates that it will match one or more white spaces preceding the self-closing tag. While the ? quantifier is not used in this code snippet, if it were added, it would make the expression optional. The ? as a quantifier implies that it will match zero or one occurrence, rendering it optional.

### Grouping Constructs
When grouping constructs are utilized, their purpose is to group distinct segments of an expression together, and this is signified by enclosing the relevant code within parentheses. We have identified some examples from our code that illustrate these grouping constructs:

([a-z]+) and ([^<]+)*: These are the two examples we previously discussed, and they are categorized as grouping constructs. They serve the purpose of grouping and capturing lowercase letters and characters, excluding the less than symbol, respectively.

(?:>(.*)<\/\1>|\s+\/>): In this particular construct, denoted by the ?: at the outset, it represents a non-capturing grouping construct. Within it, there are two alternatives separated by the | symbol. This construct is employed for matching either a complete HTML tag with content or a self-closing tag.

### Bracket Expressions
[a-z] This one capture the tag name, [^<] and this one capture the attribute inside the tag.

### Character Classes
The square brackets in our code serve to define character classes, as we've mentioned previously. Here are two examples:

[a-z]: This represents a character class that specifies lowercase letters ranging from 'a' to 'z'.

[^<]: This code defines a negated character class, which matches any single character that is not a less-than symbol '<'.

### The OR Operator
Please reference the Grouping Constructs section.

## Author
My name is Bryan and I am a student at the University of Pennsylvania Full Stack web developer program.
Here you can see my profile: https://github.com/bzinsky

## Reference links

Code definition:
https://regex101.com/ 

Anchors:
https://www.javascripttutorial.net/regular-expression-anchors/ 

Quantifiers:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_expressions/Quantifiers 

Grouping Constructs:
https://learn.microsoft.com/en-us/dotnet/standard/base-types/grouping-constructs-in-regular-expressions

Character Classes:
https://docs.oracle.com/javase/tutorial/essential/regex/char_classes.html

Bracket Expressions:
https://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap09.html#:~:text=A%20bracket%20expression%20is%20either,character%20classes%2C%20or%20range%20expressions.