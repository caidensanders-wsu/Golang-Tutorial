---
id: variables-and-assignments
title: Variables & Assignments
slug: /variables-and-assignments
---

# Variables and Assignment in Go

Variables are used to store data that will be used throughout the runtime of a program. We will go into the exact typing mechanisms of variables in a later chapter, all we need to know for now is that they are statically typed and type has to be known at compile time.

## Declaring Variables

There are two popular ways to declare variables in Go:

- Using the `var` keyword.
- Using the `:=` operator.

I'll give an example of both.

The `var` keyword explicitly defines a variable. You can add an initial value if you want.

### Example (`var` keyword)

```go
var name string = "Caiden" // Explicit type, initial value
var age int                // Explicit type, default value
var score = 100            // Type inferred, initial value
```

The shorthand `:=` syntax declares and initializes variables simulaneously. Type is inferred.

### Example (`:=` operator)

```go
name := "Caiden" // Go can tell from "Caiden" that type is string
age := 19        // Go can tell from 19 that type is int
```

## Default Values

If a variable is declared without an initial value, it gets a default value based on its type:

- `int`: `0`
- `float`: `0.0`
- `bool`: `false`
- `string`: `""`

## Multiple Declarations

Multiple variables can be declared at once in Go.

### Example

```go
var x, y int = 1, 2
a, b := "Caiden"
```

## Constants

Constants are immutable meaning that they can not be changed after declared with the `const` keyword. They must be initialized at the time that they are declared.

### Example

```go
const PI = 3.14159
const name = "Caiden"
```

## Variable Scope

Variables can have two different scopes:

- Local Scope: Declared inside a function, cannot be accessed outside of it.
- Global Scope: Declared outside any function at all, accessible all throughout package.

### Example

```go
var global_variable = "I am global" // Global scope

func main() {
	local_variable = "I am local" // Local scope
	fmt.Println(global_variable, local_variable)
}
```

## Conclusion

Variables in Go can be declared using either `var` or `:=`. If not initialized, they get default values. Constants are immutable, cannot be changed, and are declared with `const`. Be mindful of what scope you define variables in.
