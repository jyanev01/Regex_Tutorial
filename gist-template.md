# Regex Tutorial

Hello, this is tutorial on Regex concepts and syntax. I hope that you find this useful and helpful in the furtherment of your career within the field of computer science. Enjoy:)

## Summary

Regex; which is short hand for rational expression is a sequence of characters that specifies a search pattern. It is commonly used to validate string- search algorithms to find, find and replace or for input validations. Ex field that require email address on web page. We will use the following code as an example in this tutorial:

<!-- SNIPPET OF REGEX CODE HERE -->

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
    ^ - The caret anchor matches the BEGINNING of the text

    $ - The dollar anchor matches the END of the text

    Example:
    /^J/--- Match any text that starts with the letter J.

### Quantifiers
    Exact count {n}- When you append it to a character or character class, it specifies how many characters you want to match.
        
        Example: /\d{4}/ matches a four-digit number. It is the same as writting /\d\d\d\d/.

    The range {n,m}- matches a character or character class from n to m times.
        Example: To find numbers that have two, three or four digits, you use the regular expression /\d{2,5}/g

    `*`- Matches zero or more times

    `+`- Matches one or more time
    `?`- Matches a stin
    `()*`

### OR Operator
    (|) - Matches one of multiple patterns- such as this OR that- use the OR operator
        Example: hi|hello will return either 'hi' or 'hello'.

    []- Matches a pattern based on the position of a character.
        Example: [a-d] a string that contains a lowercase a,b,c, OR d. equivalent to a|b|c|d or [abcd]

    

### Character Classes
    \d- Matches the first digit or character from 0 to 9.
        Example: let phone = +359 (678-8893)
                let re = /\d/

                Returns: ["3"] 
        

    \s- Matches a whitespace symbol such a space, a tab (\t), a newline (\n), etc
        Example: let str = 'ES6 Tutorial'

            let re- /ES\d/g

            Returns: ['ES6']

    \w- Stands for word character. It matches the ASCII character [A-Za-z0-9_] including Latin alphabets, digits, and the underscore
        Example: [a-z] would match any of 26 letters in alphabet, lowercase

    `.`- Matches any character
    



### Flags

    Flas are optional parameters that can be added to a plain expression to make it search in a different way.

    Types of Flags:

    i - Ignore Casting- Makers the expression search case- insensitively
        Example: /Hello/i matches the characters 'hello' despite possible spellings (Hello, hEllo, heLlo, helLo, hellO, HELLO ALL MATCH)

    g - Global- Makes the expression search for all occurences

        Example: let string =[Hello, World, hellO, worLD ]

        /hello/g--> returns "Hello" only first item in string "Hello"

    s - Dot All- makes the wild character . match newlines as well.
        Example: var str = "Content flow\ndownward and\ndownward"
        
        /.+/gs

        Returns: "Content flows\ndownward and n/downward"


    m - Multiline - Makes the boundary characters ^ and $ match the beginning and ending of every single line instead of the beginning and ending of the whole string.
        Example: 

        /^A.+/mg

        Returns: The ^ character matches the start of everylin, thanks to the m flag. Altogether the expression looks for an 'A' at the beginning of every line and if one is found, it matches the whole line, till the end.

    y - Sticky - Makes the expressio start its searching from the index indicated in its lastIndex property.
        Example: var str = "Cats love cats, and we love cats."

        var exp= /cats/igy
        exp.lastIndex =4

        Returns: "cats, and we love cats"- onle the word "cats" after the 4th character in the array, it skips the first workd Cats.

    u - Unicode - Makes the expression assume individual characters as code points, not code units, and thus match 32- but characters as well.
        Example: /\u/

        Returns: treat all special characters such as "check marks" or "characters outside of UTF-16



### Grouping and Capturing

    ()- Matches the items within the parenthesis and remembers them for future expressions.
        Example: /(foo)/

        matches and remembers "foo" in "foo bar".


    (?:)- Matches the item BUT does not remember the character.
        Example: /(?:foo)/

        matches BUT DOES NOT remember "foo" in "foo bar".

    (?<>)- Matches item and stores it within grpups property specified under the name within <>.
        Example: (?<name>\d)

        returns: matches.groups.name - d

### Bracket Expressions
    Bracket expressions are enclosed by a '[]' matches any single character within the brackets.

        Examples:
        `[]`- matches any single character within the bracket

        '[]%' - matches the string inside the brackets before the %

        '[^]' - matches any string that has does not have a letter from within the brackets.

### Greedy and Lazy Match
    This type of Regex tries to find a match for every position in the string and try to match the pattern at that position. If there's no match, go to the next position.
        Example: <?^+.> matches any of the characters within the '<>'

### Boundaries
    Unlike anchors which are stand alone symbols, a boundary (\b) matches a position where one side os a word character and the other side is not a word character.
        Example: `\bcat\b` would therefore match "car" in "a black cat", but it wou;dn't match it in "catatonic, tomcat or certificate."

        Example: \bcat would match "cat" in "catfish"

        Example: cat\b would match "cat" in "tomcat"

    \B - Matches all position where \b doesn't match.


### Back-references
    Back- references match the same text as previously matche by a capturing group. By putting the opening tag into a backreference, one can re use the name of the tag for the closing tag.
        Example: <([A-Z][A-Z0-9]*)\b[^>]*>.*?</\1>

        Captures: [A-Z][A-Z0-9]*-----> All of the items in the first set of parenthesis.

### Look-ahead and Look-behind
    (?=X) Lookahead- Asserts that what immediately follows the current position in the string X

    (?<=X) Lookbehind- Assets that what immediately precedes the current position in the string is X

    (?!X)  Negative Lookahead- Asserts that waht immediately follows the current position in the string is not X

    (?<!X) Negative Lookbehind- Asserts that what immediately preceds the current position in the string in not X

## Author

Jordan Yanev is an upcoming developer with a passion for detail and 8 years of public accounting experience. He is in his last month of the Coding Bootcamp at University of Richmond.

[GitHub: https://github.com/jyanev01]
