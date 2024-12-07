---
id: structs
title: Structs
slug: /structs
---

# Structs in Go

In Go, you can create your own data structures by using **structs**. A struct is a data type that groups together fields, or variables, under a single name for the struct. This allows you to model real-world objects using structs.

## Defining a Struct

A struct is defined using the `type` keyword followed by the struct name and its fields.

### Example

```go
package main

import "fmt"

type Person struct {
	Name string
	Age int
}

func main() {
	p := Person(Name: "Caiden", age: 19)
	fmt.Println(p)
}
```

## Accessing Structs

Fields of a struct can be accessed using the dot (`.`) operator.

### Example

```go
package main

import "fmt"

type Person struct {
	Name string
	Age int
}

func main() {
	p := Person(Name: "Caiden", age: 19)

	fmt.Println("Name:", p.Name)
	fmt.Println("Age:", p.Age)
}
```

## Methods on Structs

Methods can be defined on structs to associate behaviors with the data in the fields.

### Example

```go
package main

import "fmt"

type Rectangle struct {
	Width float32
	Height float32
}

func (r Rectangle) Area() float32 {
	return r.Width * r.Height
}

func (r *Rectangle) Resize(newWidth, newHeight float32) {
	r.Width = newWidth
	r.Height = newHeight
}

func main() {
	rect := Rectangle(Width: 10, Height: 10)
	fmt.Println("Area:", rect.Area())

	rect.Resize(20, 10)
	fmt.Println("Updated Area:", rect.Area())
}
```

## Constructors

Go does not have constructors in the way that other programming languages do, but factories can be created to initialize structs.

### Example

```go
package main

import "fmt"

type Person struct {
	Name string
	Age int
}

func newPerson(name string, age int) Person {
	return Person(Name: name, Age: age)
}

func main() {
	p := NewPerson("Caiden", 19)
	fmt.Println(p)
}
```

## Copying Structs

When you assign a struct to another variable, only a copy is created. Modifications to one of the variables will not affect the other.

### Example

```go
package main

import "fmt"

type Person struct {
	Name string
	Age int
}

func main() {
	p1 := Person(Name: "Caiden", age: 19)
	p2 := p1

	p2.Name = "John"
	fmt.Println("p1:", p1)
	fmt.Println("p2:", p2)
}
```

As a side note, when using structs as a function parameter, you can pass them by reference using pointers where modifying one will affect the other, like such:

```go
func UpdateName(p *Person, newName string) {
	p.Name = newName
}

func main() {
	person := Person(Name: "Caiden", Age: 19)
	UpdateName(&person, "John")
	fmt.Println(person.Name)
}
```

## Conclusion

Structs can be used in Go to organize many primitive types into one composite type. This type can often be used to model real-world entities in a way that makes the code more readable and easier to program with methods for behaviors and factorys for initialization.
