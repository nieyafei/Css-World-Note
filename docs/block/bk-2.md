# width/height作用的具体细节

### 深藏不露的width:auto

?> `width`的默认值`auto`

**auto有很多不同的宽度表现**

> - **充分利用可用空间：**一般`div`、`p`元素默认为100%于父级元素，名字叫`fill-available`

> - **收缩和包裹：**典型的是浮动、绝对定位、inline-block元素或table元素，称为`shrink-to-fit`

> - **收缩到最小：**一般会在`table-layout:auto`的表格中出现

> - **超出容器限制：**除非有明确的width相关设置，否则不会超过父级容器宽度，也有特殊的，比如很长的连续的引文和数字，又或者内联元素被设置了`white-space: nowrap`

#### 1、外部尺寸和流体特性

?> 对于`block容器`的流动性，是会铺满整个容器的，这也就是为什么不需要设置`width: 100%`的属性，因为这是默认的显示，其实100%不是那么的的简单的，而是**margin/padding/border/content内容区域自动分配水平空间的机制**

**大神总结的三无准则：`无宽度，无图片，无浮动`**

<vuep template="#demo1"></vuep>
<script v-pre type="text/x-template" id="demo1">
<style>
  .cons{
    width: 80%;
  }
</style>
<template>
  <div class="cons">
    <ul>
      <li>1</li>
      <li>2</li>
    </ul>
  </div>
</template>
<script></script>
</script>

- **格式化宽度**

> 这种格式化宽度只会出现在`绝对定位模型`中，也就是 `position`的值是`absolute`和`fixed`

?> 当left/top或top/bottom对立方位的属性值同时存在时，元素的宽度表现为`格式化宽度`

<vuep template="#demo2"></vuep>
<script v-pre type="text/x-template" id="demo2">
<style>
  .cons{
    width: 80%;
  }
</style>
<template>
  <div class="cons">
    <ul>
      <li>1</li>
      <li>2</li>
    </ul>
  </div>
</template>
<script></script>
</script>

#### 2、内部尺寸和流体特性



### 



