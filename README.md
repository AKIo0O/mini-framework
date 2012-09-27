mini-framework
==============

数据绑定和组件基类。


##中间件的几个难点##
###API继承###
1. 隐私方法不予以继承。有特殊含义的方法不能继承，保证子类的纯洁。
2. 关键方法不能覆盖。如果一个方法是一个组件特殊含义的方法，则这个方法不能被覆盖，只能在子类类封装调用。
3. 调用父级的方法。不予继承的方法为父类特有，保证多个子类在业务之间没有污染。

###组件的堆砌###
初步设计是，可以堆砌的组件是静态的。
通过mix的方法来组合。
需要解决的问题有：

1. 方法优先级。如果3个组件块有重复名字的情况，则标注其优先级。或者组件的API名字加上其组件特征，但是这样API也显得过长。
2. 隐私方法是否堆砌过去。也就是特征属性。
3. 如何保证堆砌出来的组件是可靠的。

###DOM跟组件的耦合###
DOM即为组件？还是DOM只是组件的el。







