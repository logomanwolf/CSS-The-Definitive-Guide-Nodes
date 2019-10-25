# color and unit

if a rgb value bigger than `100%` or less than `0%` , it will be automatically adjusted to `100%` or `0%`. 

```css
p.one{color:rgb(300%,4200,-5000%);} /* 100%,100%,0% */
```

#### hex values

`#F00`等价于`#FF0000`

`#6FA`等价于`66FFAA`

#### Web安全颜色

Web安全色可以表示为RGB值20%和51（相应的十六进制值为33）的倍数。

### 单位

#### 相对长度单位

`em`定义为一种给定字体的`font-size`值

`ex`中所用字体中小写`x`的高度

`px`像素

> 非常适合用像素来定义图像大小
>
> 当图像是矢量图时，如果需要图像随文本的大小缩放，不建议使用`px`。

### Global keywords

inherit | initial | unset

all property