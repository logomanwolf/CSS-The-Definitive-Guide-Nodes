# pseudo-class selector

#### 伪类

- 伪类的分类(link,visited,focus,hover,active)

```css
//静态伪类
a:link{color:blue;}
a:visited {color:red;}
//动态伪类
:focus
:hover
:active
```

>  伪类的顺序：link-visited-focus-hover-active

- first-child

- lang()

- 结合伪类

```css
//顺序并不重要
a:link:hover{color:red;}
a:visited:hover{color:maroon;}
```

#### 伪元素

- first-letter,first-line,before,after

- first-letter和first-line的限制

- before和after

```css
h2:before{content:'}}';color:silver;}
body:after{content:' The End.';}
```

  