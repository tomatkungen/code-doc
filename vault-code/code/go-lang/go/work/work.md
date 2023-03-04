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

[[work-init]]

