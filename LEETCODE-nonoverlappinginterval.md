##Non-overlapping Intervals
https://leetcode.com/problems/non-overlapping-intervals/
```python
def eraseOverlapIntervals(self, intervals):       
    intervals.sort()
    i = 1
    caunt = 0
    while i < len(intervals):
        if intervals[i][0] < intervals[i-1][1]:
            intervals.pop(i)
            caunt += 1
        else:
            i += 1
    return caunt
```
