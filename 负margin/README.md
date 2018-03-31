## 负margin ##
在经典的 [圣杯布局](../圣杯布局/)和[双飞翼布局](../双飞翼布局/)中，共同点就是都把中间的dom节点放在最开始的位置，最先渲染。**主要是利用了负margin可以改变浮动元素的显示位置，即使把DOM节点，放在后面，也可以通过css控制其显示在前面**

- 负margin 不会破坏文档流。
- 它是标准的css 属性。



**static元素上的负margin**

 ![负margin](./margin-motion.gif)


**浮动元素上负margin**
 - 如果给一个浮动元素加上相反方向的负margin，则会使间距为0，且内容重叠。
 - 如果负margin 等于实际宽度，则元素会被完全覆盖。这是因为元素的完全宽度等于margin，padding,border，width相加而成，所以如果负margin等于余下三者的和，那元素的实际宽度也就变成了0px



**使用技巧**

[负margin的一些应用场景](https://www.jianshu.com/p/549aaa5fabaa)，里面介绍了几种比较常用的布局技巧，都利用了负margin的方式实现。

- [简单的两栏布局](./float.html)
- [去除最底边的边框](./border.html)
- [多列等分](./index.html)



**参考链接:**

  [负margin用法权威指南](https://www.w3cplus.com/css/the-definitive-guide-to-using-negative-margins.html)
