* module maintenance

```go
// Terminal - create mod package
go mod init example/hello

```

```go
// Terminal - add package from https://pkg.go.dev/
go mod tidy
```

```go
// Terminal - Point module to relative path
go mod edit -replace example.com/greetings=../greetings
```

[[go-lang/go/mod/mod|mod]]
[[go-lang/go/mod/edit/edit|edit]]
[[go-lang/go/mod/init/init|init]]





