## Subarray Sum Equals K

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
