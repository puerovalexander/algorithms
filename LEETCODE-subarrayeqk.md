## Subarray Sum Equals K

https://leetcode.com/problems/subarray-sum-equals-k/

```python
def subarraySum(self, nums, k):   
    sum_dict = {0: 1}
    index = 0
    count = 0
    for elem in nums:
        index = index + elem
        diff = index - k
        if diff in sum_dict:
            count += sum_dict[diff]
        sum_dict[index] = sum_dict.setdefault(index, 0) + 1
    return count
```        
