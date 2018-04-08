# CSS世界的color很单调

- ### 少的可怜的颜色关键词

> 颜色关键词是指类似`red`,`blue`,`black`之类的

**关键词历来版本支持情况：**

> - `CSS1`: 只支持16个基本的关键词

> - `CSS2`:  相对于1新增了一些颜色关键词

> - `CSS3`:  新增了100多个颜色关键词

> - `CSS4`: 增加了`rebeccapurple`关键词  rebeccapurple = #663399

- ### 不支持的transparent关键词

?> `transparent`: 透明

> - IE6及其以上支持：`background-color: transparent`

> - IE7开始支持：`border-color: transparent`

> - IE9开始支持：`color: transparent`


- ### 不支持的currentColor变量

> 事实上很多的属性值默认就是`currentColor`的表现，IE9+可以支持这个变量，可以使用当前`color`值

```css
.test{
  color: red;
  border: 1px solid currentColor;
}

// 其实可以简写如下（推荐）：
.test{
  color: red;
  border: 1px solid;
}

```

- ### 不支持的rgba颜色和hsla颜色

> `color`属性支持16进制颜色、rgb颜色 （这样的写法字符数目最少，书写更快，渲染性能更高）

> `rgb`颜色和十六进制颜色是近亲，都归属于rgb颜色，只是进制区别

> 有些支持或不支持`rgb`数值格式：

> `#f03`、`#F03`、`#ff0033`、`#FF0033`

> `rgb(255,0,51)`、`rgb(255, 0, 51)`、`rgb(255, 0, 51.2)`（整数，不支持小数）

> `rgb(100%,0%,20%)`、`rgb(100%, 0%, 20%)`、`rgb(100%, 0, 20%)`不支持整数和百分比一起使用

?> `hsl`是CSS3才出现的颜色格式，IE9+浏览器支持

?> CSS3还支持了`Alpha透明通道`，因此也就是`rgba`颜色和`hsla`颜色,`a`表示透明度，取值范围是`0~1`


- ### 支持确鸡肋的系统颜色

?> 系统颜色不同的浏览器不一样，我们可以使用系统颜色的变量

- 系统颜色本身有颜色，我们的模块是可以即时预览，双击html模块文件就可以，没有任何依赖

- 系统颜色名称都比较高冷，非常适合作为变量，替换时不会发生冲突


