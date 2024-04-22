## Whiteboarding Practice - Week 6

Every week during the final two months of the Capstone course, you and your peers will perform a whiteboarding prompt. This will be performed either in front of your peers, or have your instructor join to provide feedback directly. 

Each week, there will be 4 prompts available in lessons titled just like this lesson. The intention behind these prompts is to perform them with as little research or pre-planning as you feel comfortable with, as this will help prepare you for the world of interviewing.

Before reviewing the prompts below, overview the Recap on [Whiteboarding Best Practices](https://full-time.learnhowtoprogram.com/capstone/capstone-week-3/recap-whiteboarding-best-practices). 

Additionally, review the Recap lesson on [Recursion](https://full-time.learnhowtoprogram.com/capstone/capstone-week-3/recap-recursion), and feel free to utilize recursion in instances that you feel most comfortable. 

As one additional layer, use the concepts that you learned during the Computer Science section to help create efficient solutions.

Lastly, you are welcome to choose other prompts from other sources like [LeetCode](https://leetcode.com/). We recommend Easy to Medium prompt levels. 

### Prompts

#### Symmetric Tree

Given the root of a binary tree, check whether it is a mirror of itself (i.e., symmetric around its center).

Example:

```
Input: root = [1,2,2,3,4,4,3]
Output: true
```

<details><summary><strong>Hint 1:</strong></summary>
<p>You can solve this problem using recursion.</p>
</details>
<details><summary><strong>Hint 2:</strong></summary>
<p>Define a helper function to check if two subtrees are mirrors of each other.</p>
</details>
<details><summary><strong>Hint 3:</strong></summary>
<p>Recursively compare the left subtree of one node with the right subtree of the other node.</p>
</details>

---

#### Reverse Linked List

Reverse a singly linked list.

Example:

```
Input: 1 -> 2 -> 3 -> 4 -> 5
Output: 5 -> 4 -> 3 -> 2 -> 1

```

<details><summary><strong>Hint 1:</strong></summary>
<p>You can solve this problem iteratively or recursively.</p>
</details>
<details><summary><strong>Hint 2:</strong></summary>
<p>For the iterative approach, use three pointers to reverse the connections while traversing the list.</p>
</details>
<details><summary><strong>Hint 3:</strong></summary>
<p>For the recursive approach, recursively reverse the rest of the list and then adjust the pointers.</p>
</details>

---

#### Valid Sudoku

Determine if a 9 x 9 Sudoku board is valid. Only the filled cells need to be validated according to the following rules:

- Each row must contain the digits 1-9 without repetition.
- Each column must contain the digits 1-9 without repetition.
- Each of the nine 3 x 3 sub-boxes of the grid must contain the digits 1-9 without repetition.

The Sudoku board could be partially filled, where empty cells are filled with the character '.'.

Example:

```
Input:
[
  ["5","3",".",".","7",".",".",".","."],
  ["6",".",".","1","9","5",".",".","."],
  [".","9","8",".",".",".",".","6","."],
  ["8",".",".",".","6",".",".",".","3"],
  ["4",".",".","8",".","3",".",".","1"],
  ["7",".",".",".","2",".",".",".","6"],
  [".","6",".",".",".",".","2","8","."],
  [".",".",".","4","1","9",".",".","5"],
  [".",".",".",".","8",".",".","7","9"]
]
Output: true

```


<details><summary><strong>Hint 1:</strong></summary>
<p>You can solve this problem by checking each row, column, and sub-box separately.</p>
</details>
<details><summary><strong>Hint 2:</strong></summary>
<p>Use sets or arrays to keep track of the digits seen in each row, column, and sub-box.</p>
</details>
<details><summary><strong>Hint 3:</strong></summary>
<p>Iterate through each cell in the Sudoku board and verify if the current cell's digit is already present in its respective row, column, and sub-box.</p>
</details>

---

#### Coin Change
You are given coins of different denominations and a total amount of money amount. Write a function to compute the minimum number of coins needed to make up that amount. If that amount of money cannot be made up by any combination of the coins, return -1.

Example:

```
Input: coins = [1, 2, 5], amount = 11
Output: 3
```

<details><summary><strong>Hint 1:</strong></summary>
<p>You can solve this problem using dynamic programming.</p>
</details>
<details><summary><strong>Hint 2:</strong></summary>
<p>Define an array to store the minimum number of coins needed for each amount from 0 to the target amount.</p>
</details>
<details><summary><strong>Hint 3:</strong></summary>
<p>Use dynamic programming to fill the array by finding the minimum number of coins for each amount.</p>
</details>





