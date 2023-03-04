* `go mod tidy` ensures that the `go.mod` file matches the source code in the module
* Scans go files and adds any missing module

```go
// hello.go
...
import "rsc.io/quote"
...

// Terminal - add package from https://pkg.go.dev/
go mod tidy
```
