---
id: type-checking
title: Type Checking
slug: /type-checking
---

# Type Checking in Go

Type checking in programming languages is a way to make sure that the type declaration of variables align with the way they are being used. Go is a statically typed language, similar to the likes of C++ and Java, type checking occurs at compile time.

## **Static Type Checking** in Go

In Go, types are checked during compilation. This means that if a variable is declared as one type and being used as another, the program will error during compile time, not runtime. This drastically reduces the number of runtime errors.

### Example

```go
package main

import "fmt"

func main() {
	var my_int int = 10
	var my_string string = "hello"

	// The next line will cause a compile-time error.
	my_int = my_string

	fmt.Println(my_int, my_string)
}
```

The preceding example would fail because we are trying to assign `my_string` (a string) to `my_int` (an int), which does not make semantic sense and thus errors. As can be seen, this error happens during compile time and not runtime.

## **How To Get Around Static Checking**

Even though Go is statically typed, most modern languages allow a way for dynamic typing to occur through a subset of features. Go is no different with their provided behavior through interfaces. In Go, interfaces aree a type that allow values to have a runtime-determined type, as long as the required methods are implemented in both the type and the interface.

### Example

```go
package main

import "fmt"

func print_value(val interface{}) {
	fmt.Printf("value: %v, type: %T", val, val)
}

func main() {
	print_value(10)
	print_value("hello")
	// value: 10, type: int
	// value: hello, type: string
}
```

In the preceding example, interface{} is a type that can hold any value as well as the actual type used.

## **Type Assertions**

Go provides a way to determine the type witheld of an interface value. This is the part that makes interfaces actually useful as we can check the type before doing operations.

### Example

```go
package main

import "fmt"

func main() {
	var my_interface interface{} = "hello"

	str, ok := my_interface.(string) // We are asserting that my_interface is type string
	if ok {
		fmt.Println("my_interface is a string")
	} else {
		fmt.Println("my_interface is not a string")
	}
}
```

## Conclusion

Go's static type system is a very common system these days and helps ensure safety of programs. It's interface dynamic typing allows flexibility whenever deviations from the static type system are needed.
