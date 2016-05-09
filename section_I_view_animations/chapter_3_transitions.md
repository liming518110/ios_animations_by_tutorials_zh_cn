# 第三章：转场效果
通过前面的两章两章的学习，你已经学会如何使用view的属性如位置、透明度等进行动画播放。但是对于view的进出动画要怎么做呢？

使用之前章节中用的将view移入或者移除用户视野是一个可行的方法。然后本章将会教授另一种改变view呈现状态的动画方法：转场动画。

转场效果是一种view的预定义动画，这些预定义动画不会在view开始到结束中间产生效果，相反的，他只会影响view出现时的效果。

## 转场示例
为了更好的理解何时该使用转场动画，这一小节会先带你领略各种使用转场动画的场景。

###添加一个新的View

![chatper3_01](./images/chapter3_01.png)

通过调用和之前章节类似的API，可以为屏幕上新出现的view增加动画，不同的时，这次需要制定一个名为"animation container view"转场动画效果.

这个转场动画将作用在容器View和其容纳的所有子View上，请看如下代码片段：

	var animationContainerView: UIView?
		animationContainerView = UIView(frame: view.bounds) 		animationContainerView!.frame = view.bounds view.addSubview(animationContainerView!)

		//add the new view via transition
			duration: 0.33,








	.TransitionFlipFromRight 
	.TransitionCurlUp 
	.TransitionCurlDown 
	.TransitionCrossDissolve 
	.TransitionFlipFromTop 
	.TransitionFlipFromBottom

###删除一个view

![chapter3_02](./images/chapter3_02.png)

为从屏幕中移除一个View添加动画效果和上面的新增一个View的动画效果是类似的。只要将动画效果block里面的函数改成`removeFromSuperview()`就可以了，如：

	//remove the view via transition



和前面的例子一样，闭包中的转场动画效果将会作用在“newView”的退出时。
