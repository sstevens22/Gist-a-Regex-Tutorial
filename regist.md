## Title
Matching a Hex Value
## Intro
When writing a regex to match a Hex value, first and foremost, it is important to understand what a Hex value is. The hex system, or hexadecimal, is a number system of base 16. Because the decimal system only has 10 digits, the extra 6 digits are represented by the first 6 letters in the alphabet. For example, a hex value of B would be represented as 11 in decimal form, or binary value of 1011. Hexadecimal is an easy way to express binary numbers in modern computers in which a byte is usually defined as containing eight binary digits. 

By far the most common use for Hex values is when it comes to adding color to a web page. RGB, which stands for red, green, and blue is the color model that monitors use. Since in web design we are primarily concerned with what web pages look like on screens, RGB is the color model we use. RGB colors have three values that represent red, green, and blue. Each value can be a number between 0 and 255 or a percentage from 0 to 100%. A value of 0 means none of that color is being used and a value of 255 or 100% means all of that color is being used. A 0 for all three color values will be black and a 255 or 100% for all three color values will be white. Some examples of this are rgb(0, 0, 0) for black, rgb(255, 255, 255) for white or lets say rgb(128, 80, 200) for purple. Percentages would also work in the same way, such as rgb(100%, 100%, 100%) for white or rgb(50%, 31%, 78%) for purple. 

However, using Hex values to define colors makes it infinitely easier. Hex can be used to represent colors on web pages and image-editing programs using the format #RRGGBB (RR = reds, GG = greens, BB = blues). The # symbol indicates that the number has been written in hex format. Instead of using three numbers between 0 and 255, you use six hexadecimal numbers. Hex numbers can be 0-9 and A-F. Hex values are always prefixed with a # or a $ symbol. An example of using hex values to define RBG colors would be something like color: #000000 for black, color: #ffffff for white, or color: #8050c8 for purple. A good thing to note is the hex can also be shortened in some cases to #RGB. If both digits of the red, green and blue values are the same, you may use the short three-digit notation. A good example of this would be #000 for black instead of #000000, #fff for white instead of #ffffff, or #f00 for red rather than #ff0000.


## Summary

Since Hexadecimal is a base 16 numbering system which is made up of 16 digits 0 – 9 and six more, which is A through F, our regex expressions would look something like:
/[a-fA-F0-9]/
/\b[a-fA-F0-9]+\b/
/[#\$?[a-fA-F0-9]/
/[#\$]?([a-f0-9]{6}|[a-f0-9]{3})/  or  /^#([a-fA-F0-9]{6}|[a-fA-F0-9]{3})$/ and possibly /[#\$]?([a-f\d]{6}|[a-f\d]{3})/---- For color code specifically.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Boundaries](#boundaries)

## Regex Components
### Anchors
^                 # start of the line
$                 # end of the line

### Quantifiers
?                     # 0 or 1 possible use of what comes before it
+                      # one or more


### OR Operator
|               # or

### Character Classes
^                 # start of the line
  (                 # start of (group 1)
  )                 # end of (group 1)
  $                 # end of the line
\$                  # meaning changes to literal usage of the symbol $
\d                   # any digit 0-9

### Bracket Expressions
[a-fA-F0-9]{6}  # support a-f, A-F and 0-9, with a length of 6
[a-fA-F0-9]{3}  # support a-f, A-F and 0-9, with a length of 3
[#\$]?            # possibly starts with # or $

### Boundaries
\b                    # word boundary      
 
## Author

My name is Sheldon Stevens. I am a coding student and a link to my github profile is https://github.com/sstevens22
