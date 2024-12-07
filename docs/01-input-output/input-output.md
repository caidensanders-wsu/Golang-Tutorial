---
id: input-output
title: Input & Output
slug: /input-output
---

# IO (Input/Output) in Go

IO (Input Output) operations are critical for interacting with users or systems, as well as debugging. In Go, the `fmt` package, part of the standard library, provides functions for basic I/O operations.

## Printing Output

The `fmt` package provides several different functions to display output to the console. We will be working with `fmt.Print`, `fmt.Println` and `fmt.Printf` to print messages, the two most common functions of doing so.

### Example

```go
package main

import "fmt"

func main() {
	fmt.Print("We have to add our own newline.\n") // Prints a basic string with no newline.
	fmt.Println("Hello, World!") // Prints a basic string with a newline at the end.
	fmt.Printf("My name is %s and I am %d years old.\n", "Caiden", 19) // Prints formatted with variables.
}
```

## Reading Input

For reading user input, we will be working with `fmt.Scan`, `fmt.Scanln`, and `fmt.Scanf`.

### Example (reading single input)

```go
package main

import "fmt"

func main() {
	var name string
	fmt.Printf("What do you go by? ")
	fmt.Scan(&name)
	fmt.Println("Hello, ", name)
}
```

### Example (reading multiple inputs)

```go
package main

import "fmt"

func main() {
	var firstName, lastName string
	fmt.Print("Enter your first and last name: ")
	fmt.Scan(&firstName, &lastName)
	fmt.Printf("Hello, %s %s!\n", firstName, lastName)
}
```

### Eaxmple (reading a full line)

```go
package main

import "fmt"

func main() {
	var quote string
	fmt.Print("What's your favorite quote? ")
	fmt.Scanln(&quote)
	fmt.Println("Your favorite quote", quote)
}
```

### Example (formatted input)

The `fmt.Scanf` function inputs using format specifiers. That means, it will only read the input based on the format specifier provided.

```
package main

import "fmt"

func main() {
	var age int
	fmt.Print("Enter your age: ")
	fmt.Scanf("%d", &age)
	fmt.Printf("You are %d years old.\n", age)
}
```

## Conclusion

Go provides `fmt` for simple console I/O. With `fmt`, we can output to the console with functions such as `fmt.Print`, `fmt.Println`, `fmt.Printf`, and read from the console with `fmt.Scan`, `fmt.Scanln`, `fmt.Scanf`.
