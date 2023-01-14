# interview-prep

This repo is simply a markdown file containing notes and submitted solutions for some LeetCode problems I've come across.

# Important Concepts

## [Big O](https://en.wikipedia.org/wiki/Big_O_notation)


Big O is a BIG DEAL!

Big O is a mathematical notation used to describe an algorithm's *time* and *space* requirements as the input size grows. The `n` represents the input.

Solving DSA problems generally means writing a function that accepts an input, performs operations based on that input, and returns a result. The operations performed will contribute to the *time complexity,* and any data stored in memory during the function call contribute to the overall *space complexity*. So, in order to talk about an algorithm's Big O, you should be able to identify the time and space taken up by the operations.

Your understanding of Big O will help you optimize your algorithms for time and space efficiency. Some optimization patterns are easy to recognize, and others make use of mathematical formulas you've neither heard of, nor will ever use again, outside of that particular algorithm's niche...

Big O is tied directly to data structures as well. **Don't listen to those TikToks that say using arrays over hashes is just personal preference.** there are computational advantages and disadvantages, which you can talk about using Big O. The same concepts that can make algorithms more efficient can also be applied to applications! So, this info isn't completely useless..!

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

## Constant: O(1)

An algorithm or operation that takes constant time will remain `constant` as the size of the input grows. For space complexity, many algorithms will require at least one iteration over an enumerable object, making overall O(1) space rare, but there are some hip algorithms that *don't* take up space based on the input--like sorting in place with [bubble sort](https://en.wikipedia.org/wiki/Bubble_sort) or [insertion sort](https://en.wikipedia.org/wiki/Insertion_sort) (this doesn't make them more efficient in all cases, though).

Let's think of a real world example. If you were to check your phone for the number of the most recent incoming caller, it wouldn't matter if would take the same amount of time whether your call log contained 200 calls or 2000. The most recent should be at the top, resembling a common data structure known as a stack.   

### Common examples of O(1) time complexity:

- Pushing/popping an element at the end of an array
- Looking up an array element by index
- Getting the length of an array
- Setting the element at array[i] to some value
- Swapping the element at array[i] with array[j]
- Setting, getting, or removing a key, value pair to a hash, map, or set
- Inserting or deleting a node in a linked list (assuming you've already traversed to the node!)
- Arithmetic operations
- if/else statements

## Linear: O(n)

If I were ordering things by complexity, O(log n) would follow O(1), but O(n) is much more common. So, we'll talk about it first.

Let's get space out of the way. Every common data structure takes up O(n) space by existing. The space taken increases linearly with the size of the data. This doesn't mean that every algorithm needs O(n) space at a minimum, but it does mean that if you iterate over the data structure, you require O(n) space.

Plenty of real world tasks take O(n) time. Consider the task `cancel unwanted subscription services`. The amount of time it takes increases linearly with the amount of services you are subscribed to. Trust me, even the [best financial app that allows you to manage your spending with just a tap]() still requires you to go through one service a time, even if it is incredibly fast and easy. #sponsored #ad

### Common examples of O(n) time complexity:

- Adding an element to the beginning of an array
- Removing an element from the beginning of an array
- Removing or replacing elements *anywhere other than the end of an array*
- A loop that traverses from array[0] to array[n]
- Built-in array methods that involve iterating over every element, like reversing of filtering, or calling `indexOf(element)`
- Traversing a linked list

## Logarithmic: O(log n)

O(log n), not to be confused with O(nlog n) is logarithmic complexity. Thinking of logarithmic time or space as fitting somewhere between constant and linear is actually not a bad approach (in my opinion)--because getting to an answer logarithmically means eliminating part of the input as you go.

Let me try to explain that better. There's a classic example using a phone book, but I haven't seen one of those in a decade.

Let's say there's a stack of `alphabetized` envelopes containing wedding invitations on the table. Your spouse-to-be has just informed you that `John Malkovich` changed his address, and you'll need to swap his envelope with a new one. It wouldn't be very efficient to start at the beginning of the stack or the end of the stack, becauase M is somewhere in the middle, and you've invited 12,000 people to your wedding.

Intuitively, you may have already thought to go to the middle or another random spot. If the envelope you found reads `Fumio Kishida`, it may not be the right one, but this means that you *no longer need to search the half of the stack that comes before Fumio Kishida*. The envelopes are already sorted, meaning there is no way for Malkovich to be in the A-K envelopes.

A data structure that requires its elements be sorted in some way is a `Binary Search Tree`, and the nature of a BST means that access, search, insertion, and deletion take O(log n) time and space.
### Common examples of O(log n) time complexity

- Accessing, searching, inserting, or deleting values in a Binary Search Tree
- Quick Sort, a sorting algorithm that uses a `divide-and-conquer` approach
## Linearithmic: O(nlog n)

Linearithmic can be thought of as a combination of linear and logarithmic. It's a [portmanteau](http://www.catb.org/jargon/html/L/linearithmic.html) of the two words, isn't that nice?

We used an example of alphabetized wedding invitations when talking about logarithmic time. Let's now imagine a scenario where you've finally found John Malkovich's wedding invite, but in doing so toppled the 12,000 envelopes.

You want an efficient way of putting everything back. Maybe you make 26 stacks, one for each letter of the alphabet, and you put each envelope into one stack. Once you sort each individual stack, you just need to merge them! This is pretty efficient. You did need to look at each envelope to determine what pile it belongs to, but once you have divided your task into sub tasks, the input each sub task is using is going to be smaller than `n`. This is a common theme with complex sorting algorithms!

### Common examples of O(nlog n) time complexity

- Merge Sort, a sorting algorithm that uses a divide-and-conquer approach and combines elements in a linear manner
- Heap Sort, a sorting algorithm that utilizes a heap data structure
- Tim Sort, a hybrid sorting algorithm that combines Insertion Sort and Merge Sort for efficient sorting of large data sets.

## Quadratic: O(n<sup>2</sup>)

Quadratic space and time complexity often lies at the end brute force implementations. That is to say, many problems that may be solved with an approach that requires quadratically scaling time (and less commonly, space) may *also* be solved in a more efficient way.

Many operations themselves don't take quadratic time to perform, so the best sign that your code requires quadratic time is `nested loops`.

Let's go back to the modestly-sized wedding example. You're future spouse has actually broken up with you, but you're still financially on the hook for the ceremony for 12,000 guests. In order to stave off financial ruin, you're doing the wedding photography yourself.

Your task is to photograph all of your guests in unique pairs, meaning every guest has to be photographed individually with every other guest, plus one with the newlywed couple. This is 12,000<sup>2</sup> photos, or 144,000,000. At a speed of 1 photo per second (the guests are lining up to get this over with "quickly") you'll be there for a little over 4.5 years with no breaks. There's no way of doing this more efficiently without changing the nature of the task.

Once you're done taking the photos, you've been asked to confirm if any two guests are wearing the same outfits so you can call them back for a reshoot. Fortunately, you've have 144,000,000 photos to comb through, so it should be easy, shouldn't it? Well, you *could* perform 144,000,000 checks. But you could also get it done in 12,000. You would just need something to store information about each `outfit` related to each guest.

For the sake of making this an easy algorithm, let's assume there is only **one** pair of people who wore the exact same outfit.

Let's say you have the photos separated into folders for each of the 12,000 guests. You could start by looking at the first guest and hashing their outfit and their folder name. For each subsequent guest, perform a hash lookup--which takes O(1) time. If you haven't seen their outfit (meaning no guest you've looked at has worn the same thing) then add their info to the hash. Keep going until someone's outfit is *already in the hash map*. When you find them, your hash map should have the folder of the individual in the matching outfit! In the worst case, the first and last folder contain matching individuals, meaning you need to perform 12,000 operations. But, in a best case, you will do fewer. The worst case of 12,000 is *significantly lower* than the worst case of 144,000,000.

This algorithm is, of course, blurring lines between human tasks and computer tasks, but hopefully it demonstrates the point. If this optimization seems familiar, it is basically the same as [Two Sum](https://leetcode.com/problems/two-sum/).

## Exponential: O(2<sup>n</sup>) & Factorial: O(n!)

These are rare, but not nonexistent. I'll opt to provide ChatGPT's examples rather than my own:

```
An example of an operation that takes factorial time is the generation of all permutations of a given set of items. This can be done using the recursive algorithm called Heap's Algorithm, which generates all possible permutations of a set by swapping elements. The time complexity of this algorithm is O(n!), because for a set of n items there are n! possible permutations.

An example of an operation that takes exponential time is the generation of all subsets of a given set of items. This can be done using the recursive algorithm called the power set, which generates all possible subsets of a set by including or excluding each element. The time complexity of this algorithm is O(2^n), because for a set of n items there are 2^n possible subsets.

Another example of an operation that takes exponential time is the traveling salesman problem, which is the problem of finding the shortest possible route that visits a given set of cities and returns to the starting city. The time complexity of the brute force algorithm for solving this problem is O(n!) because for each city you have to check all the possible routes.
```

&nbsp;

Need more Big O? **Here's an [exhaustive list](https://en.wikipedia.org/wiki/Time_complexity#Table_of_common_time_complexities) that can be ordered by running time.**

&nbsp;

## [Simplifying Big O](https://medium.com/swlh/simplifying-big-o-expressions-4f7c6059d3d5)

When you're talking about an algorithm's Big O requirements, you will ultimately simplify or boil down the answer by removing constants and small terms.

O(4n<sup>2</sup>) and O(n<sup>2</sup>) are both represented as O(n<sup>2</sup>).
O(500) is simplified to O(1). O(2n) is treated like O(n)

O(4n<sup>2</sup> + 2n + 500) is simplified to O(n<sup>2</sup>).

Simplification allows you to describe the complexity that best matches your algorithim, even if you extract some constants or small terms. You may still be asked to identify the operations that contribute to the time complexity, but if you're trying to optimize for O(n) and your solution is O(3n), that's still *far* from O(n<sup>2</sup>).

&nbsp;

## Representing Big O with multiple variables

We'll see algorithms that might have a time complexity of O(m * n) or a space complexity of O(n + k), where the additional variables represent different inputs, or different data structures used for the algorithm. It's important to understand when this applies, but we'll cover that when we see an example.

&nbsp;

Up next: data structures and example algorithms
<!-- 
## [Data Structures](https://en.wikipedia.org/wiki/Data_structure)

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
## [Binary Tree Postorder Traversal](https://leetcode.com/problems/binary-tree-postorder-traversal/) -->