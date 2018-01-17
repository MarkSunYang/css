css 权威指南

1.css 选择器

选择器分组 h1,h2,h3{ color:red; }
通配符选择器 *{color:red;}
类选择器
.classname{color:red;}
element.classname{color:red;}
多类选择器
ID选择器
属性选择器：

文档结构：父子关系

2.结构层叠：
继承是从一个元素向后代元素传递属性值所采用的机制，确定应该响应一个元素，用户
代理不仅考虑继承，还要考虑声明的特殊性。

选择器的特殊性：
style="" 1,0,0,0
1.对于选择器中的各个ID属性值： 加 0,1,0,0 
2.对于选择器中给定的各个类属性、属性或伪类，加 0,0,1,0 
3.对于选择器中给定的各个元素和伪元素 加0,0,0,1 
4.通配符选择器对特殊性没有任何贡献 0,0,0,0

h1{color:red;} 给定元素 0001
p em{color:purple;} 0002
.graper{color:purple;} 0010
*.bright{color:yellow;} 0001
p.birght em.dark{color:maroon;} 0022
#id216{color:blue;} 0100
div#sidebar *{href} {color:silver;}


重要性

!important

继承样式继承


文本属性：
text-indent:块级元素的缩进，无法应用于行内元素的缩进，
图像之类的替换元素也无法应用于text-indent属性，
一个会计元素中的首行如果有一个图像，它会随改行的其余文本移动

正常流：从上向下显示
非替换元素：元素的内容包括在文档之中，则成为非替换元素，
如果一个段落的文本内容都放在该元素本省之内，这个段落就是非替换元素

替换元素：
作为其他内容占位符的一个元素，img 
块级元素
行内元素
