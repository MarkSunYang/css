精通css

基础知识
1.设计代码的结构
2.有意义的文档的重要性
3.命名约定
4.什么时候使用ID和类名
5.微格式

为样式找到应用目标
1.常用的选择器
2.高级选择器
3.新CSS3的选择器
4.特殊性和层叠的作用
5.计划和维护样式表
6.在代码中加注释

层叠和特殊性：
即使在不太复杂的样式表中，寻找同意元素可能有两种或者更多种规则；
Css通过一种称为层叠cascade的过程处理这种冲突，层叠给每个对战分配重要度~~
次序
表有!important的用户样式
标有!important的作者样式
作者样式
用户样式
浏览器/用户代理应用的样式
特殊性~~abcd
style=""  a=1
b等于ID选择器的总数
c等于类、伪类和属性选择器的数量
d等于类型选择器和为元素选择器的数量


style="" 1000
#warp #conatent 两个id 0200
#content .datePosted 一个id一个class 0110
div#content 一个类，一个id 0101
#content 0100
p.comment .datePosted 一个类，两个class 0021

#content div#main-content h2 0202
#content #main-content>h2 0201
body #content div[id="mian-content"]h2{color:green;}


继承和层叠~~
继承：元素的后代会继承样式的某些属性，比如颜色字号，
我们不会在每个元素的每个后代上去添加样式。


规划，组织和维护样式表
1.对应文档应用样式

2.设计代码的结构
为了便于维护，最好把样式分为几大块，常用的规则一般放在最前面，
body的标记，应该由站点上所有元素继承的样式，
接下来是可能需要的全局reset样式，然后是连接、标题和其他元素

 主体的样式
    reset样式
    链接
    标题
    其他元素
 辅助样式
    表单
    通知和错误
    一致的条目
页面结构
    标题、页脚和导航
    布局
页面组件
    各个页面
覆盖
/* @group general style
/* @group helper style
/* @group page struct
/* @group componets
/* @group override