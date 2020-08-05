

## function overloading:
Python doesn't support function overloading.  
When we define multiple functions with the same name, the later one always overrides the prior and thus, in the namespace, there will always be a single entry against each function name.


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

## sorting:
### sort array of pairs
```
arr.sort(key=lambda x: (x[0], x[1]))
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
 
