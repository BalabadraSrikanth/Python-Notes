# String

---

### Definition:
-A **string** is a sequence of characters that is declared or assigned between double quotes.  
It can include letters, integers, and symbols.  

-Python does not have a character data type, so a single character is also considered a string.  
A string is a data type in Python and is **immutable** (it cannot be changed).

**Example:**
```python
String = "Python String"
```


## MultiLine String 
---
If we need to span String multiple line we can use triple quates(""" """).

**Example:**
```python
Mlstr= """MUltiple Line
      String """
print(Mlstr)
```


##  Accessing charecter in python string
---
We can access a charecter using indexing start from 0 to -1


**Example:**
```python
String = "PthonCharecters"
print(String[0])  # First charector
print(String[-1])  # Last Charector
```

## String Slicing

---

**Slicing** is a way of extracting a portion of characters from a string by providing a **start** and **stop** index, separated by a colon (`:`).

The syntax for slicing is:

```python
string[start:stop]
```
**Example:**
```python
String = "Pyhton Slicing"
print(String[:])  # print starting to ending

print(String[0:5])  #print 0th index to 4th index

print(String[6:10]) #print 6th index to 9th index

print(String[-4:])  # print 4th index from last to last index

print(String[:-1])  # print from start to last

print(String[3:])    # print from 3th index to last

#Reversing a string
print(String[::-1])    
```
**Output**
``` 
Pyhton Slicing
Pyhto
 Sli
cing
Pyhton Slicin
ton Slicing
gnicilS nothyP
```

## Manipulating/Updating  the String
---
Strings in Python are **immutable**, meaning you cannot directly change individual characters.  
However, you can achieve the desired changes by **re-assigning** a new string using **slicing** and **concatenation**.

### Re-assignment

**Re-assignment** means assigning a new string to the same variable after modifying it.
**slicing** means extrating the portion that we need
**concatenation** means adding 2 or more strings

### Syntax:

```python
old_variable = modified_string
```

**Example**
```python 

String = "pythonString"
String = "P"+String[1:]
print(String)      #Output     'PythonString'
```

## Deleting a String
In string we cant delete individual charecters because of immutable so we have to deleete entire strign

``` del String```

---

## Python String Methods
Pyhton is a collection of in-built functions that operates on strings
(Even string methods in python does not change the original string insted returns new steing with ehe changed attributes)

### List of String Methods in python

| Function Name  | Description |
|----------------|-------------|
| `capitalize()`   | Converts the first character of the string to uppercase |
| `casefold()`     | Implements caseless string matching |
| `center()`       | Pads the string with the specified character |
| `count()`        | Returns the number of occurrences of a substring |
| `encode()`       | Encodes the string using the specified encoding scheme |
| `endswith()`     | Returns `True` if the string ends with the given suffix |
| `expandtabs()`   | Replaces `\t` with spaces |
| `find()`         | Returns the lowest index of the substring if found |
| `format()`       | Formats the string for output |
| `format_map()`   | Formats using dictionary values |
| `index()`        | Returns the index of the first occurrence of a substring |
| `isalnum()`      | Returns `True` if all characters are alphanumeric |
| `isalpha()`      | Returns `True` if all characters are alphabetic |
| `isdecimal()`    | Returns `True` if all characters are decimal digits |
| `isdigit()`      | Returns `True` if all characters are digits |
| `isidentifier()` | Returns `True` if string is a valid identifier |
| `islower()`      | Returns `True` if all characters are lowercase |
| `isnumeric()`    | Returns `True` if all characters are numeric |
| `isprintable()`  | Returns `True` if all characters are printable or string is empty |
| `isspace()`      | Returns `True` if all characters are whitespace |
| `istitle()`      | Returns `True` if the string is in title case |
| `isupper()`      | Returns `True` if all characters are uppercase |
| `join()`         | Concatenates elements of an iterable with the string as separator |
| `ljust()`        | Left-aligns the string using a specified width |
| `lower()`        | Converts all uppercase characters to lowercase |
| `lstrip()`       | Removes leading characters |
| `maketrans()`    | Returns a translation table |
| `partition()`    | Splits the string at the first occurrence of the separator |
| `replace()`      | Replaces all occurrences of a substring with another |
| `rfind()`        | Returns the highest index of the substring |
| `rindex()`       | Returns the last occurrence index of the substring |
| `rjust()`        | Right-aligns the string using a specified width |
| `rpartition()`   | Splits the string into three parts from the right |
| `rsplit()`       | Splits the string from the right using the separator |
| `rstrip()`       | Removes trailing characters |
| `splitlines()`   | Splits the string at line breaks |
| `startswith()`   | Returns `True` if the string starts with the given prefix |
| `strip()`        | Removes leading and trailing characters |
| `swapcase()`     | Swaps uppercase to lowercase and vice versa |
| `title()`        | Converts the string to title case |
| `translate()`    | Translates characters based on a translation table |
| `upper()`        | Converts all lowercase characters to uppercase |
| `zfill()`        | Pads the string with zeros on the left to fill the width |

---

### capitalize()

This method is used to convert the **first character** of the string to **uppercase**, and the **rest of the characters** to **lowercase**.

**Syntax**

      variable.capitalize()

**Example**
```python
String = "pythoncapitalize"
String.capitalize()      # output      'Pythoncapitalize'
```
---


### casefold()
Python String casefold() method is used to convert string to lowercase. It is similar to the Python lower() string method, but the case removes all the case distinctions present in a string.

**Case distinctions** 
refer to the difference between uppercase and lowercase letters.
casefold() is more aggressive — it removes all case distinctions, including special characters that lower() may not handle.

**Syntax:**
```
variable.capitalize()
```


**Example**
```python

text1 = "Straße"       # German word for "street"
text2 = "strasse"

print(text1.lower())      # Output: "straße"
print(text1.casefold())   # Output: "strasse"
print(text1.casefold() == text2)   # Output: True
```
---

### count()

returns the count of given input in the given range [Start, Stop], as default it checks entire string

**Syntax**

    Variable.count(value,start,end)

**Example**
```python
asdf='spam, spam, spam'
print(asdf)
print(asdf.count('spam',0,20))
```
---

### endswith()
Returns **TRUE** when the given string is ended with the given siffix, other wise returns false

**Syntax**

     Variable.endswith(suffix,start,end)
**Exmaple**
```python
VAriable="python"
print(VAriable.endswith('on',3,7))    # TRUE
```
---


### expandtabs(tabsize=8)
REturn the String with the tab space we required by defining the size. By default it prints as a 8 space


**Syntax**

     Variable.expandtabs(tabspace)
**Exmaple**
```python
VAriable="pyt\thon"
print(VAriable.tabspace(12))    # pyt            hon
```


---
### find(sub[, start[, end]])
Return the lowest index in the string where substring sub is found within the slice s[start:end]. Optional arguments start and end are interpreted as in slice notation. Return -1 if sub is not found.

**Syntax**

     VAriable.find(string)
**Exmaple**
```python
VAriable="python"
print(VAriable.find('t'))          # 2
print(VAriable.find('o',3,7))      # 4
```
---

### join()

join use to join the special charecters(, - + . ) ect in in middle of the string for each word

**Syntax**

     " ,".join(VAriable)
**Exmaple**
```python
words = ['Python', 'is', 'a', 'powerful', 'language']
sentence = " <--> ".join(words)
print(sentence)                   #Python <--> is <--> a <--> powerful <--> language
```
---


### lower()

Converting all the charcters in the string to lower case

**Syntax**

     VAriable.lower()
**Exmaple**
```python
VAriable="PYthoN"
print(VAriable.lower())           # pyhton
```
---



### strip() 

The strip()method is used to remove the spaces of a string from both sides and the charecters given in paranthesis

**Syntax**

     VAriable.strip(chars)
**Exmaple**
```python
words =" 'Python' 'Is' 'A' 'Powerful' 'Language' "
print(words.strip("'"))                        # ''Python' 'Is' 'A' 'Powerful' 'Language''
```
---

### lstrip()

Trim the empty space which is on left side of a string

**Syntax**

     VAriable.lstrip()
**Exmaple**
```python
VAriable=" PYthoN "
print(VAriable.lstrip())      # 'PYthoN '

```
---


### rstrip()

Trim the empty space which is on right side of a string

**Syntax**

     VAriable.rstrip()
**Exmaple**
```python
VAriable=" PYthoN "
print(VAriable.rstrip())      # ' PYthoN'

```
---





### removesuffix()     

If the String ending with suffix string removes the suffix string otherwise prints original string
(if the string was ending with the string which you want to remove then the **removesuffix** will perform removing the string else it not perform any thing)

**Syntax**

     VAriable="TextBook"
**Exmaple**
```python
asdf='TestHooks'
#asdf=asdf.removesuffix('Hooks')
print(asdf)                        # Test

```
---




### removepriffix()    

If the String start with prefix string removes the prefix string otherwise prints original string
(if the string strarting with the string you want to remove then it perform operation else it print original string
**Syntax**

     VAriable="TextBook"
**Exmaple**
```python
asdf='TestHooks'
asdf=asdf.removepriffix('Text')
print(asdf)                        # Hooks

```
---


### replace() 

It used to replace occurrences of a specified substring with another substring within a string.

**Syntax**

     VAriable.replace(oldstring,newString)
**Exmaple**
```python
aa='hard work'
aa=aa.replace(" ","")
print(aa)            #hardwork
```
---



### replace() 

It used to replace occurrences of a specified substring with another substring within a string.

**Syntax**

     VAriable.replace(oldstring,newString)
**Exmaple**
```python
aa='hard work'
aa=aa.replace(" ","")
print(aa)            #hardwork
```
---

### title() 
The title() method returns a string where the first character in every word is upper case. Like a header, or a title.

**Syntax**

     VAriable.titile()
**Exmaple**
```python
words ="'Python' 'is' 'a' 'powerful' 'language'"
print(words.title())                  # 'Python' 'Is' 'A' 'Powerful' 'Language'
```
---




### swapcase() 

The Swapcase() mrhtod use to swap the uppercase caherecters to lowercase and lowercase charecters to uuppercase

**Syntax**

     VAriable.swapcase()
**Exmaple**
```python
words ="'Python' 'Is' 'A' 'Powerful' 'Language'"
print(words.swapcase())                     #'pYTHON' 'iS' 'a' 'pOWERFUL' 'lANGUAGE'
```
---



### startswith() 

the startswith() method returns True if the string starts with the specified value, otherwise False.

**Syntax**

     VAriable.startswith(string, start, end)
**Exmaple**
```python
words ="'Python' 'Is' 'A' 'Powerful' 'Language'"
print(words.startswith("P", 10, 20))                     #True
```
---



### endsswith() 

the endswith() method returns True if the string ending with the specified value, otherwise False.

**Syntax**

     VAriable.endswith(string)
**Exmaple**
```python
words ="'Python' 'Is' 'A' 'Powerful' 'Language'"
print(words.endswith("e"))                     #True
```
---
---

## Formating String

String formatting allows you to create dynamic strings by combining variables and values

There are five different ways to perform string formatting in Python

⏩Formatting with % Operator.                                                      
⏩Formatting with format() string method.                                          
⏩Formatting with string literals, called f-strings.                                          
⏩Formatting with String Template Class                                                
⏩Formatting with center() string method.                                                


###⏩Formatting with % Operator                                      
It is the oldest method of string formatting. Here we use the modulo % operator. The modulo % is also known as the “string-formatting operator”.

**Exmaple1**

    print("The mangy, scrawny stray dog %s gobbled down" %'hurriedly' + 
          "the grain-free, organic dog food.")      
**OutPut**

      The mangy, scrawny stray dog hurriedly gobbled downthe grain-free, organic dog food.
      
**Exmaple2**

    variable = 12 
    string = "Variable as integer = %d \n\
    Variable as float = %f" %(variable, variable)
    print (string)
**OutPut**

    Variable as integer = 12
    Variable as float = 12.000"

###⏩Formatting with format() string method.

Formatters work by putting in one or more replacement fields and placeholders defined by a pair of curly braces { } into a string and calling the str.format(). The value we wish to put into the placeholders and concatenate with the string passed as parameters into the format function. 
**Example**

    print('We all are {}.'.format('equal'))    
**OutPut**
    
    # WE are equal

###⏩Formatting with string literals, called f-strings.                                          

 the f-string f"My name is {name}." is used to interpolate the value of the name variable into the string.

**Example**

    name = 'Ele'
    print(f"My name is {name}.")
**Output**
    
    My name is Ele

**Example**

    print(f"He said his age is {(lambda x: x*2)(3)}")
**OutPut**

    He said his age is 6

###⏩Formatting with String Template Class                                                

This code imports the Template class from the string module. The Template class allows us to create a template string with placeholders that can be substituted with actual values. Here we are substituting the values n1 and n2 in place of n3 and n4 in the string n.

**Example**

    from string import Template

    n1 = 'Hello'
    n2 = 'GeeksforGeeks'
    n = Template('$n3 ! This is $n4.')
    print(n.substitute(n3=n1, n4=n2))

**OutPut**

    Hello ! This is GreeksforGreeks

###⏩Formatting with center() string method.                                                

The center() method is a built-in method in Python's str class that returns a new string that is centered within a string of a specified width. 

**Example**

    string = "GeeksForGeeks!"
    width = 30
    centered_string = string.center(width,"_")
    print(centered_string)

**OutPut**

    ________GeeksForGeeks!________

    
