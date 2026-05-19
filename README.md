# Check if Strings are Rotations of Each Other

This repository contains my Java solution for the GeeksforGeeks problem:

🔗 Problem Link: https://www.geeksforgeeks.org/problems/check-if-strings-are-rotations-of-each-other-or-not-1587115620/1

---

## 📌 Problem Statement

Given two strings `s1` and `s2`, check whether `s2` is a rotation of `s1`.

A string is considered a rotation of another string if it can be obtained by moving characters from the beginning to the end.

### Example
Input:
s1 = "ABCD"
s2 = "CDAB"

Output:
true

Explanation:
"CDAB" is a rotation of "ABCD".

---

## 🚀 Approach

### Logic Used
1. First check whether both strings have the same length.
2. Concatenate the first string with itself.
3. Check whether the second string exists inside the concatenated string.
4. If yes → Strings are rotations.
5. Else → Not rotations.

---

## 💡 Key Idea

If `s2` is a rotation of `s1`, then it will always be a substring of:

```java
s1 + s1

Example:

s1 = "ABCD"

s1 + s1 = "ABCDABCD"

s2 = "CDAB"

Since "CDAB" exists inside "ABCDABCD", it is a rotation.

🧠 Java Solution
class Solution {
    public boolean areRotations(String s1, String s2) {

        if(s1.length() != s2.length()) {
            return false;
        }

        return (s1 + s1).contains(s2);
    }
}
⏱️ Time Complexity
Concatenation: O(n)
contains() check: O(n)
Overall Complexity: O(n)
📚 Concepts Used
Strings
String Concatenation
Substring Checking
Rotation Logic
🎯 What I Learned
Efficient way to check string rotations
Using string concatenation smartly
Working with Java String methods
Solving string-based DSA problems with optimized logic
🔗 GitHub Profile

https://github.com/chintalaAjay
