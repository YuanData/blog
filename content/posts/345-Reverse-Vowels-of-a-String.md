---
title: "345. Reverse Vowels of a String"
date: 2023-09-22T17:00:00+08:00
lastmod: 2023-09-23T11:00:00+08:00
draft: false
tags: ["LeetCode"]
---
### 345. Reverse Vowels of a String.py
```python
class Solution:
    def reverseVowels(self, s: str) -> str:
        lst = list(s)
        n = len(s)
        vowels = list("aeiouAEIOU")
        l, r = 0, n - 1
        while l < r:
            while l < r and lst[l] not in vowels:
                l += 1
            while r > l and lst[r] not in vowels:
                r -= 1
            lst[l], lst[r] = lst[r], lst[l]  # swapping the vowels

            l += 1
            r -= 1
        return "".join(lst)


if __name__ == '__main__':
    sol = Solution()
    assert sol.reverseVowels("hello") == "holle"
    assert sol.reverseVowels("leetcode") == "leotcede"
```

### lc345ReverseVowelsofaString.go
```go
package lc

import "unicode"

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
### lc345ReverseVowelsofaString_test.go
```go
package lc

import (
	"testing"
)

func TestReverseVowels(t *testing.T) {
	testCases := []struct {
		input  string
		output string
	}{
		{"hello", "holle"},
		{"leetcode", "leotcede"},
		{"aeiou", "uoiea"},
		{"", ""},       // empty string
		{"bcd", "bcd"}, // string with no vowels
		{"Aa", "aA"},   // case sensitivity
	}

	for _, testCase := range testCases {
		actualOutput := reverseVowels(testCase.input)
		if actualOutput != testCase.output {
			t.Errorf("For input %q, expected %q, but got %q", testCase.input, testCase.output, actualOutput)
		}
	}
}

```
