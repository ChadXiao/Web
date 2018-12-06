## css区块模型

 - <a href="#1">框模型（box-sizing）</a>
 - <a href="#2">背景裁剪（Background clip）</a>
 - <a href="#3">内容溢流</a>
 - <a href="#4">框类型</a>

### <a name="1">模型（box-sizing）</a>

 - content-box(默认值)
 - border-box
 - padding-box

> box-sizing 属性用于更改用于计算元素宽度和高度的默认的 CSS盒子模型。可以使用此属性来模拟不正确支持CSS盒子模型规范的浏览器的行为。

 - content-box(默认值)

> width 和height 只包括内容的宽和高，不包括边框、内边距和外边距

![content-box模型][1]

  
 - border-box

> width和height包括内容，内边距和边框，但不包括外边距

	width = border + padding + content  width
	height = border + padding + content height
	
![border-box模型][2]

 - padding-box

>只有firebox能用， Firebox 50 已被删除  width 和 height 包括内容和内边距，但不包括边框和外边距。

 - 兼容性

|  Chrome   |   Edge  |  Firefox (Gecko)   |  Internet Explorer   |  Opera   |  Safari (WebKit)   |  
| --- | --- | --- | --- | --- | --- | 
|   1.0 -webkit 10.0  |  (Yes)   |   1.0 (1.7 or earlier)-moz 29.0 (29.0)  |   8.0  |   7.0  |  3.0 (522)-webkit 5.1|

|   Android  |   Firebox Mobile(Gecko)  |  IE Phone   |   Opera Mobile  |   Safari Mobile  |
| --- | --- | --- | --- | --- |
|  2.1 -webkit 4.0   |  1.0 -moz  29.0   |   9.0  |   YES  |  YES   |


### <a name="2">背景裁剪（Background clip）</a>

> background clip属性用于设置背景的延伸方式

 - border-box
 - padding-box
 - content-box

####  border-box

> 延伸背景到外边框外沿，但在外边框之下

![ border-box][3]

#### padding-box

> 外边框下面没有背景，即背景延伸到内边距外沿

![padding-box背景裁剪][4]

#### content-box

> 延伸到内容区外沿

![content-box][5]


#### text

> 背景被裁剪为文字的前景色**chrome浏览器需添加-webkit-前缀；最新版本火狐【63.0.3（64位）】支持直接使用background-clip：text属性**


![text][6]


### <a name="3">溢流</a>
  
  

> 当一个元素内容太大而无法适应块级上下文时，可以使用overflow来处理


 - visible（默认）内容不会被修剪，会呈现在元素框之外
 - hidden  内容会被修剪，并且其余内容不可见 
 - scroll 内容会被修剪，浏览器会显示滚动条以便查看其余内容
 - auto  由浏览器定夺，如果内容被修剪，就会显示滚动条


#### [兼容性][7]

### <a name="4">框类型</a>

 - block

> 内容会独占一行，而且可以设置它的宽高

 - inline

> 随着文档的文字流动（例如：它将会和周围的文字和其他行内元素出现在同一行，而且它的内容会像一段中的文字一样随着文字部分的流动而打乱），对行内盒设置宽高无效，设置padding, margin 和 border都会更新周围文字的位置，但是对于周围的的块框（ block box）不会有影响。

 - inline-box

> 重新另起一行但会像行内框（ inline box）一样随着周围文字而流动，而且他能够设置宽高，并且像块框一样保持了其块特性的完整性，

  


  [1]: ./images/%29%5DUKXOA%5DBZ72S$8NJH9AJFW.png "content-box模型"
  [2]: ./images/$P[Y3VW5{YS1}0KNN%6_@ZA.png   "border-box模型"
  [3]: ./images/FC%7BJ4MFGUNX608%5D~JO343TJ.png " border-box"
  [4]: ./images/_8%5B6%7B$_GP%5BP~JJJVIA$Q%29UR_1.png "padding-box背景裁剪"
  [5]: ./images/OF%5BCEZ%7BM0EYC%7BS$Y60$GB_U.png "content-box"
  [6]: ./images/VA~NO6@J%6G]$FCYZ@XVS04_1.png "text"
  [7]: https://developer.mozilla.org/zh-CN/docs/Web/CSS/overflow