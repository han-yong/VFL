# 使用VFL语言给代码添加约束条件
```
|:   表示父视图
-:  表示距离
V:  表示垂直
H:  表示水平
>=: 表示视图间距、宽度和高度必须大于或等于某个值
<= :表示视图间距、宽度和高度必须小宇或等于某个值
== :表示视图间距、宽度或者高度必须等于某个值
@:  优先级 最大为  1000

|-[view]-|:                          视图处在父视图的左右边缘内
|-[view]  :                          视图处在父视图的左边缘
|[view]   :                              视图和父视图左边对齐
V:[view(100.)]  :                        设置视图的高度
H:[view(100.)]  :                        设置视图的宽度
|-30.0-[view]-30.0-|:                表示离父视图 左右间距  30
|-[view(view1)]-[view1]-| :              View和view1视图宽度一样，并且在父视图内
V:|-padding-[imageView]->=0-[button]-padding| : 表示离父视图的距离为Padding,这两个视图间距必须大于或等于0并且距离底部父视图为padding。此时必须对 metrics参数赋值eg.  metrics:@{@"topMargin":@100};

[wideView(>=60@700)]  :视图的宽度为至少为60 优先级为700
```
