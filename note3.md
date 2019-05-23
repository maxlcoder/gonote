## 指针

指针的定义是：变量的内存地址

```golang
i := 1 // 变量i的值是1
p = &i // 注意这里不是`p := &i`，生成指针p, 
fmt.Println(*p) // 输出1，*p表示指向指针p所对应的值

type Vertex struct {
    x int
    y int
}

v := Vertex{1, 2}
p = &v // 生成指向结构体的指针
fmt.Println(p.x) // 输出1，这里结构的的指针可以直接引用值

```


## 数组

go的数组申明必须指定长度


