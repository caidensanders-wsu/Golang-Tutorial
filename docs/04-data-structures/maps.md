---
id: maps
title: Maps
slug: /maps
---

# Maps in Go

Maps are a collection of key-value pairs, similar to dictionaries in other languages such as Python.

## Declaring and Initializing Maps

There are two common ways of initializing maps: using `make` like with slices, or using map literals.

### Example (map from make)

```go
m := make(map[string]int)
```

### Example (using map literal)

```go
m := map[string]int{"Caiden": 19, "Otis": 32}
```

## Accessing and Modifying Elements

The easiest way to access a value in a map is to just search for the key like such:

```go
m := map[string]int{"Caiden": 19}
fmt.Println(m["Caiden"])
```

We can use the same way of accessing to modify, as such:

```go
m := map[string]int{"Caiden": 19}
m["Caiden"] = 20
```

We can use the `delete` keyword in Go to delete a key-value pair in a map.

```go
m := map[string]int{"Caiden": 19}
delete(m, "Caiden")
```

## Iterating Over a Map

We can iterate over a map using the `range` keyword.

### Example

```go
for key, value := range m {
	fmt.Printf("key: %s, value: %d\n", key, value)
}
```

## Checking Existence

It's very important to make sure that a key exists before just trying to access it. Go makes this easy with an existence check build into maps.

### Example

```go
m := map[string]int{"Caiden": 19}
value, ok := m["Caiden"]
if ok {
	fmt.Println("Caiden is " + value + " years old.")
} else {
	fmt.Println("Caiden does not exist.")
}
```

## Some Properties

- Maps are unordered.
- Keys must be of a comparable type.

## Summary

Maps are a collection of key-value pairs. Maps are unordered and they must contain keys that are comparable. They are very similar to the likes of dictionaries in languages such as Python.
