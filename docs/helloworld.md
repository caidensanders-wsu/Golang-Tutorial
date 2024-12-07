---
sidebar_position: 2
---

# Your First Program in Go

## Hello, World

To test if everything was installed correctly and works, we are going to walk through a very simple Hello, World program, or as I like to call it, Hello, Go!

1. Create a new file named `hello.go` in your current workspace.

2. Open the file and add the following code:
   ```go
   package main
   import "fmt"

   func main() {
      fmt.Println("Hello, Go!")
   }
   ```

3. Run the program!
   ```bash
   go run ./hello.go
   ```

You should see the following output on your screen:

```bash
Hello, Go!
```

## Conclusion

If you did not get any output to your screen, or if you had any errors, try referring back to the last tutorial, installing go, and if that doesn't fix your issue, check Golang's website for more updated docs.

### Onto the basics! Proceed.
