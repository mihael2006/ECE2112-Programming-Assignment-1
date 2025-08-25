# ECE2112-Programming-Assignment-1
**Introduction to Python Programming**

Name: Padilla, Erich S. 

Section: 2ECE-C

Date Submitted: August 26, 2025

# Description
This programming assignment contains programs that solve three different problems:
1. Alphabet Soup Problem
   * Rearranges the letters of a word entered by the user into alphabetical order.
2. Emoticon Problem
   * Replaces specific words (e.g., smile, sad, mad) with their corresponding emoticons using a dictionary.
3. Unpacking List Problem
   * Takes a list of items from the user and separates them into the first, middle, and last elements.

# Alphabet Soup Problem
This program first takes a word from the user and rearranges its letters in alphabetical order. Using the ```sorted()```, the word is then in alphabetical order, with the addition of ```key=str.lower()``` to ensure that letters are still in alphabetical order even if the user entered one or more capital letters.
```python 
sorted_chars = sorted(w, key=str.lower)
```
Finally, with the use of ```"".join()```, the letters that are now in alphabetical order are joined together without unnecessary space between each letter.
```python
joined_chars = "".join(sorted_chars)
```
### Examples:
* Input: ```hello```
  Output: ```ehllo```
* Input: ```Erich```
  Output: ```cEhir```

# Emoticon Problem
The user is asked first to enter a sentence which the program will try to convert into emojis from the dictionary (see the program). Using the ```.split()``` will break the sentence into a list of words separated by spaces.
```python
word = word.split()
```
For loop is now used through each index of the words from the list, before converting each word into lowercase to match the keys in the dictionary.
```python
for i in range(len(word)):
        lw = word[i].lower()
```
Using the if statement, the program checks if the word matches one of the values from the dictionary before it joins back into the original sentence.
```python
        if lw in emoji:
            word[i] = emoji[lw]
return " ".join(word)
```
### Example:
* Input: ```Make me smile```
  Output: ```Make me :)```

# Unpacking List Problem
Using the function that will process whatever the user enters, the items are again separated using spaces with the ```.split()```. 
```python
your_list = items.split()
```
Slicing this list with ```seq[start:end:step]``` will copy the sequence from index start to index end (last element not included).
```python
    first = your_list[0]
    middle = your_list[1:-1]
    last = your_list[-1]
```
This will give you a list of items that are separated into first, middle, and last elements.
### Example:
* Input: ```1 2 3 4 5 6```
  Output: ```First: 1
Middle: ['2', '3', '4', '5']
Last: 6```

# Version History
* v.01

