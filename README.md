### 项目介绍和学习总结

通过学习完慕课网的电商网站开发课程，利用给的电商网站原型图，自己动手用html+css完成了整站静态页面的编写，更深入的体验和熟悉了电商网站的布局，网页结构的分析和搭建，页面相似部分的样式重用。
*****************************************************************************
**几个总结**

* 电商网站大多是常见的三栏式布局，布要用到常用的浮动定位布局。清除浮动用了伪类清除浮动，代码如下：
```
.clearfix:after {
    content: " ";
    display: block;
    height: 0;
    width: 0;
    visibility: hidden;
    clear: both;
}
.clearfix {
    zoom: 1;
}
```
* 页面中有不止一处轮播图，对于轮播图部分的样式可以把相同的部分提取出来，之后对于不同大小图片，只需设置图片盒子的尺寸即可，下面是我此次用到的轮播图通用样式：
```
.banner {
    float: right;
    position: relative;
    overflow: hidden;
}
.imgBox {
    position: absolute;
    left: 0px;
    top:0;
}
.imgBox li {
    float: left;
}
.imgBox img {
    display: block;
}
```
* 对作为子元素的内容要设置其和父元素外的其他元素距离，应该设置元素的padding值
* 页面还存在一些问题，没有考虑IE兼容性，只是在chrome测试完成，页面的动态展示还没有完善
******************************************************************************
**后续学习目标**

* 接下来要进一步熟悉与后台数据交互
* 熟练使用一门框架进行项目开发
* 深入学习Node.js和前端模块化