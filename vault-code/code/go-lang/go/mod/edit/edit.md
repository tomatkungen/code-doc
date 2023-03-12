* Imports local modules to its module
* `go mod edit -replace` < module > `=` < relative path >

```go
// Terminal - Point module to relative path
go mod edit -replace example.com/greetings=../greetings

// go.mod - add line to file
module example.com/hello

go 1.16

replace example.com/greetings => ../greetings

// Terminal - run tidy to add semver version where module is included ./hello
go mod tidy

```
