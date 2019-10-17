# structure and cascade

#### Specificity

| content                       | specificity |
| ----------------------------- | ----------- |
| 类属性值、**属性选择** 或伪类 | 0,0,1,0     |
| 各个元素和伪类                | 0,0,0,1     |
| ID属性值                      | 0,1,0,0     |

```css
p em{ color:purple;} /* specificity=0, 0, 0, 2 */
p.bright em.dark {color: maroon;} /* specificity= 0 0 2 2 */
html> body table tr[id="totals"] td ul > li{color:maroon;}/* specificity=0 0 1 7 */
```

**important**应该放在分号前面

```css
p.light{color:yellow; font:smaller Times, serif !important;}
```

> 比较规则：!important>没有important 然后再比较同一分组下specificity的差异

#### 继承

继承是css中“熟视无睹”的规则，但是有些属性不能被继承比如 `border`

> 0特殊性比无特殊性要强

一个声明在样式表或文档中的位置越靠后，它的权重越大。

#### Comparing

```css
p {color:gray !important;} /*胜出*/ 
<p style="color:black;"> Well, <em>hello</em> there!</p>
```

```css
p em{color:black;} /*author's style sheet 胜出*/ 
p em{color:yellow;}/*reader's style sheet */
```

```css
p em{color:black !important;} /* author's style sheet*/
p em{color:yellow !important;}/* reader's style sheet 胜出*/
```

权重大小的顺序
> 1. 读者的重要声明
> 2. 创作人员的重要声明
> 3. 创作人员的正常声明
> 4. 读者的正常声明
> 5. 用户代理声明

 