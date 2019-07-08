# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)

```
var numbaStrings = ""

for additionalString in 1...10 {
    numbaStrings += "\(additionalString) "
}
print(numbaStrings)

```

***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.

```
var fireCrotch = ""
var evenIndex = 5

for evenIndex in 5...51 {
if evenIndex % 2 == 0 {
fireCrotch += "\(evenIndex) "
}
}
print(fireCrotch)
```


***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.

```
var endzInFourResult = ""

for i in 1...60 {
if i % 10 == 4 {
endzInFourResult += "\(i) "
}
}
print(endzInFourResult)
```

***
## Question 4

Print each character in the string `"Hello world!"`

```
var helloWorld = "Hello world!"

for i in helloWorld {
print(i)

}

```

***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"`

```
let myStringSeven = "Hello world!"

print(myStringSeven.last!)
```

***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

```
var someRandoString = "telepathic"

let indexCount = someRandoString.count - 1
if someRandoString.count % 2 == 0 {
print(someRandoString)
} else {
for index in 0...indexCount {
if index % 2 != 0 {
let currentIndex = someRandoString.index(someRandoString.startIndex, offsetBy: index)
print(someRandoString[currentIndex], terminator: " ")
}

}
}
```

***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

```
var totallyAString = ""
var totallyAString: Character = "K"

```

***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.

```
"el niño" == "el ni\u{0249}o"
"café" == "\u{63}\u{61}\u{66}\u{E9}"
"Über" == "\u{DC}\u{62}\u{65}\u{72}"
"Ohio" == "\u{4F}\u{68}\u{69}\u{6F}"
"Hello World" == "\u{48}\u{65}\u{6C}\u{6C}\u{6F}\u{20}\u{57}\u{6F}\u{72}\u{6C}\u{64}""

```

***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`

```
print("\u{48}\u{45}\u{4C}\u{4C}\u{4F}\u{20}\u{57}\u{4F}\u{52}\u{4C}\u{44}\u{21}")
```

***
## Question 10

**Using only Unicode**, print out your name.

```
print("\u{4B}\u{69}\u{6D}\u{62}\u{61}\u{6C}\u{6C}")

```

***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.

```

print("\u{4F60}\u{597D}\u{FF0C}\u{4E16}\u{754C}")

```
***

## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -
```
```
var flower = "\u{2698}"
var verticalSymbol = "\u{007c}"
var horozontalSymbol = "\u{005f} "
let outline = String(repeating: horozontalSymbol, count : 11)

for _ in 1...11 {
print(horozontalSymbol, terminator: " ")
}
print(outline)
print()
for _ in 1...7 {
for _ in 1...5 {
print("\(verticalSymbol) \(flower)", terminator: " ")
}
print(verticalSymbol)
}
print(outline)
```

***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
```
```
var rookWhite = "\u{2656}"
var knightWhite = "\u{2658}"
var bishopWhite = "\u{2657}"
var queenWhite = "\u{2655}"
var kingWhite = "\u{2654}"
var pawnWhite = "\u{2659}"
var rookBlack = "\u{265C}"
var knightBlack = "\u{265E}"
var bishopBlack = "\u{265D}"
var queenBlack = "\u{265B}"
var kingBlack = "\u{265A}"
var pawnBlack = "\u{265F}"

print("\(rookWhite) \(knightWhite) \(bishopWhite) \(queenWhite) \(kingWhite) \(bishopWhite) \(knightWhite) \(rookWhite)")
for i in 1...8 {
print("\(pawnWhite)", terminator: " ")
}
for i in 1...4 {
print("")
}
for i in 1...8 {
print("\(pawnBlack)", terminator: " ")
}
print("")
print("\(rookBlack) \(knightBlack) \(bishopBlack) \(queenBlack) \(kingBlack) \(bishopBlack) \(knightBlack) \(rookBlack)")

```

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"
// Your code here
 ```
 

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

```
var aString = "Replace the letter e with *"
var replacedString = ""

replacedString = aString.replacingOccurrences(of: "e", with: "*")
print (replacedString)
```

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
var reverse = ""

// Your code here
```
```
let stringReversed = String(aString.reversed())
print(stringReversed)

```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"

// Your code here
```
```
let aString = "anutforajaroftuna"
var revString = String(aString.reversed())

if aString == revString {
print (true)
}else {
print(false)
}
```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

```
var aString = "Hello"
var revString = String(aString.reversed())

if aString == revString {
print (true)
}else {
print(false)
}
```

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```
```
var problem = "split this string into words and print them on separate lines"
let revisedSplit = "split\nthis\nstring\ninto\nwords\nand\nprint\nthem\non\nseparate\nlines"
print(revisedSplit)

```

***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

// Your code here
```
```
let someWordz = problem.components(separatedBy: " ")

var longestWord = ""

for word in someWordz {
if word.count > longestWord.count {
longestWord = word
}
}

print(longestWord)
```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"
```
```
var vowelCount = 0
var consonantsCount = 0

for char in input {
if vowels.conwtains(char) {
vowelCount += 1
} else if consonants.contains(char) {
consonantsCount += 1
}
}

var bothCounts = (vowels:vowelCount,consonants:consonantsCount)

print(bothCounts)
```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`

```
var theInput = "How are you doing this Monday?"
var newInput = theInput.split(separator: " ")
print(newInput)
var lastWord = newInput.last
print(lastWord!)

var lastWordCount = lastWord?.count
print(lastWordCount!)
```

***
