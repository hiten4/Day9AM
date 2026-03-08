# Part D — AI-Augmented Task

## 1. Prompt Used

Write a Python function that finds all pairs in a list that sum to a target number using list comprehensions.

---

## 2. AI Generated Code

```python
def pair_sum(nums, target):
    return [(a, b) for a in nums for b in nums if a + b == target]
3. Testing the Code
print(pair_sum([1,2,3,4,5], 6))
print(pair_sum([1,1,1], 2))
Output
[(1,5), (2,4), (3,3), (4,2), (5,1)]
[(1,1), (1,1), (1,1), (1,1), (1,1), (1,1)]
4. Issues in the AI Code
Duplicate Pairs

Pairs appear twice in reversed order.

Example:

(1,5) and (5,1)
(2,4) and (4,2)

Both represent the same pair but are counted separately.

Self Pair Problem

The pair (3,3) appears even though the list contains only one 3.

This happens because the code checks every element against every other element without considering index positions.

Too Many Results with Duplicates

For input [1,1,1], the function returns six identical pairs because each element is compared with all other elements.

Inefficient Logic

The algorithm checks every possible pair.

Time complexity:

O(n²)

This becomes inefficient for large lists.

5. Improved Version
def pair_sum(nums, target):
    pairs = set()
    seen = set()

    for num in nums:
        complement = target - num

        if complement in seen:
            pair = tuple(sorted((num, complement)))
            pairs.add(pair)

        seen.add(num)

    return list(pairs)
6. Testing the Improved Version
print(pair_sum([1,2,3,4,5], 6))
print(pair_sum([1,1,1], 2))
Output
[(1,5), (2,4)]
[(1,1)]
7. Improvements Made
Duplicate Pair Removal

Pairs are stored in a set.
Since sets do not allow duplicate elements, repeated pairs are automatically removed.

Order Normalization

The pair is sorted before storing.

Example:

(5,1) becomes (1,5)

This ensures (1,5) and (5,1) are treated as the same pair.

Correct Handling of Duplicates

Using a seen set ensures that duplicates in the list are handled correctly without producing excessive repeated pairs.

Example:

[1,1,1] with target 2

Correct output:

[(1,1)]
Better Time Complexity

The improved algorithm runs in:

O(n)

because each number is processed once while checking membership in a set.

8. Summary

The AI-generated code works but produces duplicate pairs and unnecessary comparisons.
The improved version removes duplicates, correctly handles repeated numbers, and improves efficiency from O(n²) to O(n) using sets.
