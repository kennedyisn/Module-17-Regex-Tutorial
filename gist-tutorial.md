# Title (replace with your title)

While Javascript can search for specific alphanumeric characters inside of a string or even a full phrase it does lack in some areas of complexity.  Regex(also known as regular expressions) helps close this gap by encompassing larger more intricate cases when we want to perform the same type of action. regex are a string of alphanumeric and scpecial characters that sets the parameters for a specific search pattern.

## Summary

The code below is an example of a regex that would be used to match a specific URL to one submitted by a user.
`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

In the following sections we will break down that code while making sense of the parameters used in regex.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components
Since a regex is a literal the pattern must be encased in slash characters. In our example code below we can see that it is wrapped with these same characters(/).

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

### Anchors

Anchors are characters that signify either the beginning or end of a string, with the (^) character telling us a string begins with the characters listed after it, while the ($) character does the opposite. In our example code the (^) character tells us that the beginning of our string must begin with "https?:" while ending with "/" to be a suitable link. When using a regex keep in mind it is case sensitive as well.

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

### Quantifiers

Quantifiers are characters that sets limits for the matches to our code. They also try to match as many instances of a pattern as possible. 

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

For instance in our code we have several different types of qualifiers that affect our bracketted information from earlier. The curly brackets following "[a-z\.]"  tells us that it must match the pattern from a minimum of 2 times to a maximum of 6. While the (+) character following "[\da-z\.-]" specifies that it matches the pattern atleast once. the question mark(?) makes a quantifier more relaxed by matching it in as few instances as possible.

### Grouping Constructs

A grouping construct breaks up a regex into parts that we want to set seperate paramters for. Groupings are defined with parentheses (()) and each section is known as a subsection. In our code the  three subsections are "(https?:\/\/)", "([\da-z\.-]+)", "([a-z\.]{2,6})" and "([\/\w \.-]*)"

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`


### Bracket Expressions

The square brackets inside our code represents the type of characters we can have in sections of our code. "[hijk]" for example would look for a string that includes the letters h, i, j, or k. If we wanted to do this but in a shorter way we can use a hyphen, [h-k]. 

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

For example in our example code we can see "[a-z\.]", this specifies that in this section we can use all lowercase letters in the alphabet followed by a period(.). When special characters follow alphanumeric specifications it means that we want to include them as apart of the range of characters that can be included.

### Character Classes

A character class does blank
In this snippet from our code "([\da-z\.-]+)", "\d" matches any numerical digit. This would act the same as a bracket expression with"[0-9]. Another example in our code is "\w", which matches any alphanumeric character including underscore(_) as well.

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

### The OR Operator

Considering that brackets only need 1 match in the paramters outlined, what would we do if we want to apply this same logic outside of a bracket expression? Thats where OR Operators(|) come into play. for example the expression [a-z] could be written as (a|z) inside a set of parentheses. In our code we do not find an example of an OR operator.

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

### Flags

Although a regex must be wrapped in slash characters there are also exceptions to this rule with flags being that. Flags can be found after the last slash in a regex and add adiotional parameters to the string. "g-" specifies that the regex must be tested against any possible match, while "i-" specifies that any case sensitive specifications should be ignored. The "m-" flag is a multi line search which means our regex should be treated as multiple lines.

### Character Escapes

In our code you will see a backslash(\) character quite often, this escapes the rules set by the character that follows it. for instance the backslash before the period in our example code "([a-z\.]{2,6})" specifies that the period should be included as a usable character inside of the brackets along with the entire lowercase alphabet.

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

## Author

Name: Kennedy Hayles
https://github.com/kennedyisn
