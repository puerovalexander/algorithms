##Subarray Sum Equals K
https://leetcode.com/problems/subarray-sum-equals-k/
```python
def subarraySum(self, nums, k):   
    hash = {0: 1}
    index = 0
    count = 0
    for elem in nums:
        index = index + elem
        diff = index - k
        if diff in hash:
            count += hash[diff]
        hash[index] = hash.setdefault(index, 0) + 1
    return count
```        
