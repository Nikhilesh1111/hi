# REFERENCE MANUAL

## Introduction
&emsp;&emsp; This manual describes our language which is named as Lazy language which is derived from C and C++.So the uses of this language are similar to C and C++ .Our language is an imperative language and the main advantage of this language is that it is user friendly so that the person using this can understand the language easily and also debug it easily.This manual will be a guide to our language.

## Lexial Conventions
&emsp;&emsp; A Program consists of one or more translation units stored in files. They are translated in many phases. The fisrt phase do low level lexical transformations, carry out directives introduced by the lines beginning with the # character and perform macro definition and expansion.When evrything is completed the program has been reduced to a sequence of tokens.

### Tokens
&emsp;&emsp; There are six classes of tokens: identifiers,keywords,constants,string literals,operators and other separators.Blanks,horizontal and vertical tabs,newlines and comments as described below are ignored except they separate tokens.Some white space is required to separate otherwise adjacent identifiers,keywords and constants.

### Comments
&emsp;&emsp; The characters  |< introduce a comment and >| end the comment.This can be used if we need a block of lines to be in comments.We cannot nest the comments. If we want only one line to be a constant we can use -> to make that line a comment.Comments do not occur within string literals.

### Identifiers
&emsp;&emsp; An identifier is a sequence of letters and digits. The first character must be a letter and also here we can have _ also.Upper and lower case letters are different.Identifiers may have any length but we must define them so that they tell us their use in the program.

### Keywords
&emsp;&emsp; The following identifiers are reserved for the use as keywords and may not be used otherwise:
|Keywords|Keywords|Keywords|Keywords|
|----|----|----|----|
|auto|real|int|struct| 
|if|else|switch|case| 
|enum|register|typedef|extern| 
|return|union|char|const| 
|continue|repeat|void|default| 
|goto|sizeof|volatile|static| 

### Constants
&emsp;&emsp; There are several kinds of constants.Each has a data type and here are some of them

&emsp;&emsp;&emsp;&emsp; Integer constant

&emsp;&emsp;&emsp;&emsp; Character constant

&emsp;&emsp;&emsp;&emsp; Floating constant

&emsp;&emsp;&emsp;&emsp; Enumeration constant

#### Integer constants
&emsp;&emsp; An integer constant consisting of a sequence of digits is taken to be octal if it begins with 0(digit zero),decimal otherwise.Octal constants do not contain the digits 8 or 9. A sequence of digits preceded by 0x is taken to be a hexadecimal integer.The hexadecimal digits include a or A through f or F with values 10 through 15.

&emsp;&emsp; An integer may be suffixed by the letter u or U to specify that it is unsigned.

&emsp;&emsp; The type of an integer constant depends on its form value and suffix. If it is unsuffixed and decimal it has these types in which its value can be represented : int,unsigned int and(long int is already included in int). If it is unsuffixed octal or hexadecimal it can be represented : int,unsigned int and the(long versions of them are also covered in these only). If it suffixed by u or U then unsigned int.

#### Character constants
&emsp;&emsp; A character constant is a sequence of one or more characters enclosed in single quotes as in 'x'. The value of a character constant with only one character is the numeric value of the character in the machines character set at execution time. The vaue of a multi character constant is implementation defined.

| Constant | Abberiviation | Symbol|
|----|----|----|
|new line|NL(LF)|\n|
|horizontal tab|HT|\t|
|vertical tab|VT|\v|
|backspace|BS|\b|
|carriage return|CR|\r|
|formfeed|FF|\f|
|audible alert|BEL|\a|
|backslash|\|\\|
|question mark|?|\?|
|single quote|'|\'|
|double quote|"|\"|
|octal number|ooo|\ooo|
|hex number|hh|\xhh|

#### Floating Constants
&emsp;&emsp; 

#### Enumeration Constants
&emsp;&emsp; Identifiers declared as enumarators are constants of type int.

### String Literals
&emsp;&emsp; A string literal also called a string constant is a sequence of characters surrounded by double quotes as in "   ". A string has type "array of characters" and storage class startic and is initialized with the given characters.Whether identical string literals are distinct is implementation defined and the behaviour of a program that attempts to alter a string literal is undefined.

Adjacent string literals are concatenated into a single string.After any concatenation a null byte \0 is appended to the string so that programs that scan the string can find its end.String literal do not contain newline or double quote characters in order to represent them,the same escape sequences as for character constants are available.

## Meaning of Identifiers
&emsp;&emsp; Identifiers or names refer to a variety of things. An object sometimes called a variable is a location in storage and its interpretation depends on two main attributes its storage class and its type.The storage class determines the lifetime of the storage associated with the identified object and the type determines the meaning of the values found in the identified object.A name also has a scope which is the region of the program in which it is known and a linkage which determines whether the same name in another scope refers to the same object or function. 

### Storage Class
&emsp;&emsp; There are two storage classes : automatic and static. Automatic objects are local to a block and are discarded on exit from the block. Declerations within a block create automatic objects if no storage class specification is mentioned or if the auto specifier is used.Objects declared register are automatic and if possible are stored in fast registers of the machine.

&emsp;&emsp; Static objects may be local to a block or external to all blocks but in either case their values across exit from and reentry to functions and blocks.The objects declared outside all blocks at the same level as function definitions are always static.They become global to an entire program by omitting an explicit storage class.

### Basic Types
&emsp;&emsp; Objects declared as characters(char) are large enough to store any number of the execution character set. If a genuine character from that set is stored in a char object its value is equivalent to the integer code for the character and is non negative. Other quantities may be stored into char variables but the avaiable range of values and especially whether the value is signed is implementation dependent.

&emsp;&emsp; Unsigned characters are declared as (unsigned char) and they are always non negative and Signed characters are declared as(signed char) they can be negative or positive.

&emsp;&emsp; There is only one definition for integer(int).There is space generated for long and short int automatically. The int type represents signed values unless specified otherwise.For unsigned integers we need to declare them as (unsigned int) and this type will store only positive values.

&emsp;&emsp; There is only definition for non integer values which is(real) which is used to store values containing decimal places.

&emsp;&emsp; Enumerations are unique types that have integral values associated with each enumeration is a set of named constants.Enumerations behave like integers but it is common for a compiler to issue a warning when an object of a particular enumeration is assigned something other than one of its constants or an expression of its type.

&emsp;&emsp; The void type specifies an empty set of values.It is used as the type returned by functions that generate no value.

### Derived types
&emsp;&emsp; Beside the basic types there is a conceptually infinite class of derived types consructed from the fundamental types in the following ways:

&emsp;ARRAYS of objects of a given type

&emsp;FUNCTIONS returning objects of a given type

&emsp;POINTERS to objects of a given type

&emsp;STRUCTURES containing a sequence of objects of various types.

&emsp;UNIONS capable of containing any of one of several objects of various types.


### Type Qualifiers
&emsp;&emsp; An objects type may have additional qualifiers.Declaring an object const announces that its value will not be changed and declaring it volatile announces that it has special properties relevant to optimization.Neither qualifier affects the range of values or arithmetic properties of the object.
