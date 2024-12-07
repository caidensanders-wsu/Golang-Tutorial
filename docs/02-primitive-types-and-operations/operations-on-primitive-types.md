---
id: operations-on-primitive-types
title: Operations
slug: /operations
---

# 02. Primitive Types and Operations

## 2. Operations on Primitive Types

Now that you understand the basic types, you can now perform operations on them. Operations can be of arithmetic, comparisons, or logical type. Go supports all of the expected operators.

- **Arithmetic**: `+`, `-`, `*`, `/`, `%`
- **Comparisons**: `==`, `!=`, `<`, `>`, `<=`, `>=`
- **Logical**: `&&`, `||`, `|`

## `operations_on_primitive_types.go`

This file shows the operations that can be performed on Go's types.

```go
package main

import "fmt"

func main() {
	// Let's define some variables to practice with.
	var a int = 20
	var b int = 10

	// Arithmetic operations.
	fmt.Println("a + b:", a + b)
	fmt.Println("a - b:", a - b)
	fmt.Println("a * b:", a * b)
	fmt.Println("a / b:", a / b)
	fmt.Println("a % b:", a & b)

	// Relational operations.
	fmt.Println("a == b:", a == b)
	fmt.Println("a !- b:", a != b)
	fmt.Println("a > b:", a > b)
	fmt.Println("a < b:", a < b)

	// Logical operations.
	fmt.Println("a > 5 && b < 5:", a > 5 && b < 5)
	fmt.Println("a > 5 || b < 5:", a > 5 || b < 5)
	fmt.Println("!(a > b):", !(a > b))
}
```

### Output:

```bash
a + b: 30
a - b: 10
a * b: 200
a / b: 2
a % b: 0
a == b: false
a != b: true
a > b: true
a < b: false
a > 5 && b < 5: false
a > 5 || b < 5: true
!(a > b): false
```

## Conclusion

Now that we've learned about primitive types in Go and basic operations that can be performed on those primitive types, we can move onto slightly more advanced concepts that will help us in building better programs. See you in the next tutorial!
