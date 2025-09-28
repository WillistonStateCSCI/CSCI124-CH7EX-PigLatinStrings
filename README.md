# CSCI124-CH7EX-PigLatinStrings
Programming Example: Pig Latin Strings from Chapter 7 of from C++ Programming: From Problem Analysis to Program Design by D.S. Malik  

In this programming example, we write a program that prompts the user to input a
string and then outputs the string in the pig Latin form. The rules for converting a
string into pig Latin form are as follows:
1. If the string begins with a vowel, add the string **"-way"** at the end
of the string. For example, the pig Latin form of the string **"eye"** is
**"eye-way"**.
2. If the string does not begin with a vowel, first add **"-"** at the end of
the string. Then rotate the string one character at a time; that is,
move the first character of the string to the end of the string until the
first character of the string becomes a vowel. Then add the string
**"ay"** at the end. For example, the pig Latin form of the string
**"There"** is **"ere-Thay"**.
3. Strings such as **"by"** contain no vowels. In cases like this, the letter
**y** can be considered a vowel. So, for this program, the vowels are
**a, e, i, o, u, y, A, E, I, O, U,** and **Y**. Therefore, the pig Latin form
of **"by"** is **"y-bay"**.
4. Strings such as **"1234"** contain no vowels. The pig Latin form
of the string **"1234"** is **"1234-way"**. That is, the pig Latin form
of a string that has no vowels in it is the string followed by the
string **"-way"**.  
**Input:** Input to the program is a string.  
**Output:** Output of the program is the string in the pig Latin form.
## Problem Analysis and Algorithm Design

Suppose that **str** denotes a string. To convert **str** into pig Latin, check the first
character, **str[0]**, of **str**. If **str[0]** is a vowel, add **"-way"** at the end of **str**—
that is, **str = str + "-way"**.  

Suppose that the first character of **str**, **str[0]**, is not a vowel. First, add **"-"** at the
end of the string. Then, remove the first character of **str** from **str** and put it at the
end of **str**. Now, the second character of **str** becomes the first character of **str**.  

This process of checking the first character of **str** and moving it to the end of **str** if
the first character of **str** is not a vowel is repeated until either the first character of
**str** is a vowel or all the characters of **str** are processed, in which case **str** does not
contain any vowels.  

In this program, we write a function **isVowel** to determine whether a character is a
vowel, a function **rotate** to move the first character of **str** to the end of **str**, and
a function **pigLatinString** to find the pig Latin form of **str**.

The previous discussion translates into the following algorithm:
1. Get **str**.
2. Find the pig Latin form of **str** by using the function **pigLatinString**.
3. Output the pig Latin form of **str**.  

**Note:  More in-depth discussion of this code can be found in Chapter 7 of C++ Programming: From Problem Analysis to Program Design by D.S. Malik**
