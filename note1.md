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

#### 常量

```
const Pi = 3.14
```

> 常量不能使用`:=`