# width/height作用的具体细节

### 深藏不露的width:auto

?> `width`的默认值`auto`

**auto有很多不同的宽度表现**

> - **充分利用可用空间：**一般`div`、`p`元素默认为100%于父级元素，名字叫`fill-available`

> - **收缩和包裹：**典型的是浮动、绝对定位、inline-block元素或table元素，称为`shrink-to-fit`

> - **收缩到最小：**一般会在`table-layout:auto`的表格中出现

> - **超出容器限制：**除非有明确的width相关设置，否则不会超过父级容器宽度，也有特殊的，比如很长的连续的引文和数字，又或者内联元素被设置了`white-space: nowrap`

### 



