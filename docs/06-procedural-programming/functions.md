---
id: functions
title: Functions
slug: /functions
---

# Functions in Go

Functions are a fundamental part of programming languages that allow separation of logic into reusable, modular code blocks. In this section, we'll learn how to define and use functions in Go.

## Defining a Function

In Go, a function is defined using the `func` keyword with a function name, parameters, and a return type.

### Syntax

```go
func function_name(parameters) return_type {
	// Code block
}
```

### Example

```go
package main

import "fmt"

func greet(name string) string {
	return "Hello, " + name + "!"
}

func main() {
	message := greet("Caiden")
	fmt.Println(message)
}
```

## Function Parameters

Go functions can take single, multiple, or no parameters, with each parameter having a type.

### Example

```go
package main

import "fmt"

func add(a int, b int) int {
	return a + b
}

func main() {
	result := add(10, 10)
	fmt.Println("10 + 10 =", result)
}
```

### Side Note

Parameters of the same type can be grouped as such:

```go
func multiply(a, b int) int {
	return a + b
}
```

## Return Values

Go functions can return a single value or multiple values.

### Example (single return value)

```go
package main

import "fmt"

func square(x int) int {
	return x * x
}

func main() {
	ten_squared = square(10)
	fmt.Print("10^2 =", ten_squared)
}
```

### Example (multiple return values)

```go
package main

import "fmt"

func divide(dividend, divisor int) (int, int) {
	quotient := dividend / divisor
	remainder := dividend % divisor
	return quotient, remainder
}

func main() {
	q, r := divide(10, 3)
	fmt.Println("quotient:", q, "reainder:", r)
}
```

## Named Return Values

Go allows putting a name to a return value, making code cleaner, like such:

```go
func rectangle(length, width int) (area, perimeter int) {
	area = length * width
	perimeter = 2 * (length + width)
	return
}
```

## Variadic Functions

A variadic function is a function that takes a special type of parameter that accepts an arbitrary number of arguments. We can use `...` before the parameter type in order to create a variadic function.

### Example

```go
package main

import "fmt"

func sum(numbers ...int) int {
	total := 0
	for _, num := range numbers {
		total += num
	}
	return total
}

func main() {
	fmt.Println("Sum:", sum(1, 2, 3, 4, 5))
}
```

## Anonymous Functions

An anonymous function is a function without a name. Go allows sthe crewation of these and they are often used to declare a function to a variable, or to call it immediately.

### Example (inline anonymous function)

```go
package main

import "fmt"

func main() {
	result := func(a, b int) int {
		return a + b
	}(5, 7)
	
	fmt.Println("Result:", result)
}
```

### Example (assigning to variable)

```go
package main

import "fmt"

func main() {
	multiply := func(a, b int) int {
		return a + b
	}
	fmt.Println("10 * 10 =", multiply(10, 10))
}
```

## Higher-Order Functions

Functions in Go can take other functions in as parameters to the function or they can return them from the function.

### Example

```go
package main

import "fmt"

func Map(slice []int, fn func(int) int) []int {
	var result []int
	for _, v := range slice {
		result = append(result, fn(v))
	}
	return result
}

func main() {
	numbers := []int{1, 2, 3, 4, 5}

	double := func(x int) int {
		return x * 2
	}

	doubledNumbers := Map(numbers, double)
	fmt.Println("Original:", numbers)
	fmt.Println("Doubled:", doubledNumbers)
}
```

## Closures

Closures are one of the more advanced topics in procedural programming. Functions in Go can create closures that capture variables from their outer scope. Below is an example.

### Example

```go
package main

import "fmt"

func main() {
	increment := func() func() int {
		counter := 0
		return func() int {
			counter++
			return counter
		}
	}()

	fmt.Println(increment()) // 1
	fmt.Println(increment()) // 2
	fmt.Println(increment()) // 3
}
```

## Conclusion

Functions are a way of organizing code into separate units, or code blocks, and increase reusability as functions can be called multiple times. Functions in Go are treated as first-class citizens, they can be passed as arguments or returned from other functions.	
