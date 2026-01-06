# 1. Two Sum

## Intuition
We need two numbers whose sum equals the target.

## Approach
Use a hash map to store seen numbers and indices.

## Complexity
Time: O(n) ,
Space: O(n)

## Code
```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
         h = {}
         for i in range(len(nums)):
             h[nums[i]] = i

         for i in range(len(nums)):
             y = target - nums[i]

             if y in h and h[y] != i:
                 return [i, h[y]] 
