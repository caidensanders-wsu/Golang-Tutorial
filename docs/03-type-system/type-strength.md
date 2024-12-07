---
id: type-strength
title: Type Strength
slug: /type-strength
---

# Type Strength in Go

Type strength is another name for how strictly a programming language enforces their type rules. Go is largely considered to be a strongly typed language because Go enforces type safety and doesn't allow implicit type conversions between two unrelated types.

## **Type Safety** in Go

Go requires explicit type conversion if we are operating with any values of different types. Implicit conversions are not allowed. Type safety helps ensure there's no unintended behavior.

### Example

```go
package main

import "fmt"

func main() {
	var diameter int = 10
	var circle_pi float32 = 3.14

	// The following line would result in a compile-time error.
	// circumference := diameter * circle_pi

	// Instead, we must use an explicit type conversion.
	circumference := float32(diameter) * circle_pi

	fmt.Println("The circumference is:", circumference)
}
```

Here, `diameter` (an int) cannot be multipled by `circle_pi` (a float32) without first converting both operands to an integer or to a float.

## **Strict Typing**

Go enforces strict type checking in functions and variables. A function's parameters must match their types given in the parameters and a function's return type must match their type given in the function declaration.

### Example

```go
package main

import "fmt"

func add(a int, b int) int {
	return a + b
}

func main() {
	fmt.Println(add(10, 10)) // No errors
	// fmt.Println(add(10, 20.5)) would cause a compile-time error
}
```

It is perfectly fine to pass an int to a parameter of `add` that is declared with type int. However, if we try to pass adifferent type such as a float, there will be a compile-time error.

## **Type Aliases** in Strong Typing

Even if two user-defined types, which we will get into later in the course, have the same representation beneath, Go will treat them as different types unless we convert them to the same type.

### Example

```go
package main

import "fmt"

type Celsius float32
type Fahrenheit float32

func main() {
	var temp1 Celsius = 50.0
	var temp2 Fahrenheit = 51.0

	// The following would result in a compile-time error.	
	temp1 = temp2

	// Instead, we must use an explicit conversion.
	temp1 = Celsius(temp2)

	fmt.Pritnln("Celsius Temperature:", temp1)
}
```

## Conclusion

Go uses a strong typing system to reduce errors and unintended behaviors. Go does this by forcing explicit conversions and strict typing. This helps create safer code.
