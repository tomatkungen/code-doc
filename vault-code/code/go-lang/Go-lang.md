* [[go]]
* Code page [Go-lang](https://go.dev/)
* Download compiler [Go compiler](https://go.dev/dl/)
* Start [Tutorial](https://go.dev/doc/tutorial/) for beginner like me :)
* Search for [Packages](https://pkg.go.dev/)


```shell
go version // to test installation in cmd
```

```vscode
* Vscode trying to install automatic when it recognize go files in map.

* Installing 5 tools at /Users/<usermap>/go/bin in module mode.
	* gotests
	* gomodifytags
	* impl
	* goplay
	* dlv
```

```Vscode
* Vscode recommend that you should install gopls

terminal:
go install -v golang.org/x/tools/gopls@latest

* Installing 1 tool at /Users/kimkarlsson/go/bin in module mode.
	* gopls
```

```go

// go.mod in terminal
go mod init example/hello

// Hello.go
package main

import "fmt"

func main() {
	fmt.Println("Hello, World!")
}

// terminal
go run .
```
