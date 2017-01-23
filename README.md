# SDCycleScrollView_PageControlExtension
SDCycleScrollView基础上的pageControl 扩展和续写.

##效果图
![图片](https://github.com/lilongcnc/SDCycleScrollView_PageControlExtension/blob/master/SDCycleScrollView_PageExtension.gif)


###感谢
感谢室友宋行同学提供的思路,本来是想着用绘制的方法的,因为想到添加图片的方式太过于耗费性能,但是当前基于项目时间比较紧,所以采用了室友实践过的方案. 
后续空闲时间里,会再用绘制的方式重新写一遍.

###思路
就是两张图片,UIView动画改变图片的大小. 
需要注意的的地方就是,阅读源码找到改动的位置 和 处理临界值的情况.
附上一张我的草稿图,图中是按照五张滚动图片的情况画的. i 代表
