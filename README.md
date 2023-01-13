# interview-prep

This repo is simply a markdown file containing notes and submitted solutions for some LeetCode problems I've come across.

# Important Concepts

## [Big O](https://en.wikipedia.org/wiki/Big_O_notation)
---

Big O is a BIG DEAL!

Big O is a mathematical notation used to describe an algorithm's *time* and *space* requirements as the input size grows. The `n` represents the input.

Solving DSA problems generally means writing a function that accepts an input, performs operations based on that input, and returns a result. The operations performed will contribute to the *time complexity,* and any data stored in memory during the function call contribute to the overall *space complexity*. So, in order to talk about an algorithm's Big O, you should be able to identify the time and space taken up by the operations.

Some optimization patterns are easy to recognize, and others make use of mathematical formulas you've neither heard of nor will ever use again, outside of that particular algorithm's niche... 

Big O is tied directly to data structures as well. When considering whether to use an array or a hash map, your decision should be influenced by more than just personal preference--there are computational advantages and disadvantages. In other words, there is a difference you can talk about in terms of Big O.

Here are two tables to refer to. I'll break down each notation below.

&nbsp;

<div style='width: 100%; display: flex; flex-direction: column; align-items: center; justify-content: center; font-size: 12px;'>
    <h3>Table 1.1 Big: O</h3>
    <table style='width: 620px;'>
    <tr>
        <th style='width: 100px;'>Data Structure</th>
        <th>Access</th>
        <th>Search</th>
        <th>Insertion</th>
        <th>Deletion</th>
        <th>Space</th>
    </tr>
    <tr>
        <td style='vertical-align: top'>Array</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>O(n)</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Linked List</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(n)</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Stack</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(n)</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Heap</td>
        <td style='vertical-align: top'>O(log n)</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>O(log n)</td>
        <td style='vertical-align: top'>O(log n)</td>
        <td style='vertical-align: top'>O(n)</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Queue</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(n)</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Hash Table</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(n)</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Binary Search Tree</td>
        <td style='vertical-align: top'>O(log n)</td>
        <td style='vertical-align: top'>O(log n)</td>
        <td style='vertical-align: top'>O(log n)</td>
        <td style='vertical-align: top'>O(log n)</td>
        <td style='vertical-align: top'>O(n)</td>
    </tr>
    </table>
</div>

&nbsp;

<div style='width: 100%; display: flex; flex-direction: column; align-items: center; justify-content: center; font-size: 12px;'>
<h3>Table 1.2: Big O Continued</h3>
    <table style='width: 620px;'>
    <tr>
        <th style='width: 100px;'>Data Structure</th>
        <th>Random access</th>
        <th style='width: 65px;'>Sorting</th>
        <th style='width: 65px;'>Memory</th>
        <th>Dynamic resizing</th>
        <th>Duplicate elements</th>
        <th>Range query</th>
    </tr>
    <tr>
        <td style='vertical-align: top'>Array</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>O(n log n)</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>Yes</td>
        <td style='vertical-align: top'>Yes</td>
        <td style='vertical-align: top'>O(n)</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Linked List</td>
        <td style='vertical-align: top'>N/A</td>
        <td style='vertical-align: top'>N/A</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>No</td>
        <td style='vertical-align: top'>Yes</td>
        <td style='vertical-align: top'>N/A</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Stack</td>
        <td style='vertical-align: top'>N/A</td>
        <td style='vertical-align: top'>N/A</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>No</td>
        <td style='vertical-align: top'>Yes</td>
        <td style='vertical-align: top'>N/A</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Heap</td>
        <td style='vertical-align: top'>N/A</td>
        <td style='vertical-align: top'>O(n log n)</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>No</td>
        <td style='vertical-align: top'>No</td>
        <td style='vertical-align: top'>N/A</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Queue</td>
        <td style='vertical-align: top'>N/A</td>
        <td style='vertical-align: top'>N/A</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>No</td>
            <td style='vertical-align: top'>Yes</td>
        <td style='vertical-align: top'>N/A</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Hash Table</td>
        <td style='vertical-align: top'>O(1)</td>
        <td style='vertical-align: top'>N/A</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>No</td>
        <td style='vertical-align: top'>No</td>
        <td style='vertical-align: top'>N/A</td>
    </tr>
    <tr>
        <td style='vertical-align: top'>Binary Search Tree</td>
        <td style='vertical-align: top'>O(log n)</td>
        <td style='vertical-align: top'>N/A</td>
        <td style='vertical-align: top'>O(n)</td>
        <td style='vertical-align: top'>No</td>
        <td style='vertical-align: top'>No</td>
        <td style='vertical-align: top'>O(log n)</td>
    </tr>
    </table>
</div>

&nbsp;

Each time one of those operations is performed on a data structure in your algorithm, you contribute to the time complexity. One of the important methods you'll do is `traversal`, which is enumerating through a data structure. It's O(n) when you're exploring every element, node, or key-value pair in your data structure, since the time it takes increases `linearly` with the size of the data structure.

Let's talk about what it all means!

### Constant: O(1)
### Logarithmic: O(log n)
### Linear: O(n)
### Linearithmic: O(nlog n)
### Quadratic: O(n<sup>2</sup>)
### Exponential: O(2<sup>n</sup>)
### Factorial: O(n!)

&nbsp;

Need more Big O? **Here's an [exhaustive list](https://en.wikipedia.org/wiki/Time_complexity#Table_of_common_time_complexities) that can be ordered by running time.**
 
&nbsp;

## [Data Structures](https://en.wikipedia.org/wiki/Data_structure)
---

Depending on the scope of your programming journey, arrays and hash maps may have been sufficient for 99% of the practical situation's you've been in. 

### Arrays
### Hashes
### Linked Lists
### Singly Linked Lists
### Doubly Linked Lists
### Trees
### Binary Search Trees
### Binary Heaps
### Graphs


&nbsp;

# Approaching Algorithims

## Intuition

## Iteration

## Optimization

## Don't be discouraged!

&nbsp;

# Problems

## [Design Underground System](https://leetcode.com/problems/design-underground-system/)
## [Remove All Adjacent Duplicates in String II](https://leetcode.com/problems/remove-all-adjacent-duplicates-in-string-ii/)
## [Design A Leaderboard](https://leetcode.com/problems/design-a-leaderboard/)
## [Flatten a Multilevel Doubly Linked List](https://leetcode.com/problems/flatten-a-multilevel-doubly-linked-list/)
## [Two City Scheduling](https://leetcode.com/problems/two-city-scheduling/)
## [Insert Delete GetRandom O(1)](https://leetcode.com/problems/insert-delete-getrandom-o1/)
## [Design an Ordered Stream](https://leetcode.com/problems/design-an-ordered-stream/)
## [Invalid Transactions](https://leetcode.com/problems/invalid-transactions/)
## [Candy Crush](https://leetcode.com/problems/candy-crush/)
## [Decode String](https://leetcode.com/problems/decode-string/)
## [Number of Ships in a Rectangle](https://leetcode.com/problems/number-of-ships-in-a-rectangle/)
## [Count Unhappy Friends](https://leetcode.com/problems/count-unhappy-friends/)
## [Minimum Remove to Make Valid Parentheses](https://leetcode.com/problems/minimum-remove-to-make-valid-parentheses/)
## [Add Two Numbers II](https://leetcode.com/problems/add-two-numbers-ii/)
## [First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/)
## [Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
## [Valid Anagram](https://leetcode.com/problems/valid-anagram/)
## [Insert Delete GetRandom O(1) - Duplicates allowed](https://leetcode.com/problems/insert-delete-getrandom-o1-duplicates-allowed/)
## [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
## [Two Sum](https://leetcode.com/problems/two-sum/)
## [Pow(x, n)](https://leetcode.com/problems/powx-n/)
## [Gas Station](https://leetcode.com/problems/gas-station/)
## [Roman to Integer](https://leetcode.com/problems/roman-to-integer/)
## [Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
## [Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
## [Unique Number of Occurrences](https://leetcode.com/problems/unique-number-of-occurrences/)
## [Minimum Size Subarray Sum](https://leetcode.com/problems/minimum-size-subarray-sum/)
## [Longest Common Prefix](https://leetcode.com/problems/longest-common-prefix/)
## [Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
## [Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
## [Palindrome Number](https://leetcode.com/problems/palindrome-number/)
## [Unique Binary Search Trees](https://leetcode.com/problems/unique-binary-search-trees/)
## [Two Sum II - Input Array Is Sorted](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
## [Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)
## [Majority Element](https://leetcode.com/problems/majority-element/)
## [Sum of All Odd Length Subarrays](https://leetcode.com/problems/sum-of-all-odd-length-subarrays/)
## [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/)
## [Remove Duplicates from Sorted List II](https://leetcode.com/problems/remove-duplicates-from-sorted-list-ii/)
## [Find the Duplicate Number](https://leetcode.com/problems/find-the-duplicate-number/)
## [Fibonacci Number](https://leetcode.com/problems/fibonacci-number/)
## [Contains Duplicate II](https://leetcode.com/problems/contains-duplicate-ii/)
## [Max Points on a Line](https://leetcode.com/problems/max-points-on-a-line/)
## [Remove Duplicates from Sorted List](https://leetcode.com/problems/remove-duplicates-from-sorted-list/)
## [Single Number](https://leetcode.com/problems/single-number/)
## [Binary Tree Inorder Traversal](https://leetcode.com/problems/binary-tree-inorder-traversal/)
## [Find Pivot Index](https://leetcode.com/problems/find-pivot-index/)
## [Binary Tree Preorder Traversal](https://leetcode.com/problems/binary-tree-preorder-traversal/)
## [Binary Search](https://leetcode.com/problems/binary-search/)
## [Same Tree](https://leetcode.com/problems/same-tree/)
## [Binary Tree Postorder Traversal](https://leetcode.com/problems/binary-tree-postorder-traversal/)