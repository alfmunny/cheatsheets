# Go Cheatsheet


## Basics

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
