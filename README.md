# SDCycleScrollView_PageControlExtension
SDCycleScrollView基础上的pageControl 扩展和续写.

##效果图
![图片](https://github.com/lilongcnc/SDCycleScrollView_PageControlExtension/blob/master/Image/SDCycleScrollView_PageExtension.gif)


###感谢
感谢室友宋行同学提供的思路,本来是想着用绘制的方法的,因为想到添加图片的方式太过于耗费性能,但是当前基于项目时间比较紧,所以采用了室友实践过的方案. 
后续空闲时间里,会再用绘制的方式重新写一遍.

###思路
就是两张图片,UIView动画改变图片的大小. 
需要注意的的地方就是,阅读源码找到改动的位置 和 处理临界值的情况.
附上一张我的草稿图,图中是按照五张滚动图片的情况画的. i 代表
![图片](https://github.com/lilongcnc/SDCycleScrollView_PageControlExtension/blob/master/Image/yanshi.png)

- index: 代表当前展示的是哪一张     
- i: 代表当前index 情况下,轮播图中所有pageControl的位置x 值
你可以使用代码比较工具,查看一下我改动了哪些代码. 主要是`TAPageControl.m`, `SDCycleScrollView.m`, `ViewController.m`三个文件中.

###关于计算pageControl
关于计算pageControl的 x 坐标值,我们可以分为两部分, 一步是`12+5(长图片的宽度+间距)`何时出现,  还有就是`5+5(短图宽度+间距)`.

为了更便于直观理解,我没有把这两个**魔法数字替**换成`self.dotSize.width`, `self.currentDotSize.width`和`self.spacingBetweenDots`. 大家后期封装可以自行替换.


###交流
![](http://www.lilongcnc.cc/lauren_picture/bottomFace.jpeg)

```
希望能和大家交流技术

[我的博客地址](http://www.lilongcnc.cc/)

[我的简书地址](http://www.jianshu.com/u/842cccac8576)
