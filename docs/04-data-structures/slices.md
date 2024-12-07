---
id: slices
title: Slices
slug: /slices
---

# Slices in Go

A slice is a dynamically-sized way to view the elements of an array.

## Creating Slices

There are many ways to create slices. One way is from an array.

### Example (slice from an array)

```go
arr := [5]int{1, 2, 3, 4, 5}
slice := arr[1:4] // Includes elements at index 1 to 4. 
```

We can also use a function built into Go called `make`, like so,

### Example (slice from make)

```go
slice := make([]int, 5)
```

That last example created a slice of 5 integers, all initialized to 0.

## Modifying Slices

Slices are different than arrays when it comes to copying. A slice is a reference to an underlying array. Thus, modifying a slice changes the original array at the same time.

### Example

```go
arr := [5]int{1, 2, 3, 4, 5}
slice := arr[1:4]
slice[0] = 100
```

The above code modified arr[1], as that is where slice starts, and set arr[1] equal to 100.

## Slice Operations

There are many operations for slices in Go, but some common ones are: `append`, `len`, `cap`.

`append`: adds another item onto the end of an array

```go
slice := []int{1, 2, 3}
slice = append(slice, 4, 100)
```

`len`: returns the number of items in a slice

```go
fmt.Println(len(slice))
```

`cap`: returns the number of items from the beginning of the slice to the end of the underlying array.

```go
fmt.Println(cap(slice))
```

## Conclusion

Slices are a way of viewing arrays that allow a dynamic-size. That is why they are preferred over arrays. Slices are references to the underlying arrays and as such they share the same underlying data.


