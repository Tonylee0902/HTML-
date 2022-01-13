####                                                前端学习知识点1：HTML     

####                                                                                                                                

##### 网页：

是构成网站的基本元素。主要由文字，图像和超链接构成。还能包含音频，视频和Flash。



##### Web标准：

- 结构标准（HTML）：超文本标记语言，从语义的角度描述页面的结构。用于对网页元素进行整理和分类。
- 表现标准（CSS）：层叠样式表，从审美的角度美化页面的样式。用于设置网页元素的版式，颜色，大小等外观样式。
- 行为标准（JS）：JavaScript,从交互的角度描述页面的行为。用于定义网页的交互和行为。



##### 浏览器的组成：

- 渲染引擎（浏览器内核）：用来解析HTML和CSS，决定浏览器如何显示网页的内容以及页面的格式信息。作用：读取网页内容，计算网页的显示方式并显示在页面上。

  | 浏览器        | 内核    |
  | ------------- | ------- |
  | chrome        | Blink   |
  | 360安全浏览器 | Blink   |
  | Safari        | Webkit  |
  | Firefox火狐   | Gecko   |
  | IE            | Trident |

- JS引擎（JS解释器）：用来解析网页中的JavaScript代码，网页通过内置JavaScript引擎来执行JS代码，所以JS属于脚本语言。	



##### 浏览器工作原理：

1. User Interface                用户界面，我们一般的浏览器。
2. Browser engine             浏览器引擎，用来查询和操作渲染引擎  。
3. Rendering engine          用来显示请求的内容，负责解析HTML，CSS。
4. Networking                      网络，负责发送网络请求。                 
5. JavaScript Interpreter     JavaScript解析器，负责执行JavaScript的代码。
6. UI Backend                       UI后端，用来绘制类似组合框和弹出窗口。
7. Data Persistence              数据持久化，数据存储cookie, HTML5中的session-Storage。



##### HTML的概念：

​	不是编程语言，是一种描述性的标记语言！

（1）标记语言是一套标记标签。比如：标签<a>表示超链接，标签<img>表示图片，标签<h1>表示一级标题等等，它们都属于HTML标签。

（2）标记语言没有编译过程，HTML标签是直接由浏览器解析执行。



##### HTML是负责描述文档语义的语言：

​	HTML格式的文件是一个纯文本文件（用txt文件改名而成），用一些标签来描述语义，这些标签在浏览器页面上是无法直观看到的。

​	例：<h1>标签有什么用？

​			正确答案：给文本增加主标题的语义。



##### XHTML介绍：

​	可扩展超文本标注语言。是为了取代HTML，也是HTML的升级版，是严格的纯净的HTML。



##### HTML的专有名词：

- 网页：由各种标记组成的一个页面。

- 主页（首页）：一个网站的起始页面 / 导航页面。

- 标记：比如<p>称为开始标记，</p>称为结束标记。

- 元素：比如”<p>内容</p>“称为元素。

- 属性：给每一个标签所做的辅助信息。

- XHTML:符合XML语法标准的HTML。

- DHTML:dynamic，动态的HTML。 JavaScript+CSS+HTML 合起来的页面就是动态HTML。

- HTTP:超文本传输协议。用来规定客户端浏览器和服务端交互时数据的一个格式。SMTP：邮件传输协议，FTP：文件传输协议。

  

##### 初试的HTML页面：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```



##### HTML骨架标签分类：

|     标签名      |    定义    |                          说明                           |
| :-------------: | :--------: | :-----------------------------------------------------: |
|  <html></html>  |  HTML标签  |                页面中最大的标签，根标签                 |
|  <head></head>  | 文档的头部 |       注意在head标签中我们必须要设置的标签是title       |
| <title></title> | 文档的标题 |            让页面拥有一个属于自己的网页标题             |
|  <body></body>  | 文档的主体 | 元素包含文档的所有内容，页面内容 基本都是放到body里面的 |



##### 文档声明头：

​	任何一个标准HTML页面，第一行一定是：

```
<!DOCTYPE ..........>
```

这一行为：文档声明头，简称DTD。告知浏览器文档使用哪种HTML或XHTML规范。

在HTML5中极大简化了DTD（文档声明头）：

```
<!DOCTYPE html>
```



##### 页面语言Lang:

```
<html lang="en">
```

用于指定页面的语言类型，最常见的有两种：

- en:定义页面语言为英文。
- zh-CN:定义页面语言为中文。



##### 头标签head:

(html5的比较完整的骨架 )

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
	<meta name="Author" content="">
    <meta name="Keywords" content="厉害很厉害" />
    <meta name="Description" content="网易是中国领先的互联网技术公司" />
    <title>Document</title>
</head>
<body>
.....
</body>
</html>
```

面试例题：网页的head标签里面，表示的是页面的配置，有什么配置？

​					答：字符集、关键词、页面描述、页面标题、IE适配、视口、iPhone小图标等等

头标签内部的常见标签：

- ```
  <title>:指定整个网页的标题，在浏览器最上方显示。
  ```

- ```
  <base>:为页面上的所有链接规定默认地址或默认目标。
  ```

- ```
  <meta>:提供有关于页面的基本信息。
  ```

- ```
  <body>:用于定义HTML文档所要显示的内容，也称为主体标签，所写的代码在此。
  ```

- ```
  <link>:定义文档与外部资源的关系。
  ```

  

##### meta标签：

​	表示”元“，就是表示基本的配置项目。

​	常见的几种meta标签：

​	（1）字符集charset:

```html
<meta http-equiv="Content-Type" content="text/html;charset=UTF-8">
```

http-equiv相当于http的头文件作用，它可以向浏览器传回一些有用的信息,属性语法格式：

```html
<meta http-equiv="参数" content="参数变量值">
```

Content-Type:显示字符集的设定，设定页面使用的字符集。

charset:字符集，网页的编码方式。UTF-8是最常用的字符编码方式。



​	（2）视口viewport:

```html
<meta name="viewport" content="width=device-width , initial-scale=1.0">
```

width=device-width:表示视口宽度等于屏幕宽度。



​	（3）定义”关键词“：

```html
<meta name="Keywords" content="网易,邮箱,游戏,新闻,体育,娱乐,女性,亚运,论坛,短信" />
```

Keywords:关键字就是告诉搜索引擎这个网页是干嘛的，提高搜索命中率。



​	（4）定义”页面描述“：

```html
<meta name="Description" content="网易是中国领先的互联网技术公司，为用户提供免费邮箱、游戏、搜索引擎服务，开设新闻、娱乐、体育等30多个内容频道，及博客、视频、论坛等互动交流，网聚人的力量。" />
```

![1621321308500](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621321308500.png)

设定Description页面描述，在搜索时能显示这些语句，称为SEO：搜索引擎优化。



​	（5）刷新：

```html
<meta http-equiv="refresh" content="3;http://www.baidu.com">
```

3秒后自动跳转到百度页面。



##### base标签：

```html
<base href = "/">
```

base 标签用于指定基础的路径。指定之后，所有的 a 链接都是以这个路径为基准。



##### body标签：

- bgcolor:设置整个网页的背景颜色。
- background:设置整个网页的背景图片。
- text:设置网页中的文本颜色。
- leftmargin:网页的左边距。IE浏览器默认是8个像素。
- topmargin:网页的上边距。
- rightmargin:网页的右边距。
- bottommargin:网页的下边距。

```html
<body link="red" alink="blue" vlink="green">
	<a href = "#">点我点我</a>
</body>
```

​	link属性：表示默认显示的颜色。

​	alink属性：表示鼠标点击但是没有松开时的颜色。

​	vlink属性：表示点击完成之后显示的颜色。



##### 标题标签：

使用<h1>和<h6>进行定义。<h1>定义最大的标题，<h6>定义最小的标题。具有align属性，属性值可以是：left , center ,right。

```html
<body>
	<h1 align="center">永不止步</h1>
</body>
```



##### HTML注释：

```html
<!--  HTML注释  -->
```



##### 段落标签p：

```html
<p> This is a paragraph </p>
```

属性：

align = "属性值" ：对齐方式。属性值包括left , center , right 。

```html
<p align="center"> This is a paragraph </p>
```

*注意：p标签是一个文本级标签！！只能放文字，图片和表单元素*



##### HTML标签等级：

- 文本标签：p、span、a、b、i、u、em。文本级标签里只能放**文字、图片、表单元素**。（a标签里不能放a和input）

  

- 容器级标签：div、h系列、li、dt、dd。容器级标签里可以放置任何东西。



##### 水平线标签hr :

```html
<body>
	<p>自古情深留不住</p>
	<hr />
	<p>总是套路得人心</p>
</body>
```

属性介绍：

- `align="属性值"`：设定线条置放位置。属性值可选择：left right center。
- `size="2" `：设定线条粗细。以像素为单位，内定为2。
- `width="500"`或`width="70%"`：设定线条长度。可以是绝对值（单位是像素）或相对值。如果设置为相对值的话，内定为100%。
- `color="#0000FF"`：设置线条颜色。
- `noshade`：不要阴影，即设定线条为平面显示。若没有这个属性则表明线条具阴影或立体。

```html
<hr align="center" size="2" width="500" color="#0000FF"></hr>
```



##### 换行标签br ：

```html
This <br /> is a paragraph <br / > with line breaks
```

作用为强制换行显示，需要使用换行标签。



##### div和span标签：

- **div标签**：可以把标签中的内容分割为独立的区块。必须单独占据一行。属性：align="属性值"：设置块儿的位置。属性值可选择： left , right , center。
- **span标签**：和div的作用一致，但不换行。



##### div和span的区别：

`<span>`和`<div>`唯一的区别在于：`<span>`是不换行的，而`<div>`是换行的。

​	如果单独在网页中插入这两个元素，不会对页面产生任何的影响。这两个元素是专门为定义CSS样式而生的。或者说，DIV+CSS来实现各种样式。

​	DIV是一个**容器级**的标签，可以内嵌DIV

​	SPAN是一个**文本级**的标签，只能放图片，文字和表单元素，其余都不行。



SPAN例子：

```html
<p>
	简介简介简介简介简介简介简介简介
	<span>
		<a href="">详细信息</a>
		<a href="">购买</a>
	</span>
</p>
```

DIV例子：

```html
<div class="header">
	<div class="logo"></div>
	<div class="nav"></div>
</div>
<div class="content">
	<div class="guanggao"></div>
	<div class="dongxi"></div>
</div>
<div class="footer"></div>
```

DIV+CSS模式：DIV标签负责布局，结构，分块 。 CSS负责样式。



##### 内容居中标签`<center>`：

这个center是一个标签而不是属性值，作用：将标签里的内容在浏览器上居中。但不常用，基本使用CSS实现。

```html
<center>
	<p>继续加油</p>
	<p>不要放弃</p>
</center>
```



##### 预定义（预格式化）标签`<pre>`：

```html
<pre>
	继续努力

	
	不断加油！
</pre>
```

作用：保留标签内部所有的空白符（空格，换行符），原封不动的输出。但在真正的排版中不需要。



##### 字体标签：

转义字符：

- `&nbsp;`：空格 （non-breaking spacing，不断打空格）
- `&lt;`：小于号（less than）
- `&gt;`：大于号（greater than）
- `&amp;`：符号`&`
- `&quot;`：双引号
- `&apos;`：单引号
- `&copy;`：版权`©`
- `&trade;`：商标`™`



##### 下划线，中划线，斜体：

- `<u>`：下划线标记
- `<s>`或`<del>`：中划线标记（删除线）
- `<i>`或`<em>`：斜体标记
- font :字体标签（已舍弃）

```html
<body>
	<font>小圆</font><br >
	<u>小圆</u><br >
	<s>小圆</s><br >
	<i>小圆</i>
</body>
```

这几个标签常用于做一些小装饰，小图标。



##### 粗体标签b:

```html
<body>
	<font>小圆</font><br >
	<b>小圆</b>
</body>
```



##### 上标`<sup>` 下标`<sub>`：

```
O<sup>2</sup>    5<sub>3</sub>
```

记忆方式：p为up , b为 down。来区分上下标



##### 超链接：

（1）外部超链接：

```html
<a href = "02页面.html"点击进入另一个文件</a>
```

href="地址" ：超文本地址

```html
<a href="www.baidu.com" target="_blank">点我</a>
```

target的属性介绍：

- _blank :在一个新的窗口打开被链接的文档。
- _self ：在当前页面打开被链接的文档。
- _parent : 在父框架集中打开被链接的文档。
- _top : 在整个窗口打开被链接的文档。



（2）锚链接：

​	是一种特殊的超链接。锚点可以在同一页面的不同位置间跳转，其实就是在元素间跳转，让用户方便在页面的不同部分间跳转。

​	1.建立锚点目标，只需要给元素增加id或者name，推荐使用id：

```html
<div id="test" name="test"></div>
```

​	2.创建跳转到id=”test"的div的锚点。

```html
<a href="#test"></a>
```

*注意：锚点的超链接路径一定要包含"#"，后面紧跟着元素的 id/name，所以 id和name必须一样*

建立锚点的元素必须要有id或name,最好两个都有。



<u> 同一个页面不同部分的跳转，锚点的写法：</u>

```html
目标元素：<p id="test"></p>  锚点超链接<a href="#test">回到test</a>
```

<u>不同页面的跳转，同时存在锚点：</u>

```html
目标元素：a.html页面的<div id="test" />   锚点超链接<a href="a.html#test"></a>
```

<u>不同页面带参数跳转，同时存在锚点：</u>

```html
目标元素： a.php?p=abc页面的<div id="test" /> 锚点超链接:<a href="a.php?p=abc#test"></a>
```



（3）邮件链接：

```html
<a href="mailto:xxx@163.com">点击进入我的邮箱</a>
```

作用：点击之后，会弹出outlook，作用不大



##### 超链接的属性：

- `href`:目标URL
- `title`:鼠标悬停文本
- `name`:主要用于锚点的名称。

```html
<a href="1.html" title="悬停文本" target="_blank">链接的内容</a>
```



##### 区分`img`和`a标签`的各自属性：

```html
<img src="1.jpg" />

区分----------------

<a href="1.html"></a>
```



##### `img`标签的介绍：

使用`img`标签在网页中显示图像，是一个单标签。

```
<img src="图片的URL" />
```

- 能插入图片类型：jpg(jpeg) , gif , png , bmp等。
- 不能插入图片类型：psd , ai 等。

HTML不能直接插入图片，而是插入图片的引用地址，所以要先把图片上传到服务器上。



##### `img`标签的`src`属性：

`src`属性：指图片的路径。在写图片路径的时候有：相对路径 ， 绝对路径。

写法一：相对路径：

相对于当前页面的所在的路径。两个标记`.`和`..`分别代表当前目录和上一层目录。

```html
<!-- 当前目录中的图片 -->
<img src="2.jpg">
<img src=".\2.jpg">

<!-- 上一级目录中的图片 -->
<img src="..\2.jpg">
```

当前html页面有一个并列的文件夹`images`，在文件夹`images`中存放了一张图片`1.jpg` 效果：

```html
<img src="images/1.jpg">
```



写法二：绝对路径：

（1）以盘开始的绝对路径。

```html
<img src="C:\Users\qianguyihao\Desktop\html\images\1.jpg">
```

（2）网络路径。

```html
<img src="http://img.smyhvae.com/20200122_200901.png">
```



##### `img`标签的weight，height属性：

- `width` ：图像的宽度。
- `height`: 图像的高度。

在HTML5中的单位是CSS像素，在HTML4中既可以是像素也可以是百分比。

可以只指定width和height中的一个值，浏览器会根据原始图像进行缩放。

**重要提示**：如果要想保证图片等比例缩放，只设置width和height中其中一个。



##### Alt属性：

`alt`:当图片无法显示的时候，代替图片显示的内容。

```html
<img src="images/22.jpg" width="300" height="300" alt="美女"
```



##### `img`标签的title属性：

`title`:提示性文本。鼠标悬停时出现的文本。

title 元素的值一般作为提示条(tooltip)呈现给用户，在光标于图片上停下后显示出来。

如果一幅图片需要小标题，使用 `figure`或 `figcaption` 元素

```html
<img src="images/1.jpg" width="300" height="`188" title="这是美女">
```



##### `img`标签的align属性：

​	图片的`align`属性：图片和周围文字的相对位置。属性值可以取：bottom(默认),center , top ,left , right。

​	（1）`align=" " ` ：图片和文字低端对齐。即默认情况（bottom）：

```html
呵呵<img src="3.jpg" align=" ">哈哈
```

![1621393518507](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621393518507.png)

​	

（2）`align="center "`：图片和文字水平方向上居中对齐，效果：

![1621393785947](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621393785947.png)

​	

（3）`align="top"` :图片和文字顶端对齐。

![1621393863791](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621393863791.png)



（4）`align="left"` :图片在文字的左边。

![1621393947955](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621393947955.png)



（5）`align="right"`:图片在文字的右边。

![1621394007801](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621394007801.png)



##### 其他已废弃的属性

- `Align`（已废弃）：指图片的水平对齐方式，属性值可以是：top、middle、bottom、left、center、right。该属性已废弃，替换为 `vertical-align`这个CSS属性。
- `border`（已废弃）：给图片加边框，单位是像素，边框的颜色默认黑色。该属性已废弃，替换为 `border`这个CSS属性。
- `Hspace`（已废弃）：指图片左右的边距。
- `Vspace`（已废弃）：指图片上下的边距。



##### 列表标签：

（1）无序列表`<ul>` , 无序列表中的每一项是`<li>`。

- `<ul>`  : 无序列表。
- `<ul>` :  列表项。

```html
<ul>
	<li>默认1</li>
	<li>默认2</li>
	<li>默认3</li>
</ul>
```

注意：

- `li`不能单独存在，必须包裹在`<ul>`里面。反过来说`<ul>`的子项只能是li。
- `ul`的作用，并不是给文字增加小圆点的，而是增加无序列表的“语义”的。

属性：

- `type="属性值"`。属性值可以选： `disc`(实心原点，默认)，`square`(实心方点)，`circle`(空心圆)。 

```html
<ul>
	<li>实心原点1,默认</li>
	<li>实心原点2,默认</li>
	<li>实心原点3,默认</li>
</ul>

<ul type="square">
	<li>实心方点1</li>
	<li>实心方点2</li>
	<li>实心方点3</li>
</ul>

<ul type="circle">
	<li>空心圆1</li>
	<li>空心圆2</li>
	<li>空心圆3</li>
</ul>
```

![1621394990341](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621394990341.png)

不管是`<ul>`标签有`<type>` , `<ul>`里面的`<li>`标签也有`<type>`属性。（但很少见）

```html
<ul type="cicrle"
	<li>训练</li>
	<li type="square">训练</li>
	<li>训练</li>
</ul>
```

![1621395210052](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621395210052.png)

注意：项目符号可以是图片，需要通过CSS设置`<li>`标记的背景图片来实现。

列表是可以嵌套的。

```html
 <ul>
	<li><b>北京市</b>
		<ul>
			<li>海淀区</li>
			<li>朝阳区</li>
			<li>东城区</li>

		</ul>
	</li>

	<li><b>广州市</b>
		<ul>
			<li>天河区</li>
			<li>越秀区</li>
		</ul>
	</li>
  </ul>
```

![1621395367284](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621395367284.png)

**css 属性**：

```css
list-style-position: inside   /* 给 ul 设置这个属性后，将小圆点包含在 li 元素的内部 */
```



##### `ul`标签实际应用场景：

###### 导航条，li是一个容器级标签，**li里面什么都能放，甚至可以再放一个`ul`**。



（2）有序列表`<ol>` , 里面的每一项是`<li>`

```html
<ol >
	<li>呵呵哒1</li>
	<li>呵呵哒2</li>
	<li>呵呵哒3</li>
</ol>
```

![1621395741992](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621395741992.png)

**属性：**

- `type="属性值"`。属性值可以是：1(阿拉伯数字，默认)、a、A、i、I。结合`start`属性表示`从几开始`。

```html
<ol type="1">
	<li>呵呵</li>
	<li>呵呵</li>
	<li>呵呵</li>
</ol>

<ol type="a">
	<li>嘿嘿</li>
	<li>嘿嘿</li>
	<li>呵呵</li>
</ol>

<ol type="i" start="4">
	<li>哈哈</li>
	<li>哈哈</li>
	<li>哈哈</li>
</ol>

<ol type="I" start="10">
	<li>么么</li>
	<li>么么</li>
	<li>么么</li>
</ol>
```

![1621395907587](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621395907587.png)

`ol`和`ul`就是语义不一样，怎么使用都是一样的。` ol`里面只能有li，`li`必须被`ol`包裹。li是容器级。



（3）定义列表`<dl>`:

`<dl>`英文单词：definition list，没有属性。dl的子元素只能是`dt`和`dd`。

- `<dt>`：definition title 列表的标题，这个标签是必须的
- `<dd>`：definition description 列表的列表项，如果不需要它，可以不加

备注：`dt`、`dd`只能在dl里面；`dl`里面只能有`dt`、`dd`。

```html
<dl>
	<dt>第一条</dt>
	<dd>你若是觉得你有实力和我玩，良辰不介意奉陪到底</dd>
	<dd>我会让你明白，我从不说空话</dd>
	<dd>我是本地的，我有一百种方式让你呆不下去；而你，无可奈何</dd>

	<dt>第二条</dt>
	<dd>良辰最喜欢对那些自认能力出众的人出手</dd>
	<dd>你可以继续我行我素，不过，你的日子不会很舒心</dd>
	<dd>你只要记住，我叫叶良辰</dd>
	<dd>不介意陪你玩玩</dd>
	<dd>良辰必有重谢</dd>

</dl>
```

![1621396260581](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621396260581.png)

上图可以看出，定义列表表达的语义是两层：

- （1）是一个列表，列出了几个dd项目
- （2）每一个词儿都有自己的描述项。

备注：`dd`是描述`dt`的。

定义列表用法非常灵活，可以一个`dt`配很多`dd`：

```html
<dl>
		<dt>北京</dt>
		<dd>国家首都，政治文化中心</dd>
		<dd>污染很严重，PM2.0天天报表</dd>
		<dt>上海</dt>
		<dd>魔都，有外滩、东方明珠塔、黄浦江</dd>
		<dt>广州</dt>
		<dd>中国南大门，有珠江、小蛮腰</dd>
	</dl>
```

还可以拆开，让每一个dl里面只有一个`dt`和`dd`，这样子感觉清晰一些：

```html
<dl>
		<dt>北京</dt>
		<dd>国家首都，政治文化中心</dd>
		<dd>污染很严重，PM2.0天天报表</dd>
	</dl>

	<dl>
		<dt>上海</dt>
		<dd>魔都，有外滩、东方明珠塔、黄浦江</dd>
	</dl>

	<dl>
		<dt>广州</dt>
		<dd>中国南大门，有珠江、小蛮腰</dd>
	</dl>
```

![1621396521718](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621396521718.png)

上图的结构如下：

```html
<dl>
	<dt>购物指南</dt>
	<dd>
		<a href="#">购物流程</a>
		<a href="#">会员介绍</a>
		<a href="#">生活旅行/团购</a>
		<a href="#">常见问题</a>
		<a href="#">大家电</a>
		<a href="#">联系客服</a>
	</dd>
</dl>
<dl>
	<dt>配送方式</dt>
	<dd>
		<a href="#">上门自提</a>
		<a href="#">211限时达</a>
		<a href="#">配送服务查询</a>
		<a href="#">配送费收取标准</a>
		<a href="#">海外配送</a>
	</dd>
</dl>
```

`dt`、`dd`都是容器级标签，想放什么都可以。所以，现在就应该更加清晰的知道：用什么标签，不是根据样子来决定，而是语义（语义本质上是结构）。



##### 表格标签：

用`<table>`表示，一个表格由每行`<tr>`组成，每行由每个单元格`<td>`组成的。

注意：一个表格是由行组成（行是由列组成），而不是由行和列组成。

例：3行4列的单元格

```html
<table>
	<tr>
		<td>朱一龙</td>
		<td>23</td>
		<td>男</td>
		<td>黄冈</td>
	</tr>

	<tr>
		<td>许嵩</td>
		<td>29</td>
		<td>男</td>
		<td>安徽</td>
	</tr>

	<tr>
		<td>邓紫棋</td>
		<td>23</td>
		<td>女</td>
		<td>香港</td>
	</tr>

</table>
```

上面的单元格是没有边框的，接下来应该使用`<table>`的标签。

##### `<table>`的属性：

- `border`：边框。像素为单位。

- `style="border-collapse:collapse;"`：单元格的线和表格的边框线合并（表格的两边框合并为一条）

  效果：![1621403024018](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621403024018.png)

  

- `width`：宽度。像素为单位。

- `height`：高度。像素为单位。

- `bordercolor`：表格的边框颜色。

- `align`：**表格**的水平对齐方式。属性值可以填：left right center。 注意：这里不是设置表格里内容的对齐方式，如果想设置内容的对齐方式，要对单元格标签`<td>`进行设置）

- `cellpadding`：单元格内容到边的距离，像素为单位。

  ​	默认情况下，文字是紧挨着左边那条线的，即默认情况下的值为0。 注意不是单元格内容到四条边的距离哈，而是到一条边的距离，默认是与左边那条线的距离。

  

  如果设置属性`dir="rtl"`，那就指的是内容到右边那条线的距离。

  

- `cellspacing`：单元格和单元格之间的距离（外边距），像素为单位。默认情况下的值为0

- `bgcolor="#99cc66"`：表格的背景颜色。

- `background="路径src/..."`：背景图片。 背景图片的优先级大于背景颜色。

- `bordercolorlight`：表格的上、左边框，以及单元格的右、下边框的颜色

- `bordercolordark`：表格的右、下边框，以及单元格的上、左的边框的颜色 这两个属性的目的是为了设置3D的效果。

- `dir`：公有属性，单元格内容的排列方式(direction)。 可以 取值：`ltr`：从左到右（left to right，默认），`rtl`：从右到左（right to left） 既然说`dir`是共有属性，如果把这个属性放在任意标签中，那表明这个标签的位置可能会从右开始排列。



##### `<tr>`：行

表格由一行一行组成的。

属性：

- `dir`：公有属性，设置这一行单元格内容的排列方式。可以取值：
  - `ltr`：从左到右（left to right，默认）
  - `rtl`：从右到左（right to left）
- `bgcolor`：设置这一行的单元格的背景色。 注：没有background属性，即：无法设置这一行的背景图片，如果非要设置，可以用`css`实现。
- `height`：一行的高度
- `align="center"`：一行的内容水平居中显示，取值：left、center、right
- `valign="center"`：一行的内容垂直居中，取值：top、middle、bottom



##### `<td>`：单元格

属性：

- `align`：内容的横向对齐方式。属性值可以填：left right center。如果想让每个单元格的内容都居中，这个属性太麻烦了，以后用css来解决。
- `valign`：内容的纵向对齐方式。属性值可以填：top middle bottom
- `width`：绝对值或者相对值(%)
- `height`：单元格的高度
- `bgcolor`：设置这个单元格的背景色。
- `background`：设置这个单元格的背景图片。



##### 单元格的合并

单元格的属性：

- `colspan`：横向合并。例如`colspan="2"`表示当前单元格在水平方向上要占据两个单元格的位置。
- `rowspan`：纵向合并。例如`rowspan="2"`表示当前单元格在垂直方向上要占据两个单元格的位置。

纵向合并：

```html
<table border="1">
	<tr>
		<td>朱一龙</td>
		<td>18</td>
		<td>男</td>
		<td>安徽</td>
	</tr>
	
	<tr>
		<td>邓紫棋</td>
		<td>20</td>
		
		<td colspan="2">香港</td>
	</tr>
</table>
	
```

![1621404474015](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621404474015.png)

纵向合并：

```html
 <table border="1">
        <tr>
            <td rowspan="2">朱一龙</td>
            <td>18</td>
            <td>男</td>
            <td>安徽</td>
        </tr>
        
        <tr>
            
            <td>20</td>
            <td>女</td>
            <td colspan="2">香港</td>
        </tr>
    </table>
```

![1621404595281](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621404595281.png)

##### `<th>`：加粗的单元格。相当于`<td>`+`<b>`

属性同`<td>`标签。



##### `<caption>`表格的标题：

使用时和`tr`标签并列 。

属性：`align`，表示标题相对于表格的位置。属性取值可以是：left、center、right、top、bottom 



##### 表格的`<thead>`标签 ， `<tbody>标签`   , `<tfoot>`标签

这三个标签有与没有的区别：

- 1、如果写了，那么这三个部分的**代码顺序可以任意**，浏览器显示的时候还是按照thead、tbody、tfoot的顺序依次来显示内容。如果不写thead、tbody、tfoot，那么浏览器解析并显示表格内容的时候是从按照代码的从上到下的顺序来显示。
- 2、当表格非常大内容非常多的时候，如果用`thead`、`tbody`、`tfoot`标签的话，那么**数据可以边获取边显示**。如果不写，则必须等表格的内容全部从服务器获取完成才能显示出来。

```html
 <body>

	<table border="1">

		<tbody>
		<tr>
			<td>生命壹号</td>
			<td>23</td>
			<td>男</td>
			<td>黄冈</td>
		</tr>
		</tbody>

		<tfoot>
		<tr>
			<td>许嵩</td>
			<td>29</td>
			<td>男</td>
			<td>安徽</td>
		</tr>
		</tfoot>

		<thead>
		<tr>
			<td>邓紫棋</td>
			<td>23</td>
			<td>女</td>
			<td>香港</td>
		</tr>
		</thead>

	</table>

 </body>
```

![1621411299011](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621411299011.png)

（会先显示`thead`然后是`tbody`,最后是`tfoot`，无论它们代码的顺序。）



##### 框架标签：

若我们需要在一个网页上显示多个页面，那么就需要运用框架标签。

注意：

- 框架标签不能放在`<body>`标签里面，因为`<body>`标签代表的只是一个页面。而框架标签代表的是多个页面，所以`<frameset>`和`<body>`只能二选一。

- 框架的集合用`<frameset>`，然后在`<frameset>`集合里放入一个一个的`<frame>`。

- `frameset`定义一个框架集，包含多个子框架，每个框架都有独立的文档。

  `iframe`是个内联框架，是在页面里生成一个内部框架。



##### `<frameset>`：框架的集合

一个框架的集合可以包含多个框架或框架的集合。

**属性：**

- `rows`：水平分割，将框架分为上下部分。写法有两种：

（1）绝对值写法：`rows="200,*"` 其中`*`代表剩余的。这里其实包含了两个框架：上面的框架占200个像素，下面的框架占剩下的部分。

（2）相对值写法：`rows="30%,*"` 其中`*`代表剩余的。这里其实包含了两个框架：上面的框架占30%，下面的框架占70%。



注：如果你想将框架分成很多行，在属性值里用逗号隔开就行了。

- `cols`：垂直分割，将框架分为左右部分。写法有两种：

（1）绝对值写法：`cols="200,*"` 其中`*`代表剩余的。这里其实包含了两个框架：左边的框架占200个像素，右边的框架占剩下的部分。

（2）相对值写法：`cols="30%,*"` 其中`*`代表剩余的。这里其实包含了两个框架：左边的框架占30%，右边的框架占70%。

注：如果你想将框架分成很多列，在属性值里用逗号隔开就行了。

```html
<frameset rows="20% , *">
	<frame src="top.html"></frame>
	<frameset cols="40% , *">
		<frame src="left.html"></frame>
		<frame src="right.html"></frame>
	</frameset>
</frameset>
```

![1621413304647](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621413304647.png)





##### `<frame>`:框架

一个框架显示一个页面。

属性：

- `scrolling="no"`：是否需要滚动条。默认值是true。
- `noresize`：不可以改变框架大小。默认情况下，单个框架的边界是可以拖动的，这样的话，框架大小就不固定了。如果用了这个属性值，框架大小将固定。

```html
<frame src="top.html" noresize></frame>
```



- `bordercolor="#00FF00"`：给框架的边框定义颜色。这个属性在框架集合`<frameset>`中同样适用。 颜色这个属性在IE浏览器中生效，但是在google浏览器中无效，不知道为啥。
- `frameborder="0"`或`frameborder="1"`：隐藏或显示边框（框架线）。
- `name`：给框架起一个名字。

利用name可以在框架里进行超链。

![1621413684374](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621413684374.png)

更新right页面为新的页面。



##### 内嵌框架：

​	内嵌框架用`<iframe>`表示。`<iframe>`是`<body>`的子标记。 (frameset / frame不能用在body下面，但iframe可以)。

​	内嵌框架inner frame：嵌入在一个页面上的框架。

**属性：**

- `src="新的页面.html"`：内嵌的那个页面

- `width=800`：宽度

- `height=“150`：高度

- `scrolling="no"`：是否需要滚动条。默认值是true。

- `name="mainFrame"`：窗口名称。公有属性。

  

内嵌框架举例：（在内嵌页面中切换显示不同的压面）

```html
<body>

 	<a href="文字页面.html" target="myframe">默认显示文字页面</a><br>
 	<a href="图片页面.html" target="myframe">点击进入图片页面</a><br>
 	<a href="表格页面.html" target="myframe">点击进入表格页面</a><br>

 	<iframe src="文字页面.html" width="400" height="400" name="myframe"></iframe>
 	<br>
 	嘿嘿

 </body>
```



##### 表单标签：

​	表单标签用`<form>`表示，用于与服务器的交互。表单就是收集用户信息的，就是让用户填写的、选择的。

**属性：**

- `name`：表单的名称，用于JS来操作或控制表单时使用；
- `id`：表单的名称，用于JS来操作或控制表单时使用；
- `action`：指定表单数据的处理程序，一般是PHP，如：action=“login.php”
- `method`：表单数据的提交方式，一般取值：get(默认)和post

注意：表单和表格嵌套时，是在`<form>`标记中嵌套`<table>`。



​	form标签里面的action属性和method属性 :

​	action属性就是表示，表单将提交到哪里。 

​	method属性表示用什么HTTP方法提交，有get、post两种。



##### get提交和post提交的区别：

​	get方式：将表单数据，以“name = value” 形式追加到action指定的处理程序的后面，两者间用？

隔开，每一个表单的” name = value“ 间用”&“号隔开。

​	特点：只适合提交少量信息，并且不太安全，提交的数据类型只限于ASCII字符。

​	

​	post方式：将表单数据直接发送（隐藏）到action指定的处理程序。post发送的数据不可见、Action指定的处理程序可以获取到表单数据。

​	特点：可以提交海量信息，相对来说安全，提交的数据格式是多样的（Word,Excel ,` rar` ,`img`)



**Enctype：** 表单数据的编码方式(加密方式)，取值可以是：application/x-www-form-urlencoded、multipart/form-data。Enctype只能在POST方式下使用。

- Application/x-www-form-urlencoded：**默认**加密方式，除了上传文件之外的数据都可以
- Multipart/form-data：**上传附件时，必须使用这种编码方式**。



##### `<input>`：输入标签（文本框）

用于接收用户输入：

```html
<input type=" text" />
```



**属性：**

- **type="属性值"**：文本类型。属性值可以是：
  - `text`（默认）
  - `password`：密码类型
  - `radio`：单选按钮，名字相同的按钮作为一组进行单选（单选按钮，天生是不能互斥的，如果想互斥，必须要有相同的name属性。name就是“名字”。 ）。非常像以前的收音机，按下去一个按钮，其他的就抬起来了。所以叫做radio。
  - `checkbox`：多选按钮，**name 属性值相同的按钮**作为一组进行选择。
  - `checked`：将单选按钮或多选按钮默认处于选中状态。当`<input>`标签设置为`type="radio"`或者`type=checkbox`时，可以用这个属性。属性值也是checked，可以省略。
  - `hidden`：隐藏框，在表单中包含不希望用户看见的信息
  - `button`：普通按钮，结合js代码进行使用。
  - `submit`：提交按钮，传送当前表单的数据给服务器或其他程序处理。这个按钮不需要写value自动就会有“提交”文字。这个按钮真的有提交功能。点击按钮后，这个表单就会被提交到form标签的action属性中指定的那个页面中去。
  - `reset`：重置按钮，清空当前表单的内容，并设置为最初的默认值
  - `image`：图片按钮，和提交按钮的功能完全一致，只不过图片按钮可以显示图片。
  - `file`：文件选择框。 提示：如果要限制上传文件的类型，需要配合JS来实现验证。对上传文件的安全检查：一是扩展名的检查，二是文件数据内容的检查。
- **value="内容"**：文本框里的默认内容（已经被填好了的）
- `size="50"`：表示文本框内可以显示**五十个字符**。一个英文或一个中文都算一个字符。 注意**size属性值的单位不是像素哦**。
- `readonly`：文本框只读，不能编辑。因为它的属性值也是readonly，所以属性值可以不写。 用了这个属性之后，在google浏览器中，光标点不进去；在IE浏览器中，光标可以点进去，但是文字不能编辑。
- `disabled`：文本框只读，不能编辑，光标点不进去。属性值可以不写。

```html
<form>
	姓名：<input value="好人" ><br >
	昵称：<input value="小菊菊菊菊" readonly=" "><br >
	名字：<input type="text" value="name" disabled=" "><br >
	密码：<input type="password" value="pwd" size="50"><br >
	性别：<input type="radio" name="gender" id="radio1" value="male" checked="">男
		<input type="radio" name="gender" id="radio2" value="female">女<br >
	
	爱好：<input type="checkbox" name="love" value="eat">吃饭
		<input type="checkbox" name="love" value="sleep">睡觉
		<input type="checkbox" name="love" value="bat">打豆豆
</form>
```

![1621480179089](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621480179089.png)



注意：多个个单选框的input标签中，name的属性值可以相同，但是id的属性值必须是唯一的。



四种按钮的举例：

```html
<form>
		<input type="button" value="普通按钮"><br>
		<input type="submit"  value="提交按钮"><br>
		<input type="reset" value="重置按钮"><br>
		<input type="image" value="图片按钮1"><br>
		<input type="image" src="1.jpg" width="800" value="图片按钮2"><br>
		<input type="file" value="文件选择框">
	</form>
```



##### `<select>`：下拉列表标签

`<select>`标签里面的每一项用`<option>`表示。select是选择，option是选项。

select标签和`ul` ,`ol` ,`dl`都是组标签。

`<select>`标签的属性：

- `<multiple>`:可以对下拉列表中的选项进行多选。属性值值为：multiple ，也可以没有属性值。所有可以写成`multiple=" "` ,也可以写成`multiple = "multiple"` 。
- `size="3"`:如果属性值大于1 ， 则列表为滚动视图，默认属性值是1，即下拉菜单

```html
		<select size="3">
			<option>小学</option>
			<option>初中</option>
			<option>高中</option>
			<option>大学</option>
			<option>研究生</option>
		</select>
		<br><br><br>

		<select multiple="">
			<option>小学</option>
			<option>初中</option>
			<option selected="">高中</option>
			<option selected="">大学</option>
			<option>研究生</option>
		</select>
		<br><br><br>

	</form>
```

![1621481088940](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621481088940.png)

##### `<textarea>`标签：多行文本输入框

**属性：**

- `rows="4"`：指定文本区域的行数。
- `cols="20"`：指定文本区域的列数。
- `readonly`：只读。

```html
<form>
		<textarea name="txtInfo" rows="4" cols="20">1、不爱摄影不懂设计的程序猿不是一个好的产品经理。
		</textarea>
</form>
```

![1621481367798](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621481367798.png)

##### 表单的语义化：

我们在注册一个网站的信息的时候，有一部分是必填信息，有一部分是选填信息，这个时候可以利用表单的语义化。

```html
<form>

		<fieldset>
		<legend>账号信息</legend>
		姓名：<input value="呵呵" >逗比<br>
		密码：<input type="password" value="pwd" size="50"><br>
		</fieldset>

		<fieldset>
		<legend>其他信息</legend>
		性别：<input type="radio" name="gender" value="male" checked="">男
			  <input type="radio" name="gender" value="female" >女<br>
		爱好：<input type="checkbox" name="love" value="eat">吃饭
			  <input type="checkbox" name="love" value="sleep">睡觉
			  <input type="checkbox" name="love" value="bat">打豆豆
		</fieldset>

	</form>
```

![1621481653491](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621481653491.png)

表单域用`<fieldset>`标签包起来，并用`<legend>`标签说明表单的用户。`fieldset`有默认样式，可以将它的border设为none  。 legend的display设为none。 



##### `<label>`标签：

```html
<input type="radio" name="sex" /> 男
<input type="radio" name="sex" /> 女
```

​	在上面这段代码中，只有点击单选框才能选中，而点击男和女两个文字是无法选中的，可以使用`<label>`标签来实现。



用`<label>`把input和汉字包裹起来。解决方式如下：

```html
<input type="radio" name="sex" id="nan" /><label for="nan">男</label>
<input type="radio" name="sex" id="nv" /><label for="nv">女</label>
```

label标签的for属性，和input标签的id属性相同。这样label和input就有联系。

复选框也有label：（任何表单元素都有label）

```html
<input type="checkbox" id="kk" />
<label for="kk">10天内免登陆</label>
```



##### 多媒体标签：

​		多媒体包含：音频，视频，Flash。网页上的多媒体基本上都是Flash格式的。不同的浏览器，播客上述视频格式，所使用插件参数又不一样。 上述格式视频一般文件较大，不利于网络下载播放。 一般情况下，是将其它的视频格式，转成Flash来在网页上播放。转换软件：格式工厂等。 Flash格式的视频兼容性非常好，Flash格式的文件很小。

​		

`<bgsound>`标签：播放背景音乐

属性：

- `src="音乐文件的路径"`
- `loop="-1"`:属性值代表播放的次数，-1代表循环播放。

```html
<body>
	<bgsound src="邓紫棋-泡沫.mp3"  loop="-1"></bgsound>
</body>
```

运行效果：打开网页后，播放时网页上显示一片空白。在google浏览器中无法播放。



##### `<embed>`标签：播放多媒体文件（音频，视频等）

<u>主要应用Netscape浏览器，它不是W3C规范。</u>

**属性：**

- `src="多媒体文件的路径"`
- `loop="-1"`：属性值代表播放次数，-1代表循环播放。
- `autostart="false"`：打开网页时，禁止自动播放。默认值是true。
- `volume="100"`：设置默认的音量大小，测试发现这个值好像不起作用哦。
- width：指Flash文件的宽度
- height：指Flash文件的高度
- quality：指Flash的播放质量，质量有高有低 hight low
- pluginspage：如果指定的Flash插件不存在，则从pluginspage指定的地方进行下载。
- type：指定Flash的文件格式类型
- wmode：指Flash的背景是否可以透明，取值：transparent是透明的

`<embed>`标签播放音频举例：

```
 <body>
	<embed src="王菲 - 清风徐来.mp3"></embed>
 </body>
```

注：在HTML5中新增了`<video>`标签播放视频。



##### `<object>`标签：播放多媒体文件（音频，视频等）

<u>主要应用IE浏览器，它是W3C规范。</u>

**属性：**

- `classid`：指定Flash插件的ID号，一般存在于注册表中。
- `codebase`：如果Flash插件不存在，则从codebase指定的地址下载。
- `<param>`标签的主要作用：设置具体的详细参数。

**总结：在网页中插入Flash时，为了同时兼容多种浏览器，需要将`<object>`标签和`<embed>`标签标记一起使用，但使用的顺序是：`<object>`中嵌套`<embed>`标记。**

```html
<object classid="clsid:D27CDB6E-AE6D-11cf-96B8-444553540000" codebase="http://download.macromedia.com/pub/shockwave/cabs/flash/swflash.cab#version=6,0,29,0" width="778" height="202">

  <param name="movie" value="images/banner.swf">
  <param name="quality" value="high">
  <param name="wmode" value="transparent">
  
  <embed src="images/banner.swf" width="778" height="202" quality="high" pluginspage="http://www.macromedia.com/go/getflashplayer" type="application/x-shockwave-flash" wmode="transparent"></embed>
</object>
```



##### `<marquee>`：滚动字幕标签

如果在这个标签里设置内容，打开网页的时候，内容会想弹幕一样自动移动。

属性：

- `direction="right"` :移动的目标方向。属性值可以是left(从右到左移动，默认值），right（从左到右），up（从下到上） ， down（从上到下）。

- `behavior = "slide"`:行为方式。属性可以是`slide`(只移动一次) ， `scroll`（循环移动，默认），`alternate`（循环移动)

  `scroll`和`alternate`的区别:

  ​		两者都属于循环移动，当direction = "right" 的时候，使用behavior = "scroll"的循环方式是		从左到右，从左到右....循环。

  ​		而使用behavior= "alternate"的时候的循环方式是从左到右，从右到左，从左到右....循环



- `scrollamount="30"`：移动的速度。
- `loop="3"`： 循环多少圈。负值表示无限循环。
- `scrolldelay`：移动一次后休息多少时间 ，单位是毫秒。

```html
<marquee behavior="alternate" direction="down"  width="300" height="200" bgcolor="#8c5dc1">我来了</marquee>
```



##### HTML5的介绍：

​	HTML5代表浏览器端技术的一个发展阶段，HTML5包含：`HTML`升级版 ， `CSS`升级版，`JS API`升级版。HTML5是新一代开发web富客户端应用 程序整体解决方案。

​	富客户端：具有很强的交互性和体验的客户端程序。

​	

##### HTML5的应用场景：

（1）极具表现力的网页：内容简约而不简单。

（2）网页应用程序：

- 代替PC端的软件：iCloud , 百度脑图 ， Office 365等。
- APP端的网页：淘宝，京东，美团等。
- 微信端：公众号，小程序等。

（3）混合式本地应用。

（4）简单的游戏。



##### HTML5中HTML新增内容：

- 标签：（1）更语义化标签   （2）应用程序标签

- 属性：（1）链接关系描述    （2）结构数据标记

  ​			 （1）新的表单类型    （2）虚拟键盘适配

- 网页多媒体 ： 音频，视频，字幕。



##### 语义化的标签：

语义标签对于我们并不陌生，如`<p>`表示一个段落、`<ul>`表示一个无序列表。**标签语义化的作用：**

- 能够便于开发者阅读和写出更优雅的代码。

- 同时让浏览器或是网络爬虫可以很好地解析，从而更好分析其中的内容。

- 更好地搜索引擎优化。

  

##### 传统网页布局：

```html
<!-- 头部 -->
<div class="header">
    <ul class="nav"></ul>
</div>

<!-- 主体部分 -->
<div class="main">
    <!-- 文章 -->
    <div class="article"></div>
    <!-- 侧边栏 -->
    <div class="aside"></div>
</div>

<!-- 底部 -->
<div class="footer">

</div>
```

##### H5的经典网页布局：

```html
<!-- 头部 -->
<header>
    <ul class="nav"></ul>
</header>

<!-- 主体部分 -->
<div class="main">
    <!-- 文章 -->
    <article></article>
    <!-- 侧边栏 -->
    <aside></aside>
</div>

<!-- 底部 -->
<footer>

</footer>
```



##### H5中新增的语义标签：

- `<section>`  :表示区块。
- `<article>`  :表示文章。
- `<header>`  :表示页眉。
- `<footer>`  :表示页脚。
- `<nav>`  :表示导航。
- `<aside>`  :表示侧边栏。如文章的侧栏
- `<figure>`  :表示媒介内容分组。
- `<mark>`  :表示标记。
- `<progress>`  :表示进度。
- `<time>` :表示日期。

本质上新语义与`<div>`和`<span>`没有区别，只是更具识别度和表意性。使用时除了在HTML结构上需要注意外，`<dis class="nav">`相当于`<nav>`。



##### 新语义标签的兼容性处理：

​	IE8 及以下版本的浏览器不支持 H5 和 CSS3。解决办法：引入`html5shiv.js`文件。

引入时，需要做if判断，具体代码如下：

```html
<!--  条件注释 只有ie能够识别-->

    <!--[if lte ie 8]>
        <script src="html5shiv.min.js"></script>
    <![endif]-->
```

上方代码是**条件注释**：虽然是注释，但是IE浏览器可以识别出来。解释一下：

- l：less 更小
- t：than 比
- e：equal等于
- g：great 更大

PS:我们在测试 IE 浏览器的兼容的时候，可以使用软件 ietest，模拟IE6-IE11。

在不支持HTML5新标签的浏览器，会将这些新的标签解析成行内元素(inline)对待，所以我们只需要将其转换成块元素(block)即可使用。

在实际开发中我们更多采用的办法是：检测IE浏览器的版本，来加载第三方的JS库来解决兼容问题。



##### HTML5中的表单：

- `email` 只能输入email格式。自动带有验证功能。
- `tel` 手机号码。
- `url` 只能输入url格式。
- `number` 只能输入数字。
- `search` 搜索框
- `range` 滑动条
- `color` 拾色器
- `time` 时间
- `date` 日期
- `datetime` 时间日期
- `month` 月份
- `week` 星期

上面的部分类型是针对移动设备生效的，且具有一定的兼容性，在实际应用当中可选择性的使用。

```html
        input {
            width: 100%;
            height: 25px;
            margin-top: 2px;
            display: block;
        }

    </style>
</head>
<body>
<form action="">
    <fieldset>
        <legend>表单类型</legend>
        <label for="">
            email: <input type="email" name="email" required>
        </label>
        <label for="">
            color: <input type="color" name="color">
        </label>
        <label for="">
            url: <input type="url" name='url'>
        </label>
        <label for="">
            number: <input type="number" step="3" name="number">
        </label>
        <label for="">
            range: <input type="range" name="range" value="100">
        </label>
        <label for="">
            search: <input type="search" name="search">
        </label>
        <label for="">
            tel: <input type="tel" name="tel">
        </label>
        <label for="">
            time: <input type="time" name="time">
        </label>
        <label for="">
            date: <input type="date" name="date">
        </label>
        <label for="">
            datetime: <input type="datetime">
        </label>
        <label for="">
            week: <input type="week" name="month">
        </label>
        <label for="">
            month: <input type="month" name="month">
        </label>
        <label for="">
            datetime-local: <input type="datetime-local" name="datetime-local">
        </label>
        <input type="submit">
    </fieldset>
</form>
</body>
</html>
```

代码解释：

`<fieldset>` 标签将表单里的内容进行打包，代表一组；而`<legend> `标签的则是 fieldset 里的元素定义标题。



##### 表单元素(标签)：

1.`<datalist>`数据列表：

```html
<input type="text" list="myData">
<datalist id="myData">
	<option>本科生</option>
	<option>研究生</option>
	<option>不明</option>
</datalist>
```

上述代码将input 的list属性和`datalist `绑定，这样数据列表会自动提示

![1621496156468](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621496156468.png)

2.`<keygen>`元素：

​	keygen 元素的作用是提供一种验证用户的可靠方法。

​	keygen 元素是密钥对生成器（key-pair generator）。当提交表单时，会生成两个键：一个公钥，一个私钥。

​	私钥（private key）存储于客户端，公钥（public key）则被发送到服务器。公钥可用于之后验证用户的客户端证书（client certificate）。



3、`<meter>`元素：度量器

- low：低于该值后警告
- high：高于该值后警告
- value：当前值
- max：最大值
- min：最小值。

```html
<meter  value="81"    min="0" max="100"  low="60"  high="80"/>
```

![1621496521682](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621496521682.png)



##### 表单属性：

- `placeholder` 占位符（提示文字）
- `autofocus` 自动获取焦点
- `multiple` 文件上传多选或多个邮箱地址
- `autocomplete` 自动完成（填充的）。on 开启（默认），off 取消。用于表单元素，也可用于表单自身(on/off)
- `form` 指定表单项属于哪个form，处理复杂表单时会需要
- `novalidate` 关闭默认的验证功能（只能加给form）
- `required` 表示必填项
- `pattern` 自定义正则，验证表单

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <style>
        form {
            width: 100%;
            /* 最大宽度*/
            max-width: 640px;
            /* 最小宽度*/
            min-width: 320px;
            margin: 0 auto;
            font-family: "Microsoft Yahei";
            font-size: 20px;
        }

        input {
            display: block;
            width: 100%;
            height: 30px;
            margin: 10px 0;
        }
    </style>
</head>
<body>

<form action="">
    <fieldset>
        <legend>表单属性</legend>
        <label for="">
            用户名：<input type="text" placeholder="例如：smyhvae" autofocus name="userName" autocomplete="on" required/>
        </label>

        <label for="">
            电话：<input type="tel" pattern="1\d{10}"/>
        </label>

        <label for="">
            multiple的表单: <input type="file" multiple>
        </label>

        <!-- 上传文件-->
        <input type="file" name="file" multiple/>

        <input type="submit"/>
    </fieldset>
</form>

</body>
</html>
```

![1621498433350](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621498433350.png)



##### 表单事件：

- `oninput()`:用户输入内容时触发，可用于输入字数统计。
- `oninvalid()`:验证不通过时候触发。如果验证不通过，可以弹出一段提示文字。

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <style>
        form {
            width: 100%;
            /* 最大宽度*/
            max-width: 400px;
            /* 最小宽度*/
            min-width: 200px;
            margin: 0 auto;
            font-family: "Microsoft Yahei";
            font-size: 20px;
        }

        input {
            display: block;
            width: 100%;
            height: 30px;
            margin: 10px 0;
        }
    </style>
</head>
<body>
<form action="">
    <fieldset>
        <legend>表单事件</legend>
        <label for="">
            邮箱：<input type="email" name="" id="txt1"/>
        </label>
        <label for="">
            输入的次数统计：<input type="text" name="" id="txt2"/>
        </label>

        <input type="submit"/>
    </fieldset>
</form>
<script>

    var txt1 = document.getElementById('txt1');
    var txt2 = document.getElementById('txt2');
    var num = 0;

    txt1.oninput = function () {  //用户输入时触发

        num++;  //用户每输入一次，num自动加 1
        //将统计数显示在txt2中
        txt2.value = num;
    }
    txt1.oninvalid = function () {  //验证不通过时触发
        this.setCustomValidity('亲，请输入正确哦');  //设置验证不通过时的提示文字
    }

</script>
</body>
</html>
```

![1621499558260](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1621499558260.png)



##### 多媒体：

H5里面提供了视频和音频的标签。

（1）音频：HTML5通过`<audio>`标签来解决音频播放的问题。

```html
<audio src="music/yinyue.mp3" autoplay controls></audio>
```

可以通过附加属性，来更好的控制音频的播放，如：

- `autoplay` :自动播放。写成`autoplay`或者`autoplay=" "` 

- `controls` ：控制条  （建议写上，要不然看不到控件在哪里）

- `loop` ：循环播放。

- `preload` ：预加载同时设置`autoplay `时此属性将失效。

  

处理兼容性问题：

为了做到多浏览器支持，可以采取以下兼容写法：

```html
<!--推荐的兼容写法-->
<audio controls loop>
	<source src="music/yinyue.mp3" />
	<source src="music/yinyue.ogg" />
	<source src="music/yinyue.wav" />
	抱歉，你的浏览器暂不支持此音频格式。
</audio>
```

如果识别不出音频格式，就弹出来那句”抱歉“。



（2）视频：H5通过`<video>`标签来解决视频播放的问题。

```html
<video src="video/moive.mp4" controls autoplay></video>
```

通过附加属性，来控制视频的播放，如：

- `autoplay` 自动播放。写成`autoplay` 或者 `autoplay = ""`，都可以。
- `controls` 控制条。（建议把这个选项写上，不然都看不到控件在哪里）
- `loop` 循环播放。
- `preload` 预加载 同时设置 autoplay 时，此属性将失效。
- `width`：设置播放窗口宽度。
- `height`：设置播放窗口的高度。



由于版权等原因，不同的浏览器可支持播放的格式不一样，兼容性写法：

```html
 <!--<video src="video/movie.mp4" controls  autoplay ></video>-->
    <!--  行内块 display:inline-block -->
    <video controls autoplay>
        <source src="video/movie.mp4"/>
        <source src="video/movie.ogg"/>
        <source src="video/movie.webm"/>
        抱歉，不支持此视频
    </video>
```



DOM操作：

（1）获取元素：

- `document.querySelector("selector")` :通过CSS选择器获取符合条件的第一个元素。
- `document.querySelectorAll("selector")`:通过CSS选择器获取符合条件的所有元素，以类数组的形式存在。



（2）类名操作：

- `Node.classList.add("class")` :添加class
- `Node.classList.remove("class")` :移除class
- `Node.classList.toggle("class")` :切换class，有则删除，无则添加。
- `Node.classList.contains("class")` :检查是否存在class



##### 自定义属性：

js 里可以通过 `box1.index=100;` `box1.title` 来自定义属性和获取属性。

H5可以直接在标签里添加自定义属性，**但必须以 data- 开头**。

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
</head>
<body>
<!-- 给标签添加自定义属性 必须以data-开头 -->
<div class="box" title="盒子" data-my-name="smyhvae" data-content="我是一个div">div</div>
<script>
    var box = document.querySelector('.box');

    //自定义的属性 需要通过 dateset[]方式来获取
    console.log(box.dataset["content"]);  //打印结果：我是一个div
    console.log(box.dataset["myName"]);    //打印结果：smyhvae

    //设置自定义属性的值
    var num = 100;
    num.index = 10;
    box.index = 100;
    box.dataset["content"] = "aaaa";

</script>
</body>
</html>
```



##### 拖拽：

​	拖拽网站里的图片和超链接，在H5的规范中，可以通过为元素增加`<draggable="true">`来设置此元素是否可以进行拖拽操作，其中图片，链接默认是开启拖拽的。

（1）拖拽元素：在页面中设置了`<draggable="true">`属性的元素。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="stylesheet" href="css/font-awesome.min.css">
    <style>
    .box1{
        width: 200px;
        height: 200px;
        background-color: green;

    }
    </style>
</head>
<body>
    <!--给 box1 增加拖拽的属性-->
    <div class="box1" draggable="true"></div>
</body>
</html>
```



##### （2）拖拽元素的事件监听：（应用于拖拽元素）

- `ondragstart` :当拖拽开始时调用。
- `ondragleave` :当鼠标离开拖拽元素时调用。
- `ondragend` :当拖拽结束时调用。
- `ondrag`  :整个拖拽过程都会调用。

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <style>
        .box {
            width: 200px;
            height: 200px;
            background-color: green;
        }
    </style>
</head>
<body>
<div class="box" draggable="true"></div>

<script>
    var box = document.querySelector('.box');

    //  绑定拖拽事件

    //  拖拽开始
    box.ondragstart = function () {
        console.log('拖拽开始.');
    }

    //  拖拽离开：鼠标拖拽时离开被拖拽的元素时触发
    box.ondragleave = function () {
        console.log('拖拽离开..');
    }

    //  拖拽结束
    box.ondragend = function () {
        console.log('拖拽结束...');
        console.log("---------------");
    }

    box.ondrag = function () {
        console.log('拖拽');
    }

</script>
</body>
</html>
```

![1625794189102](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1625794189102.png)





##### 2.目标元素：

如果想把元素A拖拽到元素B，那么元素B就是目标元素。页面中任何一个元素都可以成为目标元素。页面中任何一个元素都可以成为目标元素。



##### 目标元素的事件监听：（应用于目标元素）

- `ondragenter` ：当拖拽元素进入时调用。
- `ondragover` : 当拖拽元素停留在目标元素上，就会连续一直触发（不管拖拽元素此时是移动还是不动的状态。）
- `ondrop` ：当在目标元素上松开鼠标时调用。
- `ondragleave` ：当鼠标离开目标元素时调用。

代码：

```html
<!DOCTYPE html>
<html lang="en">
    <meta charset="UTF-8">
    <title></title>
   <head>

    <style>
    	   .one {
            width: 100px;
            height: 100px;
            border: 1px solid #000;
            background-color: green;
        }

        .two {
            position: relative;
            width: 200px;
            height: 200px;
            left: 300px;
            top: 100px;
            border: 1px solid #000;
            background-color: red;
        }
    </style>
                
   </head>
    <body>
        <div class="one" draggable="true">
            
        </div>
        <div class="two"> </div>           
		
        <script>
        	var two = document.querySelector('.two').
            //目标元素的拖拽事件
            
            //当被拖拽元素进入时触发
            two.ondragenter = function(){
                console.log("来了");
            }
            
            //当被拖拽元素离开时触发
            two.ondragleave = function(){
                console.log("走了");
            }
            
            // 当拖拽元素在 目标元素上时，连续触发
   			 two.ondragover = function (e) {
        //阻止拖拽事件的默认行为
       		 e.preventDefault(); //【重要】一定要加这一行代码，否则，后面的方法 ondrop() 无法触发。

        	console.log("over...");
    }

    // 当在目标元素上松开鼠标是触发
    two.ondrop = function () {
        console.log("松开鼠标了....");
    }
        </script>
    </body>
</html>
```

![1625795375675](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1625795375675.png)

注意，上方代码中，我们加了`event.preventDefault()`这个方法。如果没有这个方法，后面`ondrop()`方法无法触发。如下图所示：

![1625795404333](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1625795404333.png)



如上图所示，连光标的形状都提示我们，无法在目标元素里继续操作了。

**总结**：如果想让拖拽元素在目标元素里做点事情，就必须要在 `ondragover()` 里加`event.preventDefault()`这一行代码。



##### 案例：拖拽练习

```html
<!DOCTYPE html>
<html>
<head lang="en">
    <meta charset="UTF-8">
    <title></title>
    <style>
        .one {
            width: 400px;
            height: 400px;
            border: 1px solid #000;
        }

        .one > div, .two > div {
            width: 98px;
            height: 98px;
            border: 1px solid #000;
            border-radius: 50%;
            background-color: red;
            float: left;
            text-align: center;
            line-height: 98px;
        }

        .two {
            width: 400px;
            height: 400px;
            border: 1px solid #000;
            position: absolute;
            left: 600px;
            top: 200px;
        }
    </style>
</head>
<body>
<div class="one">
    <div draggable="true">1</div>
    <div draggable="true">2</div>
    <div draggable="true">3</div>
    <div draggable="true">4</div>
    <div draggable="true">5</div>
    <div draggable="true">6</div>
    <div draggable="true">7</div>
    <div draggable="true">8</div>
</div>
<div class="two"></div>

<script>
    var boxs = document.querySelectorAll('.one div');
    //        临时的盒子 用于存放当前拖拽的元素

    var two = document.querySelector('.two');

    var temp = null;
    //         给8个小盒子分别绑定拖拽事件
    for (var i = 0; i < boxs.length; i++) {
        boxs[i].ondragstart = function () {
//                保持当前拖拽的元素
            temp = this;
            console.log(temp);
        }

        boxs[i].ondragend = function () {
//               当拖拽结束 ，清空temp
            temp = null;
            console.log(temp);
        }
    }

    //        目标元素的拖拽事件
    	two.ondragover = function (e) {
//            阻止拖拽的默认行为
        	e.preventDefault();
    	}
    //        当在目标元素上松开鼠标是触发
    	two.ondrop = function () {
//            将拖拽的元素追加到 two里面来
        	this.appendChild(temp);
    }
</script>
</body>
</html>
```

效果如下：

![1625796928772](C:\Users\hp\AppData\Roaming\Typora\typora-user-images\1625796928772.png)





##### 历史：

界面上的所有JS操作不会被浏览器记住，就无法回到之前的状态。

在HTML5中可以通过`window.history` 操作访问历史状态，让一个页面可以有多个历史状态。

`window.history` 对象可以让我们管理历史记录，可用于单页面应用，可以无刷新改变网页内容。

- `window.history.forward();`   // 前进

- `window.history.back();` //后退

- `window.history.go();` //刷新

- `window.history.go(n);` 

  - n=1  ： 表示前进。
  - n= -1 :   表示后退。
  - n = 0 :    表示刷新。
  - 如果移动的位置超出了访问历史的边界，会静默失败，但不会报错。

- 通过JS可以加入一个访问状态。

- `history.pushState;`  //放入历史中的状态数据，设置title（现在浏览器不支持改变历史状态）

   

- html 的常见元素
- html 元素的分类
- html 元素的嵌套关系
- html 元素的默认样式和 CSS Reset
- html 常见面试题



##### html 的常见元素

html 的常见元素主要分为两类：head 区域的元素、body 区域的元素。下面来分别介绍。

##### 1、head 区域的 html 元素

> head 区域的 html 元素，不会在页面上留下直接的内容。

- meta
- title
- style
- link
- script
- base

**base元素的介绍**：

```
<base href="/">
```

base 标签用于指定基础的路径。指定之后，所有的 a 链接都是以这个路径为基准。



##### 2、html 元素（body 区域）

> body 区域的 html 元素，会直接出现在页面上。

- div、section、article、aside、header、footer
- p
- span、em、strong
- 表格元素：table、thead、tbody、tr、td
- 列表元素：ul、ol、dl、dt、dd
- a
- 表单元素：form、input、select、textarea、button

div 是最常见的元素，大多数场景下，都可以用div（实在不行就多包几层div）。可见，**div 是比较通用的元素，这也决定了 div 的的语义并不是很明确**。

**常见标签的重要属性**：

- a[href,target]
- img[src,alt]
- table td[colspan,rowspan]。设置当前单元格占据几行几列。在合并单元格时，会用到。
- form[target,method,enctype]
- input[type,value]
- button[type]
- selection>option[value]
- label[for]



##### html 文档的大纲

我们平时在写论文或者其他文档的时候，一般会先列出大纲，然后再写具体的内容。

同样，html 网页也可以看成是一种文档，也有属于它的大纲。

一个常见的html文档，它的结构可以是：

```html
    <section>
        <h1>一级标题</h1>

        <section>
            <h2>二级标题</h2>
            <p>段落内容</p>
        </section>

        <section>
            <h2>二级标题</h2>
            <p>段落内容</p>
        </section>

        <aside>
            <p>广告内容</p>
        </aside>

    </section>

    <footer>
        <p>某某公司出品</p>
    </footer>
```





##### 查看网页大纲的工具:

我们可以通过 <http://h5o.github.io/> 这个工具查看一个网页的大纲。

**使用方法**：

（1）将网址 <http://h5o.github.io/> 保存到书签栏

（2）去目标网页，点击书签栏的网址，即可查看该网页的大纲。

这个工具非常好用，既可以查看网页的大纲，也可以查看 markdown 在线文档的结构。





##### html 元素的分类:

按照样式分类：

- 块级元素
- 行内元素
- inline-block：比如`form`表单元素。对外的表现是行内元素（不会独占一行），对内的表现是块级元素（可以设置宽高）。

按照内容分类：

[![img](https://camo.githubusercontent.com/7effc74f77aa44a41d879cf662788d7eb96df64ab1e06adb06417618efb29d38/687474703a2f2f696d672e736d79687661652e636f6d2f32303139313030335f313934362e706e67)](https://camo.githubusercontent.com/7effc74f77aa44a41d879cf662788d7eb96df64ab1e06adb06417618efb29d38/687474703a2f2f696d672e736d79687661652e636f6d2f32303139313030335f313934362e706e67)

图片来源：<https://html.spec.whatwg.org/multipage/dom.html#kinds-of-content>





##### html 元素的嵌套关系:

- 块级元素可以包含行内元素。
- 块级元素**不一定**能包含块级元素。比如 div 中可以包含 div，但 p 标签中不能包含 div。
- 行内元素**一般**不能包含块级元素。比如 span 中不能包含 div。但有个特例：在 HTML5 中， a 标签中可以包含 div。

**注意**：在 HTML5 中 `a > div` 是合法的， `div > a > div`是不合法的 ；但是在 html 4.0.1 中， `a > div` 仍然是不合法的。



##### html 元素的默认样式和 CSS Reset:

比如下拉框这种比较复杂的元素，是自带默认样式的。如果没有这个默认样式，则该元素在页面上不会有任何表现，则必然增加一些工作量。

同时，默认样式也会带来一些问题：比如，有些默认样式我们是不需要的；有些默认样式甚至无法去掉。

如果我们不需要默认的样式，这里就需要引入一个概念：**CSS Reset**。



##### 常见的 CSS Reset 方案

**方案一**：

CSS Tools: Reset CSS。链接：<https://meyerweb.com/eric/tools/css/reset/>

**方案二**：

雅虎的 CSS Reset。链接：<https://yuilibrary.com/yui/docs/cssreset/>

我们可以直接通过 CDN 的方式引入：

```
<link rel="stylesheet" type="text/css" href="http://yui.yahooapis.com/3.18.1/build/cssreset/cssreset-min.css">
```

**方式三**：（比较有争议）

```
*{
    margin: 0;
    padding: 0;
}
```

上面何种写法，比较简洁，但也有争议。有争议的地方在于，可能会导致 css 选择器的性能问题。





##### Normalize.css

上面的几种 css reset 的解决思路是：将所有的默认样式清零。

但是，[Normalize.css](https://necolas.github.io/normalize.css/) 的思路是：既然浏览器提供了这些默认样式，那它就是有意义的。**既然不同浏览器的默认样式不一致，那么，Normalize.css就将这些默认样式设置为一致**。





##### html 常见面试题

##### doctype 的意义是什么:

- 让浏览器以标准模式渲染
- 让浏览器知道元素的合法性



##### HTML、XHTML、HTML5的区别:

- HTML 属于 SGML
- XHTML 属于 XML，是 HTML 进行 XML 严格化的结果
- HTML5 不属于SGML，也不属于 XML（HTML5有自己独立的一套规范），比 XHTML 宽松。



##### HTML5 有什么新的变化

- 新的语义化元素
- 表单增强
- 新的API：离线、音视频、图形、实时通信、本地存储、设备能力等。



##### `em `和 `i `的区别

共同点：二者都是表示斜体。

区别：

- em 是语义化的标签，表示强调。
- i 是纯样式的标签，表示斜体。HTML5 中不推荐使用。



##### 语义化的意义是什么:

- 开发者容易理解，便于维护。
- 机器（搜索引擎、读屏软件等）容易理解结构
- 有助于 SEO



##### 哪些元素可以自闭和:

> 自闭和的元素中不能再嵌入别的元素。且 HTML5 中要求加斜杠。

- 表单元素 input
- 图片 img
- br、hr
- meta、link



##### form 表单的作用:

- 直接提交表单
- 使用 submit / reset 按钮
- 便于浏览器保存表单
- 第三方库（比如 jQuery）可以整体获取值
- 第三方库可以进行表单验证

所以，如果我们是通过 Ajax 提交表单数据，也建议加上 form。





##### HTML5新元素：

`<canvas>` 标签 ： 定义图形，比如图表和其他图像。该标签基于JavaScript的绘图API。



















































































