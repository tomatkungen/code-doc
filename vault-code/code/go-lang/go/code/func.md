## Exported names

* In Go, a name is exported if it begins with a capital letter. For example, `Pizza` is an exported name, as is `Pi`, which is exported from the `math` package
```go
func Pi() { ... } // Export Pi to import in some other package

func pi() { ... } // private pi not accessible from outside package

```