---
id: arrays
title: Arrays
slug: /arrays
---

# Arrays in Go

An array is a fixed-size collection of elements. An array has order and all elements must be of the same type.

## Declaring and Initializing Arrays

Let's begin by declaring an array of five integers.

### Declaring an Array

```go
var arr [5]int
```

That wasn't too bad?

### Initializing an Arrray

Now this time when we declare the array let's initialize it also.

```go
arr := [5]int{10, 20, 30, 40, 50}
```

### Accessing and Changing Values

Now we have an array with five integers in it, let's verify.

```go
fmt.Println(arr[0])
```

You should get an output of 10. Now let's change that element to 25.

```go
arr[1] = 25
fmt.Println(arr[0])
```

You should get an output of 25.

## Iterating Over Arrays

There are two simple ways to iterative over an array, using for loops, or using range.

### Example (using `for` loop)

```go
for i := 0; i < len(arr); i++ {
	fmt.Println(arr[i])
}
```

### Example (using `range`)

```go
for index, value := range arr {
	fmt.Printf("index: %d, value: %d\n, index, value)
}
```

## Multidimensional Arrays

Multidimensional arrays are supported in Go and can be declared and accessed.

### Example

```go
var multidimensional [3][3]int
multidimensional[0][0] = 1
fmt.Println(multidimensional[0][0])
```

## Copying

Assigning a variable that holds an array to another variable in Go will just create a new array with copies of all elements in the original. Modifying one of the arrays will not change the other.

## Conclusion

Arrays are a common data structure in almost all programming languages, and as such, Go has them. However, they are rarely used due to Go having a data structure called `slice` that we will go into in the next section. Sneak peek: Slices have a dynamic size.
