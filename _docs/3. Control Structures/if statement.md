---
title: If statement
category: Control Structures
order: 1

---
 The 'If' statement is a very useful conditional and does not need two backets `()` like in PHP and in some languages. It's defined in one line in go.

 ```go
 if condition {
     doSomething()
 }
 ```
Let's examine an example.
```go
package main

import (
	"fmt"
)

func main() {
	counter := 2
	if counter == 2 {
		fmt.Printf("%d is equal to counter", counter)
	}
}
```
In the example above, our conditional is `counter == 2` which is defined in one line.
If you notice we do not need tripple `=` sign for the condition like in Javascript. 

We'll add one more condition to our example above.

```go
....

func main() {
	counter := 2
	if counter == 2 {
		fmt.Printf("%d is equal to counter", counter)
	} else if counter == 3 {
		fmt.Printf("%d is equal to counter", counter)
	} else {
		fmt.Printf("Counter is neither equal to 2 nor 3")
	}
```
We added another one more condition and a default condition when `counter` does not equate 2 or 3.
`else if` statement must be defined on the same with the closing parathensis `}`.

You can also have variable defined in the same line with the condition 