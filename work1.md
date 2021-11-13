## go

```go
package main

import (
	"fmt"
)

func main() {
	a, b, c, d := make(chan string), make(chan string), make(chan string), make(chan string)
	for i := 0; i < 10; i++ {
		go func() {
			a <- "张三"

		}()
		fmt.Println(<-a)
		go func() {
			b <- "李四"

		}()
		fmt.Println(<-b)
		go func() {
			c <- "王五"

		}()
		fmt.Println(<-c)
		go func() {
			d <- "赵六"
		}()
		fmt.Println(<-d)
	}
}

```

