# example-in-memory-cache
Я не зрозумів, як правельно робити домашня завдання. Був би радий, щоб Ви пояснили, як правельно його зробити.
Код наведений нижче я взяв рандомний з ютубу.

```go
go get github.com/dmytrodemianchuk/in-memory-cache
```

```go
package main

import (
	"fmt"
	"time"

	"github.com/dmytrodemianchuk/in-memory-cache"
)


type example struct {
	Name string
	age  int
}

func main() {

	newExample := &Example{
		Name: "Dima",
		Age:  18,
	}

	c := cache.New(3*time.Minute, 5*time.Minute)

	abcd, found := c.Get("abcd")

	if found {
		abcd.([]Example)
		a = append(a, *newExample)
		c.Set("abcd", a, cache.NoExpiration)
		fmt.Println("Stored from if Part")

	} else {
		c.Set("abcd", newExample, cache.NoExpiration)
		fmt.Println("stored from else Part")

	}

	abcd, found = c.Get("abcd")
	if found {
		fmt.Println(abcd)
	}
}