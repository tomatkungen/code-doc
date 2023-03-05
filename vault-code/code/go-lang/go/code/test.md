* < filename >_test.go tells the `go test` command that this file contains test functions
* And function name start Test`Name`

```go

// hello.go
package greetings

import (
    "testing"
)

// hello_test.go
TestHello(t *testing.T) {
	... code ...
}

// terminal - run test with verbose flag where the module map is
go test -v
```
