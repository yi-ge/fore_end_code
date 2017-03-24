1、尺寸与边框
-------------

### 1、单位

px、rem等

### 2、尺寸属性

#### 1、宽度

_属性_：  
width : 宽度(以 px 或 % 作为单位)  
max-width : 最大宽度  
min-width : 最小宽度

#### 2、高度

_属性_：  
height : 高度  
max-height:~  
min-height:~

#### 3、页面中允许修改尺寸的元素

1、块级元素全部允许修改  
2、大部分的行内块元素允许修改  
 radio 和 checkbox 除外  
3、元素本身（html元素）具备 width 和 height 的话是允许修改的  
 `<img>` : 行内元素，但允许修改尺寸  
 `<table>` : table元素，但允许修改尺寸  
4、绝大部分的行内元素 "不能修改"

#### 4、溢出

1、什么是溢出  
 当使用尺寸属性限制元素大小时，如果内容所需空间大于元素本身，则会产生溢出  
2、属性  
 overflow:  
 overflow-x:横向溢出处理  
 overflow-y:纵向溢出处理

_取值_：  
 1、visible  
 默认值，显示  
 2、hidden  
 隐藏  
 3、scroll  
 滚动，默认显示滚动条，溢出可用  
 4、auto 自动，溢出时显示滚动条并可用

### 3、边框

#### 1、边框

##### 1、简写属性

border: width style color;  
width: 边框宽度，以px为单位  
style: 边框样式  
 -solid : 实线  
 -dotted : 虚线(点状)  
 -dashed : 虚线(线状)  
color:边框颜色  
 合法的颜色值  
 也可以为transparent(透明)  
ex:  
 1、border:1px solid red;  
 2、border:2px dotted transparent;  
 3、border:0; 或 border:none;

##### 2、单边定义

定义某以方向边框的所有属性  
_语法_：  
 border-方向:width style color;  
 方向：top/right/bottom/left

##### 3、单属性定义

定义 四条边框的 某个属性值  
_语法_：  
border-属性:值;  
_属性_：width/style/color

##### 4、单边单属性定义

_语法_： border-方向-属性:值; ex:

###### 1、上边框颜色为红色

border-top-color:red;

###### 2、下边框样式为虚线

border-bottom-style:dashed;

#### 2、边框倒角

###### 1、what

将 元素 四个角的 直角倒换成圆角

###### 2、语法

属性：border-radius 作用：设置四个角的倒角圆的半径 取值：px 或 % 取一个值：表示的四个角的半径相同 ... ... 取四个值：表示从左上角开始，按顺时针方向设置四个角

单角定义: border-left-top-radius: border-left-bottom-radius: border-bottom-right-radius: border-top-right-radius:

#### 3、边框阴影(元素阴影，盒子阴影)

1、语法  
属性：box-shadow  
取值：由 空格 隔开的值列表，指定了阴影的多个属性值  
box-shadow:h-shadow v-shadow blur spread color inset; -h-shadow:  
 --阴影的水平偏移距离,必须的  
 --取值为正，阴影右偏移  
 --取值为负，阴影左偏移  
 -v-shadow:  
 --阴影的垂直偏移距离,必须的  
 --取值为正，阴影下偏移  
 --取值为负，阴影上偏移  
 -blur : 可选，模糊距离  
 -spread : 可选，阴影大小  
 -color : 可选，颜色  
inset : 可选值，将默认的外阴影改为内阴影

#### 4、轮廓

##### 1、what

绘制元素边框外的一条线

##### 2、语法

_属性_：  
outline:width style color;  
outline-width:轮廓宽度  
outline-style:轮廓样式  
outline-color:轮廓颜色

outline:none; 或 outline:0;

2、框模型
---------

### 1、框模型

_框_：Box，主要作用是为了盛装内容，页面所有元素皆为框  
_框模型_：Box Model，定义了元素框处理元素内容，内边距，边框 和 外边距的方式

*table*: cellspacing : 单元格 外边距 -> 外边距  
cellpadding : 单元格 内边距 -> 内边距

当框模型属性介入到元素中的时候，元素的整体占地区域会发生改变。

元素整体宽度=左右外边距 + 左右边框 + 左右内边距 + width;  
元素整体高度=上下外边距 + 上下边框 + 上下内边距 + height;

元素可见宽度(边框内)=左右边框+左右内边距+width;  
元素可见高度(边框内)=上下边框+上下内边距+height;
