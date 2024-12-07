---
id: loops
title: Loops
slug: /loops
---

# Loops in Go

Loops are used to execute a block of code repeatedly. Unlike most languages, Go only has a single looping construct, `for`, however functionality of other looping constructs can still be achieved.

## For Loops

The `for` keyword can be used for traditional for looping, which works as such:
- The first statement, `i := 0`, initializes the starting value.
- The second statement, `i < 10`, is the condition and is when the loop stops.
- The third statement, `i++`, is the step and controls what happens after every loop.

### Example

```go
package main

import "fmt"

func main() {
	for i := 0; i < 10; i++ {
		fmt.Println(i)
	}
}
```

## While-loop Functionality

A `for` loop without an initialization statement and step statement acts like a `while` loop would in most programming languages.

### Example

```go
package main

import "fmt"

func main() {
	x := 0
	for x < 10 {
		fmt.Println(x)
		x++
	}
}
```

## Infinite Loop

A `for` loop without any condition will execute forever and is thus an infinite loop.

### Example

```go
package main

import "fmt"

func main() {
	for {
		fmt.Println("infinite loop")
	}
}
```

## Range Loop

The `range` keyword can be used to iterate over collections such as slices, arrays, or maps.

### Example

```go
package main

import "fmt"

func main() {
	name := []int{1, 2, 3, 4, 5}
	for index, value := range nums {
		fmt.Printf("index: %d, value: %d\n", index, value)
	}
}
```

## Break, Continue Statements

The `break` statement allows exit out of a loop prematurely. The `continue` statement allows skipping an iteration of the loop.

### Example

```go
package main

import "fmt"

func main() {
	for i := 0; i < 10; i++ {
		if i == 0 {
			continue
		} else if i == 5 {
			break
		}

		fmt.Println(i)
	}
}
```

## Conclusion

Loops are another type of control structure that allows repeating the execution of code inside of a block for a certain condition. Once the condition is met, the execution will stop.
