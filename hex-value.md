# Hex values

in this document we will be going over a specifix regular expression of matching hex values. below you will see all the specific components of how to do this



## Summary

here is an example of the regular expression we will be examining:
```
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```
below we will pull this code apart and explain each section.



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

### Anchors
what are anchors?
There are 2 kinds of anchors: ` ^ ` and ` $ `.
the first `^` is used to anchor the start of a string for instance if we lok at this line:
```
The water is blue
```
Then the starting anchor would be ` ^The `.

NOTE: these are all case sensative 

Now if we were to look at our other anchor ` $ ` this indicates the end of the string.

using the same example as above the end expression would be ` blue$ `

now if we use this on our beginning example then we can se our code starts with ` ^# ` and ends with ` {3}$ `



### Quantifiers
there are a few different types of qunatifiers such as:

` # ` - matches a # (this is optional it can be read either with or without the #)

` * ` - matching the pattern zeor or more times

` + ` - matches the pattern one or more times

` ? ` - matches the pattern zero or one time 

` {} ` - curly brackets can specify three different ways to set limits for a match:

 * ` { N } ` - matches the pattern exactly ` n ` number of times

 * ` { n, } ` - matches the pattern at least ` n ` number of times 

 * ` { n, x } ` - matches the pattern from the minimum `n` to the maximum `x` number of times

 now if we use this and look at our example again then we can see we start with ` ^#? `

 now we know the ` ? ` matches a 0 or 1.

 we also have two instances of ` { n } ` within our expression ` [a-f0-9]{6} ` and ` [a-f0-9]{3} `

 these mean we are looking for a string or 6 and 3 characters 



### Grouping Constructs
the grouping of an expression is expressed as anything between ` () ` the grouping of multiple characters between these parenthesis as a single unit. this will be displayed in the form of an arrayand each value can be accessed unsing an index on the result of the match

for example if we have ` (ball){4}` then our result would be ballballballball



### Bracket Expressions
bracket expressions are ` [] ` this is used to match a specific regax pattern of characters defined within the brackets and seperated with a hyphento to set the range of characters for instance we can have
* ` [a-z] ` this looks for a sting from a to z 
* ` [0-9] ` this looks for any number from 0 to 9
* ` [a-z0-9] ` we can also have a mix so with this example it will get any letter or number.

in our example we have ` [a-f0-9]{6} ` and ` [a-f0-9]{3} ` and we now know that this is looking for any charracter repeated 6 times and any character repeated 3 times 



### Character Classes
character classes only match wat is defined with a hyphen used to set the limits for example ` a-g ` will only accept a character between a and g or we can use this with numbers as well so if we have ` 0-5 ` if will only accept numbers between 0 and 5. 

for example if we have ` [g-m4-9]{4} `

then we will be looking for a sting or 4 characters with letters between g and m as well as numbers between 4 and 9which could look something like this ` i6k8 ` but thses are able to be in any order.



### The OR Operator
the or operator is indicated by ` | ` in our example we have ` ([a-f0-9]{6}|[a-f0-9]{3}) ` we now know that this is looking for a string or 6 letters between a and f or numbers between 0 and 9, or a string of 3 letters between a and f or numbers between 0 and 9



## Author

my name is Andrew. my goal is to transition from a trade to a tech career which means ill need to be able to explain code concepts as well as use them which has made this a great project.
you can see all ive learnt and any future projects as my github:  https://github.com/AndrewDippel
