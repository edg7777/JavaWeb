# JavaWeb笔记

## 1.HTML

#### 1.1HTML文件书写规范和整体框架解析 

```html
<!DOCTYPE html>     
<html lang="en">				表示整个html页面的开始，lang="zh_CN"表示中文
<head>							头信息
    <meta charset="UTF-8">		设置字符集为"UTF-8"
    <title>标题</title>			标题
</head>							
<body>							页面的主题内容
    helloworld					页面的具体内容(自己的代码)
</body>							
</html>							整个html页面的结束


html的注释:<!--  注释  -->
```

#### 1.2html标签的介绍

##### 1.2.1标签的格式：

<标签名>封装的数据</标签名>  带/的为结束标签

##### 1.2.2标签名大小写不敏感

##### 1.2.3标签拥有自己的属性

###### 		1.2.3.1分为基本属性：bgcolor=“red” 可以修改简单的样式效果

###### 		1.2.3.2事件属性οnclick=“alert(‘你好！’);” 可以直接设置事件响应后的代码。

##### 1.2.4标签又分为，单标签和双标签

###### 		1.2.4.1单标签格式：<标签名 />

###### 		1.2.4.2双标签格式：<标签名>…封装数据…<标签名/>

#### 1.3标签的正确语法

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>0-标签语法.html</title>
</head>
<body>
	<!--标签不能交叉嵌套-->
	正确：<div><span>早安，尚硅谷</span></div>
	错误：<div><span>早安，尚硅谷</div></span>
	<hr/> hr为水平线
	<!--标签必须正确关闭(闭合)-->
	<!--1、有文本内容的标签-->
	正确：<div>早安，尚硅谷</div>
	错误：<div>早安，尚硅谷
	<hr/>
	<!--2、没有文本内容的标签-->
	正确：<br/>  br为换行
	错误：<br>
	<hr/>
	<!--属性必须有值，属性值必须加引号-->
	正确：<font color="#00bfff">早安，尚硅谷</font>
	错误：<font color=#00bfff>早安，尚硅谷</font>
	错误：<font color>早安，尚硅谷</font>
	<hr/>
    <!--注释不能嵌套-->
    正确：<!--注释内容--><br/>
    错误：<!--注释内容<!--注释内容-->-->
</body>
</html>

```

#### 1.4常用标签介绍

#### 1.4.1font字体标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>  <!--在网页上显示我是字体标签，字体为宋体颜色为红色-->
<font color="red" face="宋体" size="7">我是字体标签</font>   color修改字体颜色，face修改字体，size修改字体大小
</body>
</html>
```

#### 1.4.2特殊字符

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
我是&lt;br&gt;标签  如果想在页面中展示< 或者 >,要使用&lt;代表<，使用&gt;代表 >,浏览器总是会截短 HTML 页面中的空格。如果您在文本中写 10 个空格，在显					示该页面之前，浏览器会删除它们中的 9 个。如需在页面中增加空格的数量，您需要使用 &nbsp;
</body>
</html>
```

#### 1.4.3标题标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>3-标题标签</title>
</head>
<body>
<!--标签标题
    需求1：演示标题1到标题6的
    h1-h6都是标题标签
    h1 最大
    h6 最小
    align：属性是对其属性
    left     左对齐：默认
    right    右对齐
    center   居中           
-->
<h1 align="left">标题1</h1>
<h2 align="center">标题2</h2>
<h3 align="right">标题3</h3>
<h4>标题4</h4>
<h5>标题5</h5>
<h6>标题6</h6>
</body>
</html>

```

#### 1.4.4超链接

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>4-超链接</title>
</head>
<body>
<!--a标签是：超链接
        href属性设置链接的地址
        target属性设置那个目标进行跳转
            _self        表示当前页面（默认）
            _blank       表示打开新页面来进行跳转
-->
<a href="http://www.baidu.com">百度</a>
<a href="http://www.baidu.com" target="_self">百度</a>
<a href="http://www.baidu.com" target="_blank">百度</a>
</body>
</html>

```

#### 1.4.5列表标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<!--ul表示无序，ol表示有序，无序和有序的区别仅在于有序前面多了数值
type属性可以修改数据前面的符号-->
<body>
    <ol>
        <li type="none">jiejie</li>
        <li>meiko</li>
        <li>Fofo</li>
        <li>leave</li>
        <li>Ale</li>
    </ol>
</body>
</html>
```

#### 1.4.6img标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Family Guy</title>
</head>
    <!--
    img标签是图片标签，用来显示图片
        src属性可以设置图片的路径
        width属性可以设置图片的宽度
        height属性可以设置图片的高度
        border属性可以设置图片的边框大小
        alt属性设置当指定路径找不到图片时，用来替代显示的文本内容
     在web中路径分为相对路径和绝对路径两种
        相对路径：
            .          表示当前文件坐在的目录
            ..         表示当前文件所在的上一级目录
            文件名       表示当前文件所在目录的文件，相当于  ./文件名    ./可以省略

        绝对路径：
            正确格式是：http://ip:prot/工程名/资源路径
            错误格式是：盘符:/目录/文件名
--> 
<body>
    <img src="../imag/Snipaste_2023-04-02_11-54-36.png" width="300" height="300" border="20" alt="所找的图片不存在" />
</body>
</html>
```

####  1.4.7表格标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Family Guy</title>
</head>
        <!--table为表格标签  align可以调整表格位置居中居左居右
            tr为行标签
            td为列标签
            th为表头标签，即加粗又居中
            b为加粗标签
            cellspacing为单元格间距
            -->
<body>
    <table align="center" border="1" width="400" height="400" cellspacing="10">
        <tr>
            <th>1.1</th>
            <th>1.2</th>
            <th>1.3</th>
        </tr>
        <tr>
            <td>2.1</td>
            <td>2.2</td>
            <td>2.3</td>
        </tr>
        <tr>
            <td>3.1</td>
            <td>3.2</td>
            <td>3.3</td>
        </tr>
    </table>
</body>
</html>
```

#### 1.4.8跨行跨列表格

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<!--
 colspan属性设置跨列 col为列
 rowspan属性设置跨行 row为行
 跨列或者跨行之后要把所跨的列和行删掉
需求：第一行一列跨2列
      第2行1列跨2行
      第4行4列跨2行2列

 -->
<body>
    <table border="1" width="500" height="500" cellspacing="0">
        <tr>
            <th colspan="2">1.1</th>
            <th>1.3</th>
            <th>1.4</th>
            <th>1.5</th>
        </tr>
        <tr>
            <td rowspan="2">2.1</td>
            <td>2.2</td>
            <td>2.3</td>
            <td>2.4</td>
            <td>2.5</td>
        </tr>
        <tr>
            <td>3.2</td>
            <td>3.3</td>
            <td>3.4</td>
            <td>3.5</td>
        </tr>
        <tr>
            <td>4.1</td>
            <td>4.2</td>
            <td>4.3</td>
            <td rowspan="2" colspan="2">4.4</td>
        </tr>
        <tr>
            <td>5.1</td>
            <td>5.2</td>
            <td>5.3</td>
        </tr>
    </table>
</body>
</html>
```

#### 1.4.9iframe框架标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<!--
iframe标签可以在页面上面开辟一个小区域显示一个单独的页面
iframe和a标签使用步骤:
        1.在iframe标签中用name属性定义一个名称
        2.令a标签中的target属性等于iframe标签中name属性的值

 -->
<body>
    <iframe src="imag标签.html" width="500" height="500" name="if"></iframe>
    <ol>
        <li><a href="font标签.html" target="if">font标签.html</a></li>
        <li><a href="helloworld.html" target="if">helloworld.html</a></li>
    </ol>

</body>
</html>
```

#### 1.4.10表单标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<!--form表示表单标签,input是最重要的表单元素
    <input> 元素有很多形态，根据不同的 type 属性。
    <input type="text"> 定义用于文本输入的单行输入字段.
    <input type="radio"> 定义单选按钮。
    <input type="submit"> 定义用于向表单处理程序（form-handler）提交表单的按钮。
    <input type="reset"> 定义用于向表单处理程序（form-handler）重置表单的按钮。
    <select> 元素定义下拉列表：
      <option> 元素定义待选择的选项
    <textarea> 元素定义多行输入字段（文本域）
    <button> 元素定义可点击的按钮
    value 属性规定输入字段的初始值
    表单格式化可以创建一个表格来完成，使表单更加工整


    action 属性定义在提交表单时执行的动作
    method 属性规定在提交表单时所用的 HTTP 方法（GET 或 POST）

    您能够使用 GET（默认方法）：
    如果表单提交是被动的（比如搜索引擎查询），并且没有敏感信息。
    当您使用 GET 时，表单数据在页面地址栏中是可见的
    使用get方法就要给每个属性设置name值，name

    您应该使用 POST：
    如果表单正在更新数据，或者包含敏感信息（例如密码）。
    POST 的安全性更好，因为在页面地址栏中被提交的数据是不可见的。

    表单的target属性默认为_blank，即另起一个页面，这里将其修改为_self
-->
<body>
  <form action="www.baidu.com" method="get" target="_self">
    <h1 align="center">用户注册</h1>
    <table align="center">
      <tr>
        <td>用户名称:</td>
        <td><input type="text" value="default" name="username"/></td>
      </tr>
      <tr>
        <td>用户密码:</td>
        <td><input type="password" value="abc"/></td>
      </tr>
      <tr>
        <td>确认密码:</td>
        <td><input type="password" value="abc"/></td>
      </tr>
      <tr>
        <td>性别:</td>
        <td>
          <input type="radio" name="sex" checked="checked" value="man"/>男
          <input type="radio" name="sex" value="woman"/>女
        </td>
      </tr>
      <tr>
        <td>兴趣爱好:</td>
        <td>
          <input type="checkbox" checked="checked"/>Java
          <input type="checkbox" name="hobby" value="c语言"/> c语言
          <input type="checkbox"/> c++
        </td>
      </tr>
      <tr>
        <td>国籍:</td>
        <td>
          <select>
            <option>---请选择你的国籍---</option>
            <option selected="selected">China</option>
            <option>America</option>
            <option>Britain</option>
            <option>Japan</option>
          </select><br/>
        </td>
      </tr>
      <tr>
        <td>自我评价:</td>
        <td><textarea rows="20" cols="20">默认值</textarea><br/></td>
      </tr>
      <tr>
        <td><input type="reset" value="重置"/></td>
        <td><input type="button" value="点击保存"/></td>
        <td><input type="submit" value="提交"/></td>
        <td><button>点击保存</button></td>
      </tr>
    </table>
  </form>
</body>
</html>
```

#### 1.4.11其它标签(div,span,p)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<!--p标签：
    注释：浏览器会自动地在段落的前后添加空行。（<p> 是块级元素）
    提示：使用空的段落标记 <p></p> 去插入一个空行是个坏习惯。用 <br /> 标签代替它！
    
    div标签默认独占一行
    span标签的长度为封装数据的长度


 -->
<body>
    <div>我是div标签</div>
    <div>我是div标签</div>
    <span>我是span标签</span>
    <span>我是span标签</span>
    <p>我是段落标签</p>
    <p>我是段落标签</p>

</body>
</html>
```

## 2.CSS技术

#### 2.1CSS技术介绍

CSS是层叠样式表单。是用于控制网页样式并允许将样式信息与网页内容分离的一种标志性语言

#### 2.2CSS的语法规则

选择器：浏览器根据"选择器"决定CSS样式影响的HTML元素（标签）

属性：是你要改变的样式名，并且每个属性都有一个值。属性和值被冒号分开，并由花括号包围，这样就组成了一个完整的声明，例如：p{color:bule}

多个声明：如果要定义不止一个声明，则需要用分号将声明分开。虽然最后一条声明的最后可以不用加分号（但尽量在每条声明的末尾都加上分号）

例如：

p{

color:red;

font-size:30px;

}

一般每行只描述一个属性

CSS：注释：/**/

#### 2.3CSS和HTML的结合方式

##### 2.3.1第一种方式：

在标签的style属性上设置"key:value value;"，修改标签样式(缺点明显)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<!--
   分别定义两个div和span标签，分别修改每个div标签的样式为：边框1个像素，实线，红色
 -->
<body>
    <div style="border: solid 1px red">我是div标签</div>
    <div style="border: solid 1px red">我是div标签</div>
    <span>我是span标签</span>
    <span>我是span标签</span>
</body>
</html>
```

##### 2.3.2第二种方式：

在head标签中，使用style标签来定义各种自己需要的css样式

格式如下：xxx为要定义的标签

xxx{

 key : value value;

}

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>   style里面的注释要用CSS注释来写--/*  */
        div{
            border: 1px red solid;
        }
        span{
            border: 2px green dashed;
        }
        p{
            border: 10px blue groove;
        }
    </style>
</head>
<!--
   分别定义两个div和span标签，分别修改每个div标签的样式为：边框1个像素，实线，红色
 -->
<body>
    <div>我是div标签</div>
    <span>我是span标签</span>
    <p>我是段落标签</p>
</body>
</html>
```

缺点：1.只能在一个页面复用代码，不能在多个页面复用

​				2.维护起来不方便

##### 2.3.3第三种方式

把CSS样式写成一个单独的CSS文件，再通过link标签引入

CSS文件

```css
div{
    border: aliceblue solid 5px;
}

span{
    border: black solid 5px;
}

p{
    border: aliceblue solid 5px;
}
```

html文件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="stylesheet" type="text/css" href="divstyle.css"/> 使用link标签引入
</head>
<!--
   分别定义两个div和span标签，分别修改每个div标签的样式为：边框1个像素，实线，红色
 -->
<body>
    <div>我是div标签</div>
    <span>我是span标签</span>
    <p>我是段落标签</p>
</body>
</html>
```

#### 2.4CSS选择器

##### 2.4.1标签名选择器

标签名选择器和上述一样

标签名{

​	属性：值

}

同上，不再插入代码块

##### 2.4.2id选择器

id选择器的格式是:

#id 属性值{

​		属性：值

}

id选择器可以让我们通过id属性选择性的使用这个样式，比如我在一个项目中要写很多个div样式或者span样式，我不用创建很多个css文件来逐个存储这些样式，可以只写一个文件通过id选择器来选择不同的样式

css文件

```css
#id001{
    color: blue;
    font-size: 30px;
    border: 1px yellow solid ;
}

#id002{
    color:red;
    font-size: 20px;
    border: 5px blue dotted;
}
```

html文件

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="stylesheet" type="text/css" href="divstyle.css"/>
</head>

<body>
    <div id="id001">我是调用id001的标签</div>
    <div id="id002">我是调用id002的标签</div>
    <span id="id001">我是调用id002的span标签</span>

</body>
</html>
```

##### 2.4.3class选择器(类选择器)

格式：

.class{

属性：值

}

class类选择器，可以通过class属性有效的选择性的去使用样式，学完class选择器之后我第一时间其实不知道和id选择器的区别，因为在上个html文件中我id选择器使用了两次而且能够正常运行(虽然idea会报错但是能够跑起来)，然后就去网上搜了一下

class与id选择器的区别为：id选择器在一个html文档中只能使用一次，而class选择器可以使用多次，但是在上面的代码中id使用多次一样能正常运行(虽然idea会有红线)，在idea中一个html文档使用多次class选择器则不会报错

css文档

```css
.class01{
    color:blue;
    font-size: 30px;
    border:yellow 1px solid;

}

.class02{
    color:grey;
    font-size: 26px;
    border: 1px red solid;
    
}
```

html文档

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="stylesheet" type="text/css" href="divstyle.css"/>
</head>

<body>
    <div class="class01">我是调用class01的div标签</div>
    <div class="class02">我是调用class02的div标签</div>
    <span class="class01">我是调用class01的span标签</span>
</body>
</html>
```

##### 2.4.4组合选择器

格式：

选择器1，选择器2，选择器n{

属性：值

}

组合选择器可以让多个选择器共用一个css样式代码

```css
.class01,#id01{
    color: blue;
    font-size: 30px;
    border:yellow 2px solid;
}
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="stylesheet" type="text/css" href="divstyle.css"/>
</head>

<body>
    <div class="class01">我是调用class01的div标签</div>
    <div id="id01">我是调用组合选择器中id01选择器的div标签</div>
</body>
</html>
```

#### 2.5CSS常用样式

##### 1.字体颜色:

color

##### 2.宽度

width:

##### 3.高度

height:

##### 4.背景颜色

background:

##### 5.字体样式:

font-size

##### 6.div居中：

margin-left:auto;

matgin-right:auto;

##### 7.边框:

border

##### 8.文本居中：

text-align:center

##### 9.超链接去下划线：

text-decoration:none

##### 10.表格细线:

border: 1px black solid;/设置边框/
border-collapse: collapse;/将边框合并/

##### 11.ul无序列表去除符号:

list-style: none;

代码就不插入了，感觉记住就行

## 3.JavaScript

