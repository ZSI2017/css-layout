## 双飞翼布局  ##
**始于淘宝UED**

**特点：**
 - 中间内容最先渲染
 - 中间内容的`div`外部又嵌套了一层`div`,使用`margin`，保证中间内容不被覆盖
 - 相比圣杯布局，使用了更加少的`CSS`,多了额外的`div`
 - 页面结构更加清晰,少用了`position`定位属性

**基础HTML**
```
<div class="" id="container">
  <div id="main" class="col">
     <div id="main-wrap">  #main</div>
  </div>
  <div id="left" class="col">  #left </div>
  <div id="right" class="col"> #right </div>
</div>
```

**CSS 样式**
- 同样利用浮动，使三栏在一列
   ```
     .col {float: left;}
   ```
- 中间内容，外部`div`宽度，覆盖整个页面，内部`div`，利用`margin`保证左右侧边不被覆盖。
   ```
   #main {width: 100%;height: 400px;background-color: #ccc;}

   #main-wrap {margin: 0 190px 0 190px;}
   ```
- 左和右侧边栏，利用负`margin-left`，被拉到第一行
  ```
    #left {width: 190px;height: 400px;margin-left: -100%;background-color: #0000FF;}

    #right {width: 190px;height: 400px;margin-left: -190px;background-color: #FF0000;}
  ```

[完整css代码](./index.html)
