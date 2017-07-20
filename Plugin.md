# `plugin`
This module allows writing custom modules in Go using shared objects.

## Writing a plugin
Assuming you already know [Go](https://golang.org/), writing a plugin is not difficult.

### UNIX timestamp example
#### Source code
```go
package main

import (
	"strconv"
	"time"

	. "github.com/reujab/bronze/types"
)

func Main(segment *Segment, args []string) {
	segment.Value = strconv.FormatInt(time.Now().Unix(), 10)
}
```

#### Compiling
```sh
go build -buildmode plugin
```

#### Using the plugin
```sh
BRONZE+=(plugin:black:white:plugin.so)
```
