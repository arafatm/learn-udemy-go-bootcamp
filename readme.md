# Udemy: Go Bootcamp

https://www.udemy.com/course/learn-go-the-complete-bootcamp-course-golang/learn/lecture/12329000#overview

Code: https://github.com/inancgumus/learngo

## Configure VS Code

Open VS Code; from the extensions tab at the left, search
for "go" and install it

Close VS Code completely and open it up again

Go to View menu; select Command Palette
- Or just press cmd+shift+p

Type: go install
- Select "Go: Install/Update Tools"
- Check all the checkboxes

After it's done, open the Command Palette again
- Type: shell
- Select: "Install 'code' command in PATH"

NOTE: You don't have to do this if you're on Windows.

## 7. What is GOPATH?

`go env` to see all go env set

`go env PATH` to see the `$GOPATH`

:warning: course assumes using `$GOPATH` in `$HOME/go`

## 10. Compile with "go build"

`go build` compiles your code
- `./mygocode` to run after compile

:neckbeard: `go help build` to see help

## 12. Run with "go run"

`go run` compiles and runs your code

:neckbeard: `go help run` to see help

`go run -x myprog.go` will show additional info e.g. package imports

## 13. ★ FIRST GO PROGRAM EXERCISES ★

[:ship: 3d10061](https://github.com/arafatm/learn-udemy-go-bootcamp/commit/3d10061)
Exercise: `fmt.Println`

```diff
diff --git a/learngo/02-write-your-first-program/exercises/01-print-names/main.go b/learngo/02-write-your-first-program/exercises/01-print-names/main.go
index 5972806..4f228f5 100644
--- a/learngo/02-write-your-first-program/exercises/01-print-names/main.go
+++ b/learngo/02-write-your-first-program/exercises/01-print-names/main.go
@@ -8,6 +8,8 @@
 
 package main
 
+import "fmt"
+
 // ---------------------------------------------------------
 // EXERCISE: Print names
 //
@@ -24,6 +26,6 @@ package main
 // ---------------------------------------------------------
 
 func main() {
-	// ?
-	// ?
+	fmt.Println("Arafat")
+	fmt.Println("Sally")
 }
```

[:ship: b745f3e](https://github.com/arafatm/learn-udemy-go-bootcamp/commit/b745f3e)
`fmt.Prinln` and `Print` can take multiple params

```diff
diff --git a/learngo/02-write-your-first-program/exercises/01-print-names/main.go b/learngo/02-write-your-first-program/exercises/01-print-names/main.go
index 4f228f5..d4c7def 100644
--- a/learngo/02-write-your-first-program/exercises/01-print-names/main.go
+++ b/learngo/02-write-your-first-program/exercises/01-print-names/main.go
@@ -26,6 +26,6 @@ import "fmt"
 // ---------------------------------------------------------
 
 func main() {
-	fmt.Println("Arafat")
+	fmt.Print("My name is ", "Arafat\n")
 	fmt.Println("Sally")
 }
```

[:ship: ccb74ac](https://github.com/arafatm/learn-udemy-go-bootcamp/commit/ccb74ac)
`fmt.Println` will accept double quote and backtick, but not `single quote`

```diff
diff --git a/learngo/02-write-your-first-program/exercises/01-print-names/main.go b/learngo/02-write-your-first-program/exercises/01-print-names/main.go
index d4c7def..f0a7b10 100644
--- a/learngo/02-write-your-first-program/exercises/01-print-names/main.go
+++ b/learngo/02-write-your-first-program/exercises/01-print-names/main.go
@@ -26,6 +26,6 @@ import "fmt"
 // ---------------------------------------------------------
 
 func main() {
-	fmt.Print("My name is ", "Arafat\n")
+	fmt.Print(`My name is Arafat\n`)
 	fmt.Println("Sally")
 }
```

:neckbeard: `package` and `import` declarations must come at top

## 14. ⭐️ Packages ⭐️

## 17. What is a package?

Rules
- all package files should be in the **same directory**
- all files *in the same folder* should be in the **same package**
  - ie `package "mypkg"`
- `package "main"` to make it executable

## 18. Learn the differences between Executable and Library Packages

An **executable package**
- should be part of `package "main"`
- also include a `func main()`
- cannot be imported

A **Library Package**
- has a `package "mypackage"`
- cannot be executable directly
- can be `import "mypackage"` in other packages

## 19. Scopes: What is the importance of names?

There are **package**, **file**, **func**, and **block** scopes that are **unique within the scope**

```go
package "main"
import "fmt" // file scoped (visible in this file)

const ok = true // package scoped: visible to all files in the package
                // not available to other packages unless imported

func nope() {
  const notok = false
}

func main() {
  var hello = "Hello!" // block scoped declaration

  fmt.Println(hello, ok) // "ok" from declaration above
  fmt.Println(hello, notok) // ERR: notok declared in func nope() scope
}
```

## 20. What is a package scope?


xxx
## 21. The same names in the same package
## 22. Importing happens in the file scope
## 23. Renaming imported packages
## Quiz 3: Prove Yourself: Scopes
## 24. ⭐️ Statements and Expressions ⭐️
## 25. What is a statement?
## 26. What is an expression?
## 27. Print the number of CPUs
## Quiz 4: Prove Yourself: Statements and Expressions
## 28. How Go comments work?
## 29. Quick Notice: Go Doc
## 30. What is Go Doc?
## 31. ★ FUNDAMENTALS EXERCISES ★
## 32. ⭐️ Write a Library Package! ⭐️
## 33. Create your first library package
## 34. How Go standard library exports?
## 35. Export a function from your package
## Quiz 5: Prove Yourself: Library Packages
## 36. ★ LIBRARY PACKAGE
## EXERCISES ★


