
```go
// terminal - list install path (/Users/<username>/go/bin/hello)
go list -f '{{.Target}}'

// terminal - ./hello will end up in Users/<username>/go/bin/hello
go install

// terminal - setup global path to run every where "hello" - mac
export PATH=$PATH:/path/to/your/install/directory

// terminal - setup global path to run every where "hello" - windows
set PATH=%PATH%;C:\path\to\your\install\directory
```
