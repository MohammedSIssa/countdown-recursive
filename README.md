#  Recursion Explained:

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

##  base case is reached! `(n < 1)`. Time to unwind and continue with the next line `A.unshift(n)`

### The unwinding process takes each instance made and executes newest instance to oldest instance:

```
countdown(0) returns []

countdown(1) -> A.unshift(1) -> return [1]

countdown(2) -> A.unshift(2) -> return [2,1]

countdown(3) -> A.unshift(3) -> return [3,2,1]

countdown(4) -> A.unshift(4) -> return [4,3,2,1]

countdown(5) -> A.unshift(5) -> return [5,4,3,2,1]
```

### This can get very complicated. But it's necessary to understand the "unwinding" process.

#### Hope this helped!
