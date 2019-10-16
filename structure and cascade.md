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
html> body table tr[id="totals"] td ul > li{color:maroon;}/* specificity=0 0 1 7*/

```

