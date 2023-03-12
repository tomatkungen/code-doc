* Root workspaces
* Create workspace file

```go
// Terminal - init work file
go work init

// go.work - file created
go 1.20 
```


```go
// Terminal - init work file
go work init ./hello

// go.work - file created
go 1.18

use ./hello

// or
go 1.20

use {
	./greetings
	./hello
}
```
