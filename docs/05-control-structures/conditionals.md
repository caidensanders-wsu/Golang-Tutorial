---
id: conditionals
title: Conditionals
slug: /conditionals
---

# Conditionals in Go

Conditionals are used in Go to structure and execute code based on the results of certain conditions. The main forms of conditionals in Go are `if`, `else if`, `else`, and `switch`.

## If Statement

The `if` statement executes the block of code contained within it if the condition evaluates to true.

### Example

```go
package main

import "fmt"

func main() {
	x := 10
	if x == 10 {
		fmt.Println("x is equal to 10")
	}
}
```

## If-Else Statement

The `if` block also supports an `else` block after it that will execute code if the condition does not evaluate to true, or in other words, it evaluates to `false`.

### Example

```go
package main

import "fmt"

func main() {
	x := 10
	if x == 11 {
		fmt.Println("x is equal to 11")
	} else {
		fmt.Println("x is not equal to 11")
	}
}
```

## Else If Statement

The `else if` block can be used after an if to check multiple conditions.

### Example

```go
package main

import "fmt"

func main() {
	x := 0
	if x > 0 {
		fmt.Println("x is positive")
	} else if x < 0 {
		fmt.Println("x is negative")
	} else {
		fmt.Println("x is zero")
	}
}
```

## Switch Statement

The `switch` statement in Go is a way to handle multiple conditions in a cleaner form than using multiple `else if` blocks. Unlike similar languages, Go's `switch` does not require `break` conditions after every case.

### Example

```go
package main

import "fmt"

func main() {
	x := 0

	switch x {
	case x > 0:
		fmt.Println("x is positive")
	case x < 0:
		fmt.Println("x is negative")
	case x == 0:
		fmt.Println("x is zero")
	default:
		// Executed if none of the above evaluate to true (else).
		fmt.Println("x is complex")
	}
}
```

### Fallthrough

Go terminates the switch statement after it executes a block that evluated to true. However, the `fallthrough` keyword can be used to allow execution to continue through other blocks after a block was executed.

### Example

```go
package main

import "fmt"

func main() {
	x := 10

	switch x {
	case x > 0:
		fmt.Println("x is positive")
		fallthrough
	case x > 1:
		fmt.Println("x is greater than one")
	default:
		fmt.Println("x is negative")
}	
```


## Conclusion

Control structures can be used in Go to execute code based on the evaluation of a value or an operation on values. This can help structure code for maintainability and readability.
