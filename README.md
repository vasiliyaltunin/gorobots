# Robots.txt Gin's middleware

Gin middleware to support robots.txt.

based on https://github.com/thinkerou/favicon

## Usage

### Start using it

Download and install it:

```sh
$ go get github.com/vasiliyaltunin/gorobots
```

Import it in your code:

```go
import "github.com/vasiliyaltunin/gorobots"
```

### Canonical example:

```go
package main
            
import (
    "github.com/gin-gonic/gin"
    "github.com/vasiliyaltunin/gorobots"
)
            
func main() {
    r := gin.Default()
    r.Use(gorobots.New("./static/robots/robots.txt"))

    r.Run(":8080")
}
```
