## grid 网格布局 ##

> grid 布局，是一个二维的基于网格的布局系统。通过将css规则应用于父元素（成为网格容器）和改元素的子元素（网格元素），来使用网格布局。

**[完整指南](https://segmentfault.com/a/1190000012889793)**


- 指定Grid Container
  设置父容器的`display`,同时利用`grid-template-columns`,将页面设置成三列,中间放`main`,设置成`auto`,实现宽度自适应。左右侧边栏就需要设置固定的宽度。

  在利用 `grid-area`指定网格区域的名称来定义网格模板，分别为三栏指定名称`left main right`;


  ```
  .container {
    display:grid;
    grid-template-columns:150px auto 150px;
    grid-template-rows:auto;
    grid-template-areas:"left main right";
    box-sizing:border-box;
    border:1px solid #ddd;
    border-radius:4px
  }
  ```

- 为三列指定不同的`grid-area`名称，嵌套到不同的网格中.
 ```
     #main {
       grid-area:main;
       background-color:#ddd;
     }
     #left {
       grid-area:left;
       background-color: yellow;
     }
     #right {
       grid-area:right;
       background-color:blue;
     }
 ```
 [完整代码](./index.html)
