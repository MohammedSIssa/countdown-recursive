# countdown-recursive

##  Recursion Explained:

##### The example here is written in `JavaScript`

```
function countdown(n){
	if (n < 1){
	return []
	}
else{
	const A = countdown(n - 1)
	A.unshift(n)
	return A
	}
}
```

#### `countdown(5)` Outputs `[5,4,3,2,1]`

##### The recursion process:

```
n = 5
new instance: countdown(4)

n = 4
new instance: countdown(3)

n = 3
new instance: countdown(2)

n = 2
new instance: countdown(1)

n = 1 
new instance: countdown(0)

n = 0
return []
```

####  base case is reached! `(n < 1)`. Time to unwind and continue with the next line `A.unshift(n)`

##### The unwind process takes each instance made and executes newest instance to oldest instance:

```
countdown(0) returns []

countdown(1) returns A.unshift(1) -> [1]

countdown(2) returns A.unshift(2) -> [2,1]

countdown(3) returns A.unshift(3) -> [3,2,1]

countdown(4) returns A.unshift(4) -> [4,3,2,1]

countdown(5) returns A.unshift(5) -> [5,4,3,2,1]
```
