* Add dependency module to go.mod
* go get < depenency >

```go
// terminal - add dependecy
go get golang.org/x/example

// terminal - add reqiure version
go mod tidy

// go.mod
require (
	golang.org/x/example v0.0.0-20220412213650-2e68773dfca0equire (
	...
require (
	golang.org/x/example v0.0.0-20220412213650-2e68773dfca0 // indirect
	...
```