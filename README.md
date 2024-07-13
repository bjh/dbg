#### Getting Started

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
