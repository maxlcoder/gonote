## 流程控制语句

#### if

```go
if x < 1 {
    return 'x小于1'
}

if x := 2; x < 1 {
    return 'x小于1'
}

```

#### switch

> go的switch由上而下进行判断，只要匹配到了直接返回，不需要break

```golang
// 参数赋值，判断
switch a := 1; a {
    case 1:
        fmt.Println("a is 1")
    case 2:
        fmt.Println("a is 2")
    default:
        fmt.Println("a is nothing")
}

// 外置参数
switch 


```
