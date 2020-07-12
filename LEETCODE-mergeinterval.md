##Merge Intervals
https://leetcode.com/problems/merge-intervals/
```python
def merge(self, intervals):
    i=1
    intervals.sort()
    while i < len(intervals) :
        if intervals[i][0] <= intervals[i-1][1]:
            intervals[i-1] = [intervals[i-1][0], max(intervals[i][1], intervals[i-1][1])]
            intervals.pop(i)
        else:
            i += 1
    return intervals
```        
