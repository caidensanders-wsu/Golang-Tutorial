---
id: packages-modules
title: Packages & Modules
slug: /packages-modules
---

# Modularization in Go

Modularization is a common practice in programming that involves taking a large chunk of code and organizing it into smaller, reusable parts. In Go, modularization is done through two concepts named **packages** and **modules**.

## Packages

A **package** in Go is a collection of code files grouped together. Every single file in Go belongs to a package, the `package` keyword is used to define the package. Packages allow a reuse of code across projects.

### Example (creating a package)

1. Create a folder, `mypackage`.
2. Create a file, `mypackage/mypackage.go`:
   ```go
   package mypackage

   func Hello() string {
   	return "Hello from mypackage"
   }
   ```
3. Use the package in a Go program:
   ```go
   package main

   import (
   	"fmt"
   	"mypackage"
   }

   func main() {
   	fmt.Println(mypackage.Hello())
   }
   ```
4. To run this, place the `mypackage` folder in the same directory as the main program.

## Exported vs. Unexported

In a Go package, there are some identifiers that are exported and some that are not. An identifier is exported if it starts with an uppercase letter. If an identifier begins with a lowercase letter, it is unexported, and it is considered private to the package.

### Example

```go
package mypackage

// The following identifier will be exported.
func ExportedFunc() {
	fmt.Println("This is exported.")
}

// The following identifier will be unexported, or "private."
func unexportedFunc() {
	fmt.Println("This is unexported.")
}
```

## Modules

Go Modules are used for dependencies in a Go project. They allow versions and easy importing/exporting of external libraries.

### Example (creating a Go Module)

1. Create a new project directory.
2. Run:
   ```bash
   go mod init (my_module_name)
   ```

This creates a `go.mod` file which tracks your module's name and dependencies.
Using the `go get` command, third party dependencies can be added to your project.
```bash
go get github.com/some/go/library
```

## Conclusion

Go allows modularization with two separate features: Go Packages and Go Modules. A package is a directory within a project that allows separating files with similar logic or features. A module allows your code to be versioned and used as a dependency in other projects.
