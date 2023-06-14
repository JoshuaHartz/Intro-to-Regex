# Intro-to-Regex

Regex, short for regular expression is a specified set of text to help you locate patterns in text. This can be very useful in many applications, specifically in applications where the data is very large and you only want certian occurances but it would be impossible to find all. Regex can be very simple or very complicated. Giving it use in a wide range of applications. Its best to understand the basics and how you can utilize them to your advantage in CTF competitions. 

I cant remember all the regex things on my own so i like to use online [cheat sheets](https://cheatography.com/davechild/cheat-sheets/regular-expressions/) and I love to use chatgpt to generate regex strings for me. There are also websites that you can test your regex on and it will tell you what you are creating in real time, I like to use [regex101](https://regex101.com)


### Example

An example of how regex can be used is this.

A NCL SKY flag has 3 secionts seperated by dashes it looks like this. SKY-TEST-6969. SKY and then 4 uppercase letters and then 4 numbers.

Regex for the whole SKY flag would be this "SKY-[A-Z]{4}-\d{4}" [A-Z]{4} means we are looking for four uppercase letters from A to Z, \d{4} means we are looking for four digits 0-9.
Since SKY flags are always different we cannot assume that it will be TEST-6969 every time so with the beauty of regex we can have a generic pattern to look for every occurance in a file or text. 

![image](https://github.com/JoshuaHartz/Intro-to-Regex/assets/102620766/4fb37ef4-2df1-4a49-a688-bd427611d826)

Yes this could be solved by using the CTRL+F funcitonality that most if not all browsers support, but where Ctrl+F stops regex starts. Linux commands like grep, awk, sed, and probably many other commands take regex. But if you arent a linux user dont worry, many programming languages can understand regex, most notably python. Ive used python on many occasions in log analysis to scrape together certain parts of a log that could only be done with regex. 


## Regex Aspects 

1. Literals: Literal characters match themselves. For example, the regex a will match the letter "a" in a string.
2. Character Classes: Character classes allow you to specify a set of characters to match. For example, [abc] matches any single occurrence of "a", "b", or "c". You can also use ranges like [a-z] to match any lowercase letter.
3. Quantifiers: Quantifiers define how many times a character or group can repeat. Common quantifiers include:
    
    '*' : Matches zero or more occurrences of the preceding element.


    '+' : Matches one or more occurrences of the preceding element.


    '?' : Matches zero or one occurrence of the preceding element.
    
    
    {n} : Matches exactly n occurrences of the preceding element.
    
    
    {n,} : Matches at least n occurrences of the preceding element.
    
    
    {n,m} : Matches between n and m occurrences of the preceding element.

<br>

4. Anchors: Anchors allow you to specify positions in the string:

    ^: Matches the start of the string.
  
    $: Matches the end of the string.
  
    \b: Matches a word boundary.


5. Grouping and Capturing: Parentheses () are used for grouping and capturing parts of a pattern. They also influence the precedence of operators and allow you to apply quantifiers to multiple characters.
6. Alternation: The pipe character | represents alternation, allowing you to match one pattern or another. For example, cat|dog matches either "cat" or "dog".
7. Escaping: Certain characters have special meanings in regex. To match these characters literally, you need to escape them with a backslash '\.' For example, to match a literal dot, use '\.'.
8. Modifiers: Modifiers change the behavior of a regular expression. Common modifiers include case-insensitive matching (i), global matching (g), and multiline matching (m).

## Must know regex 
