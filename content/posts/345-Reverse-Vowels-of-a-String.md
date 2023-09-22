---
title: "345. Reverse Vowels of a String"
date: 2023-09-22T17:00:00+08:00
draft: false
tags: ["LeetCode"]
---
### 345. Reverse Vowels of a String
```go
func isVowel(char rune) bool {
    // converting the char to lower case to ensure case insensitivity
    char = unicode.ToLower(char)
    // checking whether the given char is a vowel
	return char == 'a' || char == 'e' || char == 'i' || char == 'o' || char == 'u'
}

func reverseVowels(inputString string) string {
    runes := []rune(inputString)  // converting the string to a slice of runes
    strLength := len(runes)  // storing the length of the runes slice
    leftPointer, rightPointer := 0, strLength - 1  // initializing the pointers
    
    // looping until the left pointer is less than the right pointer
    for leftPointer < rightPointer {
        // finding the index of the first vowel from the left
        for leftPointer < rightPointer && !isVowel(runes[leftPointer]) {
            leftPointer += 1
        }
        // finding the index of the first vowel from the right
        for rightPointer > leftPointer && !isVowel(runes[rightPointer]) {
            rightPointer -= 1
        }
        
        // swapping the vowels
        runes[leftPointer], runes[rightPointer] = runes[rightPointer], runes[leftPointer]
        
        // moving the pointers inward
        leftPointer += 1
        rightPointer -= 1
    }
    // converting the slice of runes back to a string
    return string(runes)
}
```
