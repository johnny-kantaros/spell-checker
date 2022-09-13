# Spell-checker

## Introduction

For my final project in CS201, I created a high-level Spell-Checker algorithm (written in Java).
Below, I will briefly elaborate on the different classes and methodology of my implementation.


## Methodology


SpellChecker & SpellSorter classes:


These two classes are very similar, with the main difference being SpellSorter's extra output file.

Both of these files will complete the following operations:

-Take in dictionary file as parameter, store in Quadratic Probing Hash Table (QPHT)

-Prompt user for a file to be spell checked

-Prompt user whether user wants to print words, enter new file, or quit

-When user enters p, program will iterate through file, line by line

-For each misspelled word, it will store bucket style (to be sorted later) by their first letter (case sensitive)

-Will prompt user what action they would like to choose for misspelled word

-Will attempt to replace word with suggestions

-At the end of the program, it will output a corrected file, and an order file (chronological order of misspelled words)

** see code for description of each method


In SpellSorter

-used quicksort and insertionsort to sort each bucket of misspelled words and return file of sorted misspelled words.


## Replacement methods


** If I had more time, I would try to implement more replacement methods. 

As of now, only the following three are implemented:


### Delete:

Tries to delete each character in misspelled word to account for extra character typo


### Swap:

Swaps each pair of adjacent characters to account for order typo



### Split:

Tries to split the word in multiple 2 word combinations to account for user forgetting a space.


## Other classes


### Word.java


In this class, I created a word object with a few data fields:

-text: string, actual text of word.

-ignored: boolean, if true, a duplicate word will be skipped. 

-replaced: boolean, if true, user has decided to replace word.

-replacement: string, word that acts as replacement when replaced = true.

-linenum: array list of integers, keeps track of line numbers for words for output file

Each of these data fields has corresponding setter / getter methods




### QuadraticProbingHashTable.java

-Written by Mark Allen Weiss
-Contains necessary implementation / methods in order to use QPHT

## Technologies Used

Java 14.0.2



