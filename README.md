# Can Place Flowers Problem

 Programming Problem

## Problem Statement

You have a long flowerbed in which some of the plots are planted, and some are not. However, flowers cannot be planted in **adjacent** plots.

Given an integer array `flowerbed` containing `0`'s and `1`'s, where `0` means empty and `1` means not empty, and an integer `n`, return *if* `n` new flowers can be planted in the `flowerbed` without violating the no-adjacent-flowers rule.

**Example 1:**

**Input:** flowerbed = [1,0,0,0,1], n = 1
**Output:** true

**Example 2:**

**Input:** flowerbed = [1,0,0,0,1], n = 2
**Output:** false

**Constraints:**

- `1 <= flowerbed.length <= 2 * 104`
- `flowerbed[i]` is `0` or `1`.
- There are no two adjacent flowers in `flowerbed`.
- `0 <= n <= flowerbed.length`

## Explanation & Solution

The solution is very simple. We can find out the extra maximum number of flowers, ```count```, that can be planted for the given ```flowerbed``` arrangement. To do so, we can traverse over all the elements of the ```flowerbed``` and find out those elements which are 0(implying an empty position). For every such element, we check if its both adjacent positions are also empty. If so, we can plant a flower at the current position without violating the no-adjacent-flowers-rule. For the first and last elements, we need not check the previous and the next adjacent positions respectively.

If the ```count``` obtained is greater than or equal to ```n```, the required number of flowers to be planted, we can plant nnn flowers in the empty spaces, otherwise not.
