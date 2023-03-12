* workspace maintenance

```go
// Terminal - init work file
go work init

// Terminal - add go module
go work use ./hello ./greetings

// Folder
|-> hello/
|-> greetings/
|-> go.work

// go.work - file
go 1.20

use (
	./greetings
	./hello
)
```

[[go-lang/go/work/init/init|]]
[[go-lang/go/work/init/init|init]]

