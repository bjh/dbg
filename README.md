#### Getting Started

- run `go get github.com/bjh/dbg`
- write `init` function to set up the logging/output
- call with DEBUG=true
- `DEBUG=true go run amazing-project.go`


```go
package main

import (
	"os"

	"github.com/bjh/dbg"
	"github.com/sirupsen/logrus"
	"github.com/subosito/gotenv"
)

func init() {
	gotenv.Load()

	if os.Getenv("DEBUG") == "true" {
		logrus.SetLevel(logrus.DebugLevel)
	}
}

func main() {
	dbg.Log("Hello, World!")
}
```
