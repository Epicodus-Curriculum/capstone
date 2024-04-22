## Whiteboarding Practice - Week 6

Every week during the final two months of the Capstone course, you and your peers will perform a whiteboarding prompt. This will be performed either in front of your peers, or have your instructor join to provide feedback directly. 

Each week, there will be 4 prompts available in lessons titled just like this lesson. The intention behind these prompts is to perform them with as little research or pre-planning as you feel comfortable with, as this will help prepare you for the world of interviewing.

Before reviewing the prompts below, overview the Recap on [Whiteboarding Best Practices](https://full-time.learnhowtoprogram.com/capstone/capstone-week-3/recap-whiteboarding-best-practices). 

Additionally, review the Recap lesson on [Recursion](https://full-time.learnhowtoprogram.com/capstone/capstone-week-3/recap-recursion), and feel free to utilize recursion in instances that you feel most comfortable. 

As one additional layer, use the concepts that you learned during the Computer Science section to help create efficient solutions.

Lastly, you are welcome to choose other prompts from other sources like [LeetCode](https://leetcode.com/). We recommend Easy to Medium prompt levels. 

### Prompts

#### Climbing Stairs

You are climbing a staircase. It takes n steps to reach the top.

Each time you can either climb 1 or 2 steps. In how many distinct ways can you climb to the top?

Example:

```
Input: n = 3
Output: 3
Explanation: There are three ways to climb to the top: 1 step + 1 step + 1 step, 1 step + 2 steps, 2 steps + 1 step.

```

<details><summary><strong>Hint 1:</strong></summary>
<p>You can solve this problem using dynamic programming.</p>
</details>
<details><summary><strong>Hint 2:</strong></summary>
<p>Define an array to store the number of distinct ways to climb to each step.</p>
</details>
<details><summary><strong>Hint 3:</strong></summary>
<p>Use dynamic programming to fill the array by considering the number of ways to climb to the current step based on the previous steps.</p>
</details>

---

#### Find All Anagrams in a String

Given a string s and a non-empty string p, find all the start indices of p's anagrams in s.

Strings consist of lowercase English letters only and the length of both strings s and p will not be larger than 20,100.

Example:

```
Input: s = "cbaebabacd", p = "abc"
Output: [0, 6]
```

<details><summary><strong>Hint 1:</strong></summary>
<p>You can solve this problem using a sliding window approach.</p>
</details>
<details><summary><strong>Hint 2:</strong></summary>
<p>Use a hashmap to store the frequencies of characters in `p`.</p>
</details>
<details><summary><strong>Hint 3:</strong></summary>
<p>Use two pointers to create a sliding window over `s` and maintain a hashmap for the current window.</p>
</details>

---

#### Unique Paths

A robot is located at the top-left corner of a m x n grid. The robot can only move either down or right at any point in time. The robot is trying to reach the bottom-right corner of the grid.

How many possible unique paths are there?

Example:

```
Input: m = 3, n = 7
Output: 28
```


<details><summary><strong>Hint 1:</strong></summary>
<p>You can solve this problem using dynamic programming.</p>
</details>
<details><summary><strong>Hint 2:</strong></summary>
<p>Define a 2D array to store the number of unique paths for each cell in the grid.</p>
</details>
<details><summary><strong>Hint 3:</strong></summary>
<p>Use dynamic programming to fill the array by considering the number of unique paths for each cell based on the previous cells.</p>
</details>

---

#### Longest Common Subsequence

Given two strings text1 and text2, return the length of their longest common subsequence.

A subsequence of a string is a new string generated from the original string with some characters(can be none) deleted without changing the relative order of the remaining characters. (e.g., "ace" is a subsequence of "abcde" while "aec" is not).

Example:


```
Input: text1 = "abcde", text2 = "ace"
Output: 3

Input: text1= "abcd", text2 = "ace"
Ouput: 2 // ("ac" is a subsequence of both "abcd" and "ace")
```

<details><summary><strong>Hint 1:</strong></summary>
<p>You can solve this problem using dynamic programming.</p>
</details>
<details><summary><strong>Hint 2:</strong></summary>
<p>Define a 2D array to store the lengths of the longest common subsequences.</p>
</details>
<details><summary><strong>Hint 3:</strong></summary>
<p>Use dynamic programming to fill the array by considering the lengths of the longest common subsequences for substrings of the two input strings.</p>
</details>





