# Revising common Interview Questions

Following leetcode most asked questions



## Q1 (Easy) - Valid Anagrams

Q. Check if two strings are anagrams

**Method 1**

We have an array of length 26 with each representing the difference in frequency of char in that string position. By iterating through the strings we add if that char in 's' and subtract if in 't'. If the resultant array has 0 in all positions then it is an anagram.



```python
class Solution:
    def isAnagram(self, s: str, t: str) -> bool:
        if len(s) != len(t):
            return False

        count = [0] * 26
        for i in range(len(s)):
            count[ord(s[i]) - ord('a')] += 1
            count[ord(t[i]) - ord('a')] -= 1

        for val in count:
            if val != 0:
                return False
        return True
```

**Method 2**

We start with initial window starting for string index 0 to k. Count the number of vowels in that and store in vowelCount. Now you increase the right pointer and left pointer and simply change the vowelCount by checking the first and last index of the window

```python
class Solution:
    def maxVowels(self, s: str, k: int) -> int:
        vowels = {'a', 'e', 'i', 'o', 'u'}
        
        # Build the window of size k, count the number of vowels it contains.
        vowelCount = 0
        for i in range(k):
            vowelCount += int(s[i] in vowels)
        answer = count
        
        # Slide the window to the right, focus on the added character and the
        # removed character and update "count". Record the largest "count".
        for i in range(k, len(s)):
            vowelCount += int(s[i] in vowels)
            vowelCount -= int(s[i - k] in vowels)
            answer = max(answer, count)
        
        return answer
```



## Q2 (Easy) - Valid Anagrams
## Q1 (Easy) - Valid Anagrams
## Q1 (Easy) - Valid Anagrams
## Q1 (Easy) - Valid Anagrams
## Q1 (Easy) - Valid Anagrams
## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

