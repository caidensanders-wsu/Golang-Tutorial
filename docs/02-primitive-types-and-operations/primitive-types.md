---
id: primitive-types
title: Primitive Types
slug: /primitive-types
---

# 02. Primitive Types and Operations

In this section, we are going to explore the second concept in a template for learning a new programming language. This topic is primitive types and their operations. Go supports many types, with a strong and statically typed system. This means that in Go, you have to specify the type of each variable, unlike some languages like Python or JavaScript with a dynamic typing system.

## 1. Primitive Types in Go

Go supports several basic data types, these are:

- Integers: Used to represent whole numbers.
- Floating-point numbers: Used to represent numbers with decimal points.
- Booleans: Used to represent a `true` or `false` value.
- Strings: Used to represent a string of characters.

### `primitive_types.go`

This file shows you how to declare and access primitive types in Go.

```go
package main

import "fmt"

func main() {
	// Declare variables.
	var age int = 21
	var gravity float32 = 9.8
	var name string = "Caiden"
	var yummy bool = true	

	// Access the variables and print to screen.
	fmt.Println("Age:", age)
	fmt.Println("Gravity:", gravity)
	fmt.Println("Name:", name)
	fmt.Println("Yummy:", yummy)
}

### Output:

```bash
Age: 21
Gravity: 9.8
Name: Caiden
Yummy: true
```

### Things to keep in mind whilie programming in Go:

- Types must be explicitly declared.
- Go has two types of numbers, `int` for integers and `float32` or `float64` for floating-point numbers.
- Strings are immutable.

## Conclusion

Now that you know the basic, or primitive, data types in Go, you can go on and learn about how to operate on them. See you in the next lesson!
