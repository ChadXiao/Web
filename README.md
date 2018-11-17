# Flexbox布局
------------

## 属性

> - flex-direction 主轴方向
> - flex-wrap 换行方式
> - flex-flow	主轴方向与换行方式
> - justify-content	主轴对齐方式
> - align-items	交叉轴对齐方式
> - align-content	多根轴对齐方式


### flex-direction

> - row(默认) 水平排列
> - row-reverse 水平反向排列
> - column 垂直排列
> - column 垂直反向排列

### flex-wrap

> - nowrap(默认) 不换行
> - wrap 换行，第一行在上面
> - wrap-reverse 换行，第一行在下边

### flex-flow

	.box {
	  flex-flow: <flex-direction> || <flex-wrap>;
	}
	
### justify-content

> - flex-start (默认值)开始位置对齐
> - flex-end 结束位置对齐
> - center 居中
> - space-between 两端对齐
> - space-around 间距相等

### align-items

> - stretch（默认）占满整个容器
> - flex-start 交叉轴开始方向对齐 
> - flex-end 交叉轴结束方向对齐 
> - center 交叉轴居中
> - baseline 项目第一行文字基线对齐

### align-content

> - stretch（默认值）占满整个交叉轴
> - flex-start 交叉轴起点对齐 
> - flex-end 交叉轴结束点对齐
> - center 交叉轴居中
> - space-between 交叉轴两侧对齐 ，中间间隔平均分布
> - space-around 每一项间隔相等

## item属性

- order 排序
- flex-grow 放大比例
- flex-shrink 缩小比例
 - flex-basis 分配多余空间之前项目占据主轴的空间
 - flex flex-grow, flex-shrink 和 flex-basis的简写
 - align-self 项目在交叉轴的对齐方式
 
###  order

> order属性定义项目的排列顺序。数值越小，排列越靠前，默认为0

	.item {
	  order: <integer>;
	}
	
### flex-grow

> flex-grow属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。

	.item {
	flex-grow: <number>; /* default 0 */
	}
		
### flex-shrink

> flex-shrink属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。

	.item {
	  flex-shrink: <number>; /* default 1 */
	}

### flex-basis

> flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。

	.item {
	  flex-basis: <length> | auto; /* default auto */
	}
	
### align-self
> align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。

	.item {
	  align-self: auto | flex-start | flex-end | center | baseline | stretch;
	}



