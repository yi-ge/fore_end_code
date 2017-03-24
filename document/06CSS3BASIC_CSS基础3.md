```
1、CSS Sprites
	雪碧图，精灵图
	将若干小图拼合到一副大图中去，通过背景图以及背景图像定位实现图像移动以便显示
	实现步骤：
	1、根据想看图像大小，创建等比区域
	2、设置背景图 以及 位置 ，来实现图像的显示
2、渐变
	1、什么是渐变
		渐变就是多种颜色柔和变化
	2、渐变重要特点
		色标：指定渐变的 颜色 及其 出现位置
	3、渐变的分类
		1、线性渐变
		2、径向渐变
		3、重复线性渐变
		4、重复径向渐变
	4、语法
		1、属性
			background-image
		2、取值
			1、线性渐变
				linear-gradient(angle,color-point1,color-point2,......)
				详解：
					1、angle ：方向 或 角度
						1、方向：关键字
							1、to top : 从下向上填充
							2、to right : 从左向右填充
							3、to bottom : 从上向下填充
							4、to left : 从右向左填充
						2、角度
							0deg ~ 360deg
							关键度数:
							0deg : to top
							90deg : to right
							180deg : to bottom
							270deg : to left
					2、color-point : 色标
						颜色值   位置值
						ex:
						1、red 0%
						2、green 15px
						3、blue 30%
						4、yellow
							由浏览器自动分配颜色
			2、径向渐变
				语法：
					1、属性
						background-image
					2、取值
						radial-gradient(size at position,color-point1,color-point2);
						1、size at position
							size ：半径值
							at ：关键字，不能省略
							position ：圆心所在位置

							注意：size at position 是可以省略的
			3、重复线性渐变
				语法：
					属性：background-image
					取值：repeating-linear-gradient(同线性渐变);
						repeating-linear-gradient(to bottom,red 0%,green 10%,blue 20%);
			4、重复径向渐变
				语法：
					取值：repeating-radial-gradient(同径向渐变);
	5、浏览器兼容性问题
		对于不支持渐变的浏览器，可以添加浏览器前缀来适应渐变效果
		浏览器前缀：
			Firefox ：-moz-
			Chrome & Safari ：-webkit-
			Opera : -o-
			IE : -ms-
		1、如果浏览器不支持属性的话，前缀则加载属性名称前
			ex:
				animation : css3中做动画的属性

				-moz-aniamtion:值;/*火狐*/
				-webkit-animation:值;/*Chrome&Safari*/
				-o-aniamtion:值;/*Opera*/
		2、如果浏览器不支持属性值的话，前缀则加在属性值的前面
			background-image:-moz-linear-gradient();
			....
3、文本格式化
	1、字体属性
		1、字体系列
			属性：font-family
			取值：value1,value2,... ...
			注意：如果字体中包含 中文 ，特殊符号，最好用 "" 或 '' 引起来
			ex:
				font-family:"microsoft yahei",arial,verdana,simsun;
		2、字体大小
			属性：font-size
			取值：px ，pt ，em ，rem
			注意：大小是受 font-family 影响
		3、字体加粗
			属性：font-weight
			取值：
				1、normal ：正常(无加粗)
				2、bold ：加粗
				3、整百倍数的数字
					400 : normal
					900 : bold
		4、字体样式
			属性：font-style
			取值：
				1、normal ：正常
				2、italic ：斜体
		5、小型大写字符
			作用：
				将英文字符中的小写字母转换为大写字母，但是大小与小写字母一样
			属性：font-variant
			取值：
				1、normal : 正常
				2、small-caps : 小型大写字符
		6、字体属性(简写)
			font : style variant weight size family;
			注意：
				使用简写模式，family的值必须要设置，否则无效
	2、文本属性
		1、文本颜色
			属性：color
			取值：颜色合法值
		2、文本排列方式
			作用：控制元素内容的水平排列方式
			属性：text-align
			取值：left / center / right / justify
		3、文本修饰(线条修饰)
			属性：text-decoration
			取值：
				1、none
					无任何线条修饰
				2、underline
					下划线修饰
				3、overline
					上划线
				4、line-through
					删除线 -> <s></s>
		4、行高
			作用：一行数据的高度,每行文字将在指定的行高范围内垂直居中显示
			场合：
				1、设置一行文本的垂直居中效果
				2、设置行间距
			属性：line-height
			取值：
				1、以 px 为单位的数值
				2、无单位数字表示倍数
					line-height:1.5;
		5、首行文本缩进
			属性：text-indent
			取值：以 px 为单位的数值
		6、文本阴影
			属性：text-shadow
			取值：h-shadow v-shadow blur color;
4、表格属性
	1、表格常用属性
		1、边距属性 : padding
		2、尺寸属性 : width , height
		3、文本格式化属性：font-*,text ...
		4、背景属性 : background-*
		5、边框属性 : border
		6、垂直方向对齐 :
			属性：vertical-align
			取值：top / middle / bottom
	2、表格特有属性
		1、边框合并
			属性：border-collapse
			取值：
				1、separate
					默认值，分离边框模式
				2、collapse
					边框合并
		2、边框边距
			1、作用
				设置相邻的两个单元格之间的距离
			2、属性
				属性：border-spacing
				取值：
					指定一个值：水平和垂直间距相同
					指定两个值：
						第一个值表示水平间距
						第二个值表示垂直间距
						两个值，用空格隔开
			3、注意
				仅在 边框模式为 分离模式下 才有效(border-collapse:separate;)
		3、标题位置
			属性：caption-side
			取值：
				1、top
					默认值，标题在表格之上
				2、bottom
					标题在表格之下

		4、显示规则
			1、作用
				指定表格的布局方式,相当于指定单元格，行，表格的 尺寸算法模式
			2、语法
				属性：table-layout
				取值：
					1、auto
						自动
						列宽度由单元格的内容决定，默认值 - 自动表格布局
					2、fixed
						固定
						列宽度由设定为准，不以内容尺寸来决定-固定表格布局
			3、自动表格布局 VS 固定表格布局
				1、自动表格布局
					1、单元格大小由内容决定
					2、表格复杂时，加载速度慢(缺点)
					3、适用于不确定每列大小时使用(场合)
					4、布局方式足够的灵活(优点)
				2、固定表格布局
					1、单元格大小由设定的值为准
					2、加速显示表格(优点)
					3、确定每列大小时使用(场合)
					4、布局方式不够灵活(缺点)













```
