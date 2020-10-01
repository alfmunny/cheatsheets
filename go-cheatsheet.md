# Go Cheatsheet


## Basics

```
$ go build
```

```go
package main

import ("math")

import (
  "fmt"
  "math/rand"
)



func main() {
  fmt.Printf("%g", math.Sqrt(7))
  fmt.Println("My favarite number is", rand.Intn(10))
  fmt.Println(add(42, 13))
}

```

Function

```go
func add(x int, y int) int {
  return x +y
}

// or
func add(x, y int) int {
  return x + y 
}

// multiple result

func add(x, y int) int {
  return y, x
}

func split(sum int) (x, y int) {
  x = sum * 4 / 9
  y = sum - x
  return // return x, y
}
```

Variables

```go

var c, python, java bool
var i, j int = 1, 2
k := 3
```

Types

```
bool string int int8 int18, ..., byte, rune
```

Constant

```go
const pi = 3.14
1 << 100
1 >> 99
```

for

```go
for i := 0; i < 10; i++ {
  sum += 1
}

for ; sum < 1000; {
  sum += sum
}

for {
}
```

if

```go

if x < 0 {
  reutrn sqrt(-x) + "i"
}

if v := math.Pow(x, n); v < lim {
return v
} else {
}
```

Defer

```
defer fm.Printlin("world")
```

## Methods and interfaces

## Concurrency

Goroutines

```go
go f(x, y, z)
```

Channels

```go
ch = make(chan int)
ch < -v
v := <-ch

go sum(s[:len(s)/2], ch)
go sum(s[len(s)/2:], ch)
x, y := <-c, <-c
```

Range and Close

    sender can close the channel

```go
v, ok := <-ch
i := range c {
  fmt.Println(i)
}
```

Select

```go
select {
  case c <- x:
    x, y = y, x + y
  case <- quit
    fmt.Println("quit")
    return
}
```

\`\`\`
