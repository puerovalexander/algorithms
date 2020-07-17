## Two Sum

https://leetcode.com/problems/two-sum/

```python
def twoSum(self, nums, target):
    nums = [elem for elem in enumerate(nums)]
    nums.sort
    first = 0
    last = len(nums) - 1
    while first != last:
        if nums[first][1] + nums[last][1] == target:
            return [nums[first][0], nums[last][0]]
        elif nums[first][1] + nums[last][1] < target:
            first = first + 1
        else:
            last = last - 1
```
