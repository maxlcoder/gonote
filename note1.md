## go语法上的注意点

#### 变量赋值

```
var a int
a = 1

var a int = 1
var a = 1 (可省略int)

a := 1 (不能在函数外面使用)

var (
    fsdf bool = false
    fsd int   = 0
)
```

#### 零值

```
var c int, d bool 
```
> 数值类型为 `0`，
> 布尔类型为 `false`，
> 字符串为 `""`（空字符串）

#### go多值返回

> 这个没有什么可说的，主要是函数可以定义且返回多值

#### 没有参数的 return 语句返回结果的当前值

```
func split(sum int) (x, y int) {
	x = sum * 4 / 9
	y = sum - x
	return
}

func main() {
	fmt.Println(split(17))
}
```
> 可以从上面看到，当没有给`return`返回值时，会默认返回函数定义的字段，同时要求函数定义的返回字段与程序中出现的字段名匹配

```
func split(sum int) (int, int) {
	x := sum * 4 / 9
	y := sum - x
	return x, y
}

func main() {
	fmt.Println(split(17))
}
```
> 注意上面两种写法的不同之处，第一种相当与在函数返回值定义中初始化了变量，第二种则是在函数中初始化了变量，而且第二种`return`后面必须带上返回字段 

#### 常量

```
const Pi = 3.14
```

> 常量不能使用`:=`

#### 数组

1. 定义和赋值分开
```
var arr [3]string

arr[0] = "123"
arr[1] = "sss"
```
> 数组容量必须提前定义

2. 定义和赋值合并
```
arr := []string{"123", "sss", "ggg"}
```
> 数组容量将根据实际赋值确定
