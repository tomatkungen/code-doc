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

[[tidy]]
[[mod-init]]
[[mod-edit]]


