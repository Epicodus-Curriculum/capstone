## Whiteboarding Practice - Week 5

Every week during the final two months of the Capstone course, you and your peers will perform a whiteboarding prompt. This will be performed either in front of your peers, or have your instructor join to provide feedback directly. 

Each week, there will be 4 prompts available in lessons titled just like this lesson. The intention behind these prompts is to perform them with as little research or pre-planning as you feel comfortable with, as this will help prepare you for the world of interviewing.

Before reviewing the prompts below, overview the Recap on [Whiteboarding Best Practices](https://full-time.learnhowtoprogram.com/capstone/capstone-week-3/recap-whiteboarding-best-practices). 

Additionally, review the Recap lesson on [Recursion](https://full-time.learnhowtoprogram.com/capstone/capstone-week-3/recap-recursion), and feel free to utilize recursion in instances that you feel most comfortable. 

As one additional layer, use the concepts that you learned during the Computer Science section to help create efficient solutions.

Lastly, you are welcome to choose other prompts from other sources like [LeetCode](https://leetcode.com/). We recommend Easy to Medium prompt levels. 

### Prompts

#### Search in Rotated Sorted Array

You are given an integer array nums sorted in ascending order (with distinct values), which is rotated at an unknown pivot index. You need to find the index of the value `n` in the array.

Example:

```
Input: nums = [4,5,6,7,0,1,2], n = 7
Output: 3
```

<details><summary><strong>Hint 1:</strong></summary>
<p>You can solve this problem using a binary search approach.</p>
</details>
<details><summary><strong>Hint 2:</strong></summary>
<p>Think about how to modify the binary search algorithm to handle the rotated sorted array.</p>
</details>
<details><summary><strong>Hint 3:</strong></summary>
<p>Compare the middle element with the left and right endpoints to determine which half of the array to search.</p>
</details>

---

#### Jump Game

You are given an array of non-negative integers nums where each element represents your maximum jump length at that position. Determine if you can reach the last index.

Example 1:

```
Input: nums = [2,3,1,1,4]
Output: true
```

For further visual, here is how we determined that this array of values returns "true". We can jump like this:

```
 0  1  2  3  4
[2, 3, 1, 1, 4]
 ^
 0  1  2  3  4
[2, 3, 1, 1, 4]
       ^
 0  1  2  3  4
[2, 3, 1, 1, 4]
          ^
 0  1  2  3  4
[2, 3, 1, 1, 4]
             ^
```

Or like this:

```
 0  1  2  3  4
[2, 3, 1, 1, 4]
 ^
 0  1  2  3  4
[2, 3, 1, 1, 4]
    ^
 0  1  2  3  4
[2, 3, 1, 1, 4]
             ^
```


Example 2: 

```
input: [3, 2, 1, 0, 4]
output: false
```

For this example, the result would be false. You will always end at index 3. The value there is 0 so you’re stuck, and no index before that index has a high enough value to jump past it.

```
 0  1  2  3  4
[3, 2, 1, 0, 4]
```
<details><summary><strong>Hint 1:</strong></summary>
<p>You could start at the beginning of the array and use recursion to test every possible jump path. That’s not going to be as good from a time complexity stand point though.</p>
</details>
<details><summary><strong>Hint 2:</strong></summary>
<p>You can solve this problem using greedy approach. (See the [Greedy Algorithm](https://en.wikipedia.org/wiki/Greedy_algorithm)</p>
</details>
<details><summary><strong>Hint 3:</strong></summary>
<p>Iterate through the array and keep track of the furthest index you can reach.</p>
</details>
<details><summary><strong>Hint 4:</strong></summary>
<p>If at any point you cannot reach a certain index, return false.</p>
</details>

---

#### Word Break

Given a string s and a dictionary of strings wordDict, return true if s can be segmented into a space-separated sequence of one or more dictionary words.

All the strings of wordDict are unique.

Note that the same word in the dictionary may be reused multiple times in the segmentation.

Example:

```
Input: s = "leetcode", wordDict = ["leet","code"]
Output: true
```

```
Input: s = "applepenapple", wordDict = ["apple","pen"]
Output: true

```
**Explanation:** Return true because "applepenapple" can be segmented as "apple pen apple".
Note that you are allowed to reuse a dictionary word.

```
Input: s = "catsandog", wordDict = ["cats","dog","sand","and","cat"]
Output: false
```
**Explanation:** Here, no combination of words exist in wordDict that can perfectly recreate the input string s.

"cats" + "dog" will require "an" in wordDict in order to recreate s

"cats" + "and" will require "og" in wordDict in order to recreate s

"cat" + "sand" will require "og" in wordDict in order to recreate s

And so on.

<details><summary><strong>Hint 1:</strong></summary>
<p>You can solve this problem using dynamic programming.</p>
</details>
<details><summary><strong>Hint 2:</strong></summary>
<p>Define a boolean array to store whether substrings are breakable.</p>
</details>
<details><summary><strong>Hint 3:</strong></summary>
<p>Use dynamic programming to fill the boolean array by checking if the current substring can be segmented using words from the dictionary.</p>
</details>
<details><summary><strong>Hint 4 (Solution):</strong></summary>
<p>

```js
var wordBreak = function (s, wordDict) {
    const n = s.length;

    // Create a Set of words from the array so that the
    // lookup cost in the Set becomes O(1)
    const wordSet = new Set(wordDict);

    // Initialize the lookup table
    const dp = new Array(n + 1).fill(false);

    // Set the first element to true as it represents the
    // empty string
    dp[0] = true;

    for (let i = 1; i <= n; i++) {
        for (let j = 0; j < i; j++) {
            // Checking if the substring from j to i is
            // present in the wordSet and dp[j] is true
            if (dp[j] && wordSet.has(s.substring(j, i))) {
                dp[i] = true;
                // If a substring is found, no need to check
                // further smaller substrings
                break;
            }
        }
    }

    // Return the last element of dp array
    return dp[n];
};
```
</p>
</details>

---

#### Sliding Window

Given an array `data` containing integers, an integer `n`, and an integer `m`, return a nested array containing all subarrays within the window with size of `n` using `m` as the distance between the start of each window.


Ex: 

```
Input: array = [1, 2, 3, 4, 5], n = 3, m = 2
Output: [[1, 2, 3], [3, 4, 5]]
```

Explanation: 

`n` represents the size of the window, which defines the length of the subarray elements. 
`m` represents how many indecies we jump to create subarrays following the first window. 

So, given `n` is 3, we know our subarrays will have a length of 3. And given `m` is 2, we will build new subarrays every 2 indexes, like so: 

```
 0  1  2  3  4
[1, 2, 3, 4, 5] 
 ^     ^
 ```
 Starting at index 0, we find our first subarray (window) using `n`, which is 3. So the first subarray is `[1, 2, 3]`
 
 ```
0  1  2  3  4
[1, 2, 3, 4, 5] 
       ^     ^
```

We then use `m` to jump to the next window location. Because `m` is 2, we jump two indexes to retrieve the next subarray, which is `[3, 4, 5]`

Once we reach the end of the data array, we return all subarrays. 





