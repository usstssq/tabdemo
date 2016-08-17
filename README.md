BFC: Box, Formatting ,Context
块级元素
行级元素
run-in box(css3中才有)

BFC是块级格式化上下文，是一套渲染规则，它决定了其子元素如何定位，以及其他元素的关系和互相作用，最常见的格式化上下文有BFC,
块级格式化上下文，和IFC行级格式化上下文

CSS 2.1中只有BFC和IFC，CSS3中还增加了GFC和FFC

BFC布局规则：
1、内部的Box会在垂直方向，一个接一个地放置
2、Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠。关于margin重叠，是上下重叠，左右不会重叠。
3、每个元素的margin box的左边，与包含块border box的左边相接触（对于从左到右的格式化，否则相反）。即使存在浮动也是如此。
4、BFC的区域不会与float box重叠。
5、BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素，反之也是如此。
6、计算BFC的高度时，浮动元素也参与计算。

哪些元素会产生BFC?
1、跟元素自带BFC
2、float属性不为none
3、position为absolute或fixed
4、display为inline-block,table-cell,table-caption,flex,inline-flex
5、overflow不为visible