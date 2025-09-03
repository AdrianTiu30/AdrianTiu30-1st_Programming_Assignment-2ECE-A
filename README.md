# AdrianTiu30/TIU_Marc_Adrian/-2ECE-A

# Programming Assignment 1

This repository presents the explanation of my submitted code for 
**ECE2112: Advanced Computer Programming and Algorithm**.

## 1. Alphabet Soup Problem
**Goal:** Arrange the letters of the given word in alphabetical order.

**Process:**
- The user will enter a word that the code will sort into alphabetical order and then print the original word along with the sorted word at the bottom.

**Step-by-step:**
1. Ask the user to write a word.
2. The word will then be sorted into alphabetical order.
3. The original word is printed.
4. The sorted word is printed below the original.

## Code Snippet:
```
def alphabet(word):
    return ''.join(sorted(word))

word = input("Enter a word: ")
print("Your word:", word)
print("Sorted:", alphabet(word))
```

## Result:
```
Input: banana
Output: aaabnn
```

## 2. Emoticon Problem
**Goal:** Replace words ("smile", "sad", "mad", and "grin") with their corresponding emoticons and then print the emotified sentence.

**Process:**
- The user enters a sentence or phrase, and the code will check the words to see if any match the keys in the dictionary. The words **"smile"**, **"sad"**, **"mad"**, and **"grin"** are converted into their emoticon counterparts. The code works by splitting the sentence into individual words and then checking if any words are similar to the keys in the dictionary by passing them into the function emoticon_map. The words that match the keys in the dictionary are swapped and returned, and then concatenated into an empty string. The output is then printed along with the original sentence.

**Step-by-step:**
1. Ask the user to write a sentence.
2. The sentence is then split and checked by the method to identify matching words.
3. Words that matched are replaced by emoticons and then returned.
4. The original sentence is printed.
5. The emotified sentence is printed right after the original sentence.

## Code Snippet:
```
def emoticon_map(sentence):
    emoticons = {
    "smile": ":)",
    "sad": ":(",
    "mad": ">:(",
    "grin": ":D"
    }

    words = sentence.split()
    result = [emoticons.get(word.lower(), word) for word in words]
    return " ".join(result)

sentence = input("Write a sentence with (smile, sad, mad, grin): ")
print("Your sentence:", sentence)
print("emotified sentence:", emoticon_map(sentence))
```

## Result:
```
Input: Programming makes me sad
Output: Programming makes me :(
```

## 3. Unpacking List Problem
**Goal:** Unpack the list and arrange it into order (First, Middle, and Last)

**Process:**
- The user will enter a list of numbers or words that are separated by a comma that they would like to unpack and arrange. The code will arrange the contents of the list into three parts (First, Middle, and Last). The code will then print the arranged input of the user with the First on top, the Middle below it, and the Last on the bottom. The comma will also be replaced with spacings in the output.

**Step-by-step:**
1. Ask the user for input.
2. The inputted list will be unpacked and arranged into three parts (First, Middle, and Last).
3. The comma is replaced with spacings.
4. The arranged list is printed in order.

## Code Snippet:
```
def unpack_list(lst):
    first, *middle, last = lst
    return first, middle, last

user_input = input("Create a list: ")
lst = [int(x) for x in user_input.replace(',', ' ').split()]

first, middle, last = unpack_list(lst)

print("First:", first)
print("Middle:", middle)
print("Last:", last)
```

## Result
```
Input: 1, 2, 3, 4, 5, 6
Output: First: 1
        Middle: [2, 3, 4, 5]
        Last: 6
```
