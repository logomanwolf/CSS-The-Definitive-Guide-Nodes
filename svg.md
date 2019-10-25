# svg

### viewBox

```html
<svg style="width:150px; height:300px" viewBox="0 0 400 400">
    <circle cx="200" cy="200" r="200" fill="#fdd" stroke="none"></circle>
</svg>
```

在我的理解，就是在viewBox这个小的box里面将图形相对位置调整好，这样当svg的大小发生变化时，图形的位置就不会受到影响。

这个属性会受到隐藏属性 `preserveAspectRatio` 的影响。

`preserveAspectRatio`属性表示是否强制进行统一缩放.

第一个参数有9个不同值可选

```
xMinYMin,
xMinYMid,
xMinYMax,
xMidYMin,
xMidYMid,
xMidYMax,
xMaxYMin,
xMaxYMid,
xMaxYMax
```

x和y表示对齐的轴线，min,mid,max表示对齐的方式。min是往坐标小的方向对齐；mid居中对齐；max是往坐标大的方向对齐（顺带一提svg的坐标0刻度在左上角）。

第二个参数有两个值可选：meet和slice
meet就是前面那种自动调整viewBox到可以在svg画布中完全展示。非常类似css里background-size:contain
而slice是自动调整viewBox到撑满整个svg画布。非常类似background-size:cover

preserveAspectRatio还有个单独使用的参数："none"。
**不会进行强制缩放**。这种时候viewBox会被拉伸到和svg画布相同尺寸，而内部的所有svg元素也会被等比拉伸，而不是维持原有比例。