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


&emsp;&emsp;&emsp;&emsp;| auto | real | int | struct |

&emsp;&emsp;&emsp;&emsp;| if | else | switch | case |

&emsp;&emsp;&emsp;&emsp;| enum | register | typedef | extern |

&emsp;&emsp;&emsp;&emsp;| return | union | char | const |

&emsp;&emsp;&emsp;&emsp;| continue | repeat | void | default |

&emsp;&emsp;&emsp;&emsp;| goto | sizeof | volatile | static |

### Constants
&emsp;&emsp; There are several kinds of constants.Each has a data type 

### String Literals
&emsp;&emsp; A string literal also called a string constant is a sequence of characters surrounded by double quotes as in "   ". A string has type "array of characters" and storage class startic and is initialized with the given characters.Whether identical string literals are distinct is implementation defined and the behaviour of a program that attempts to alter a string literal is undefined.

Adjacent string literals are concatenated into a single string.After any concatenation a null byte \0 is appended to the string so that programs that scan the string can find its end.String literal do not contain newline or double quote characters in order to represent them,the same escape sequences as for character constants are available.

## Meaning of Identifiers

