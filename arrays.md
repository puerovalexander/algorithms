
https://leetcode.com/problems/subarray-sum-equals-k/

```python 
def subarraySum(self, nums, k):   
    sumdict = {0: 1}
    index = 0
    count = 0
    for elem in nums:
        index = index + elem
        diff = index - k
        if diff in sumdict:
            count += sumdict[diff]
        sumdict[index] = sumdict.setdefault(index, 0) + 1
    return count
```

## 3Sum

https://leetcode.com/problems/3sum/

```python
def threeSum(self, nums):        
    nums.sort()
    length = len(nums)
    result = set()
    for i in range(length-2):
        left = i + 1
        right = length-1
        while left < right:
            sum_value = nums[i] + nums[left] + nums[right]
            if sum_value == 0:
                result.add((nums[i], nums[left], nums[right]))
                left += 1
                right -= 1
            elif sum_value < 0:
                left += 1
            else:
                right -= 1
    return result
```

## Two sum

https://leetcode.com/problems/two-sum/
