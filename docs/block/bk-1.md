# 块级元素

所谓的`块级元素（block-level element）`,他们都有个特征是**在一个水平流上只能单独显示一个元素，多个块级元素则换行显示**

### 问：display:block 和 块级元素 一样？？？

> 这种说法是错误的

> `li`元素的`dispaly:list-item`也是`块级元素`

> `table`元素的`display:table`也是`块级元素`

<vuep template="#demo1" class="full-page"></vuep>
<script v-pre type="text/x-template" id="demo1">
<style>
  .con{
    padding:30px;
  }
  .con .cell{
    width:50%;float:left;padding:0 20px;
  }
  .clear{
    border:10px solid #b4a078;
  }
  .clear img{
    width:100%;
    float:left;
  }
  .clear2:after,.con:after{
    clear:both;
    content:"";
    display: table;// block
  }
</style>
<template>
  <div class="con">
    <div class="cell">
      <span>正常内部float的效果</span>
      <div class="clear">
        <img src="http://img.hb.aicdn.com/a06a559b578bdfb4611dce9b654e15b8d4ee7e6b41e4a-3IJwoF_fw658" />
      </div>
    </div>
    <div class="cell">
      <span>清楚float的效果</span>
      <div class="clear clear2">
        <img src="http://img.hb.aicdn.com/a06a559b578bdfb4611dce9b654e15b8d4ee7e6b41e4a-3IJwoF_fw658" />
      </div>
    </div>
  </div>
</template>
<script></script>
</script>

### 问：为什么实际开发的过程中，不使用dispaly:list-item 设置块级元素，而经常使用block或者table?

> - 字符比较多，其他两个相对少

> - 会出现不需要的项目符合，当然也可以解决 `list-style:none`

> - IE浏览器不支持微元素的`display:list-item`,属于兼容性的问题

### 问：为什么**list-item**元素会出现项目符号？

> 系统会生成一个附加的盒子，学名`标记盒子（marker box）`,专门用来放圆点、数字这些项目符号

### 特殊性别display:inline-block

?> 俗话：穿着`inline`的皮藏着`block`的心,专业名称叫`容器盒子`，

> - 不仅有`inline`的特性，和图文一行显示

> - 而且有`block`的特性，可以设置`width`和`height`


### 盒子display:inline-table

?> 从上面可以知道，`inline`内联盒子和`table`盒子的结合，得到一个和文字在一行中的显示的表格

<vuep template="#demo2"></vuep>
<script v-pre type="text/x-template" id="demo2">
<style>
  .con{
    padding:30px;
  }
  .con .inline-table{
    display:inline-table;
    width:130px;
    background-color:#b4a078;
    text-align:center;
    margin-bottom:10px;
  }
</style>
<template>
  <div class="con">
    <div class="inline-table">
      第一列
    </div>
    <div class="inline-table">
      第二列
    </div>
    <div class="inline-table">
      第三列
    </div>
    <div class="inline-table">
      第一列
    </div>
    <div class="inline-table">
      第二列
    </div>
    <div class="inline-table">
      第三列
    </div>
  </div>
</template>
<script></script>
</script>