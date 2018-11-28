# css选择器


----------

 - <a href="#1">元素选择器</a>
 - <a href="#2">类选择器</a>
 - <a href="#3">ID选择器</a>
 - <a href="#4">分组</a>
 - <a href="#5">通配器</a>
 -  <a href="#6">属性选择器</a>
 -  <a href="#7">文档结构</a>
 -  <a href="#8">伪类和伪元素</a>


## <a name="1">元素选择器</a>

	P{
		background-color: red; 
	}

## <a name="2">类选择器</a>

	.warning{
		background-color: red; 
	}
	
#### 元素类选择器
	P.warning{
		background-color: red; 
	}
	
#### 多类选择器

> 同时满足多个类才会被选中

	.test.warning{
		background-color: red; 
	}
	
## <a name="3"> ID选择器</a>

	#warning{
		background-color: red; 
	}
	
## <a name="4">分组</a>

	

> 如果希望多个类或元素同时拥有同样的样式，可以使用‘，’进行分组

	.test, .warning{//test 和warning类的元素都会被选中
		background-color: red; 
	}
	
## <a name="5">通配器</a>

 	*.warning{//所有warning类的元素都会被选中
		background-color: red; 
	}
	
## <a name="6">属性选择器</a>

	

> 要根据元素的属性及属性值来选择元素，可以使用属性选择器，共有四种属性选择器

 - <a href="#61">简单属性选择</a>
 - <a href="#62">具体属性值选择</a>
 - <a href="#63">部分属性值选择</a>
 - <a href="#64">特殊属性选择类型</a>
 
 
 #### <a name="61">简单属性选择</a>
 
 	a[class] {color: silver;}
 	a[class][href] {color: silver;}
 
 
 #### <a name="62">具体属性值选择器</a>
 
 	a[href="#xxx"][title="W3C"]{color: silver;}
	

 #### <a name="63">部分属性值选择器</a>


| 类型 | 描述 |
| ------------ | -------------------------------------- |
| [foo^="bar"] | 选择foo属性值以"bar"开头的所有元素     |
| [foo^="bar"] | 选择foo属性值以“bar”结尾的所有元素   |
| [foo^="bar"] | 选择foo属性值包含子串“bar”的所有元素 |

 
 #### <a name="64">特定属性值选择器</a>
 
 	[lang|="en"]{color: white}//选择所有lang等于”en“或者以”en-“开头的元素
	

## <a name="7">文档结构</a>

 - <a href="#71">后代选择器</a>
 - <a href="#72">子选择器</a>
 - <a href="#73">相邻选择器</a>


 #### <a name="71">后代选择器</a>
 
 	h1 em{color: gray;}//选择所有h1元素的后代为em的元素
	
	
 #### <a name="72">子选择器</a>
 
 	h1 > em{color: gray;}//选择所有h1元素的em子元素
	

 #### <a name="73">相邻选择器</a>
 
 	h1 + p {margin-top: 0;}//所有和h1有相同父元素的段落元素
	
	
## <a name="8">伪类和伪元素</a>

#### 伪类选择器

|   伪类名  |  描述   |
| --- | --- |
|  :link   |   做为超链接（即有一个href属性）并指向一个未访问地址的所有锚。（有些浏览器会不正确的将：link解释为所有超链接，包括已访问和未访问的）  |
|  :visited   |  作为已访问地址超链接的所有锚   |
|     |     |
|   :focus  |  当前拥有输入焦点的元素   |
|   :hover  |  鼠标停留的元素 (IE6之前只允许动态伪类选择超链接，而不允许选择其他元素，IE7所有元素都能使用hover，但不支持表达元素应用：focus)  |
|   :active  |  指示被用户输入激活的元素，例如鼠标停留在超链接上，如果点击就会激活这个超链接的，：activity 将会指示这个超链接  |
|     |   伪类的顺序很重要，最好是“link-visited-hover-active”  |
|     |     |
|   :first-child  |  选择作为第一个子元素的元素   |

#### 伪元素选择器

|     |     |
| --- | --- |
|  :first-letter   |  选择首字母  |
|   :first-line  |  选择首行   |
|  :before   |  元素之前添加   |
|   :after  |   元素之后添加  |
> **警告：**
> css2中:first-letter和:first-line只能用于标记或段落之类的块级元素，不能用于超链接等行内元素
> css2.1中可以应用到所有的元素，当对于CSS属性有限制

伪元素所允许的属性表
|   :first-letter  |  :first-line   |
| --- | --- |
|   所有font属性  |  所有font属性   |
|   color  |   color  |
|   所有background属性  |  所有background属性   |
|   所有margin属性  |  word-spacing   |
|   所有padding属性  |   letter-spacing  |
|   所有border属性  |  text-decoration   |
|  text-decoration(如果float设置为none)   |  vertical-align   |
|  vertical-align   |  text-transform   |
|   text-transform  |  line-height   |
|   line-height  |  clear （仅适用CSS2， CSS2.1已去除）  |
|   float  |  text-shadow （仅适用于CSS2）  |
|   letter-spacing（css2.1新增）  |    
|   word-spacing（Css2.1新增）  |    
|   clear（仅适用CSS2， CSS2.1已去除）  |    
|   text-shadow（仅适用于CSS2）  |    