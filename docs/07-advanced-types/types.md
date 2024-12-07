---
id: types
title: Types
slug: /types
---

# Types in Go

The `type` keyword in Go allows you to define user-defined types.

## Type Aliases

A type alias lets you create another name for an existing type. Aliases are used for increasing readability or forcing compatibility with an external library that uses another name for a type.

### Syntax:

```go
type AliasName = ExistingType
```

### Example:

```go
package main

import "fmt"

type MyString = string

func main() {
	var name MyString = "Caiden"
	fmt.Println(name)
}
```

In this case, `MyString` is 100% interchangeable with `string`.

## New Types

A new type creates a type based on another one. Unlike type aliases, this creates a new type with its completely own identity, it just shares the same underlying structure as the original type.

### Syntax:

```go
type NewType ExistingType
```

### Example:

```go
package main

import "fmt"

Type Celsius float32
Type Fahrenheit float32

func main() {
	var temp1 Celsius = 50.0
	var temp2 Fahrenheit = 51.0

	temp1 = Celsius(temp2)
	fmt.Println(temp1)
}
```

If you remember, we saw this example back in the section about type strength.

