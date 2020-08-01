# intervals

+[Non-overlapping Intervals](#non-overlapping-intervals)
+[Merge Intervals](#merge-intervals)
+[Insert Intervals](#insert-intervals)

## Non-overlapping Intervals

https://leetcode.com/problems/non-overlapping-intervals/

## Merge Intervals

https://leetcode.com/problems/merge-intervals/

## Insert Interval

https://leetcode.com/problems/insert-interval/

```python
def insert(self, intervals, newInterval):
    mid = [newInterval[0], newInterval[1]]
    left = []
    right = []
    for elem in intervals:
        if elem[1] < mid[0]:
            left.append(elem)
        elif elem[0] > mid[1]:
            right.append(elem)
        else:
            mid[0] = min(elem[0], mid[0])
            mid[1] = max(elem[1], mid[1])
    return left + [mid] + right
```

```python
def insert(self, intervals, newInterval):
    intervals.append(newInterval)        
    intervals.sort()        
    tmp = []
    for interval in intervals:
        if not tmp or tmp[-1][1] < interval[0]:
            tmp.append(interval)
        else:
            tmp[-1][1] = max(tmp[-1][1], interval[1])        
    return tmp
```    
