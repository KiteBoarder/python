## Q: What does `yield` do in Python?

`yield` pauses a function, returns a value, and resumes execution from the same
point on the next call. A function that uses `yield` becomes a **generator**.

### Example

```python
def numbers():
    yield 1
    yield 2
    yield 3

gen = numbers()

next(gen)  # 1
next(gen)  # 2
next(gen)  # 3
```
return vs yield
```
# return
def f():
    return 1
    return 2  # never executed

# yield
def g():
    yield 1
    yield 2
```
---

## function overloading:

# Python doesn't support function overloading.  
When we define multiple functions with the same name, the later one always overrides the prior and thus, in the namespace, there will always be a single entry against each function name.
---

## for loop: 

### for loop with index, number 
```
for i, number in enumerate(numbers):
    print(i * 2, number)
    
```
### for loop on pairs:
```
 [(a, 1) for (a,b) in intervals] + [(b, -1) for (a,b) in intervals]   
```

### for loop string: 
```
for c in "string":
    #do something with c
```

### for loop two arrays simultaneously: 
```
for f, b in zip(foo, bar):
    print(f, b)
```
zip stops when the shorter of foo or bar stops.

---
## sorting:
### sort array of pairs
```
arr.sort(key=lambda x: (x[0], x[1]))
```

### min function with lambda: 
```
    closest = min(closest, node.val, key = lambda x: abs(x - target))
```


## for loop reversed:
```
for i in reversed(range(101)):
    print(i) # prints 100 to 0 

# another way. note: the first parameter is always inclusive, the second always exclusive:    
for i in range(100,-1,-1):
    print(i) # prints 100 to 0
```

## return statement one line:
```
return min(arr) if arr else 0
```
Notes: empty arr [] is false.  
min returns the min of an array too. 

## array initialization
```
 arr = [ [0]*3 for i in range(3)]
 
 d3 = [[[0 for col in range(4)]for row in range(4)] for x in range(6)]
``` 
 
 ## nested function
 ### nonlocal variable
 In python 3.x:
 ```
 def f1():
        x = 5
        def f2():
                nonlocal x
                x+=1
        return f2
 ```


 ## Max Heap
 default heapq in python is min heap. 
```
import heapq

class MaxHeapObj(object):
  def __init__(self, val): self.val = val
  def __lt__(self, other): return self.val > other.val
```
Example of a max-heap:
```
maxh = []
heapq.heappush(maxh, MaxHeapObj(x))
x = maxh[0].val  # fetch max value
x = heapq.heappop(maxh).val  # pop max value
```
