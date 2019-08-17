# Javaweb开发：

​	架构：
​	c/s
​		优点：用户体验好
​		缺点：开发、维护、部署麻烦 
​	b/s：通过URL访问不同的客户端程序
​		优点：开发、维护、部署简单
​		缺点：如果应用过大，用户体验差
​			对硬件要求高

​	架构详解：
​	静态资源：
​		使用静态网页开发技术发布的资源
​		HTML，CSS，JAVASCRIPT（三个静态网页开发技术）
​		如果用户请求静态资源，那么服务器会直接将静态资源发送给浏览器，浏览器内置了静态资源的解析引擎，可以展示静态资源
​		
​	动态资源：（java开发
​		使用动态网页开发技术发布的资源
​			jsp/servlet（学习），php，asp
​			如果用户请求动态资源，服务器会执行动态资源，转换为静态资源，再发送给浏览器
​	学习动态资源，必须先学习静态资源：
​		HTML：用于搭建基础网页，展示页面内容
​		CSS：用于美化页面，布局页面
​		JavaScript：控制页面元素，让页面有动态效果

HTML	最基础的网页开发语言
	Hyper Text MarkUp Language 超文本标记语言
	超文本：用超链接的方法，将各种不同空间的文本信息连接起来
	标记语言：由标签构成的语言 <标签名称> 
		标记语言不是编程语言

快速入门：.html/.htm
	标签分为
		围堵标签:<html> </html>
		标签可以嵌套，需要正确嵌套

​		自闭合标签，开始和结束在一起<br/>

​		在开始标签中可以定义属性。属性由键值对构成，值需要用引号（单双都可以）引起来
​		html标签不区分大小写，建议使用小写

标签：
	文件标签：构成HTML最基本的标签
		html：html文档的根标签
		head：头标签。用于指定html文档的一些属性。引入外部的资源
		title：定义标题
		body：体标签
		< !DOCTYPE html>? : html5中定义该文档是html文档
		< meta charset="UTF-8">指定字符集
		

​	文本标签：和文本相关的标签
​		注释：<!-- 注释内容 -->
​		< h1> to < h6> 标题标签，字体大小递减
​		< p>	段落标签，围堵标签
​		< br/>	换行标签
​		< hr/>	显示一条水平线
​		<b> 字体加粗
​		<i> 斜体
​		<font>字体标签 //已过时
​		特殊字符  &copy；等

​	图片标签：
​		<img>  展示图片 需要在模组下
​		./当前目录
​		../上级目录

​	列表标签：
​		有序列表：
​			ol:
​			li:

```html
<ol> 
    <li>2</li>   
    <li>3</li>
</ol>
```

​		无序列表：
​			ul:
​			li:

```
<ul type="2">    
	<li>1</li>
</ul>
```

​	连接标签：
​		a:超链接
​			herf：指定访问资源的URL（统一资源定位符）
​				target="_ blank"新选项卡跳转
​				target="_self"本页面跳转
​				./本地目录
​				mailto:xxx@xxx.com

```html
<a herf="1_Helloworld.html"<img src="1_HelloWorld.html"></a>
```

​	div/span标签：
​		<span>将文本包裹起来，进行样式控制<span/>
​			文本信息在一行展示，也称为行内标签，内联标签
​		< div>同上<div/ >
​			每个div占满一行。块级标签

语义化：
html4 < div id=xxx><div/>	
html5 <xxx><div></div></xxx>

	<table border="1" width="30%" style="stroke-dasharray: 300px">
	    <thead>
	        <caption>信息</caption>
	        <tr>
	            <td>编号</td>
	            <td>成绩</td>
	        </tr>
	    </thead>
	    <tbody>
	        <tr>
	            <td>x</td>
	            <td>122</td>
	        </tr>
	    </tbody>
	    <tfoot>
	        <tr>
	            <td>0</td>
	        </tr>
	    </tfoot>
	</table>

form：用于定义表单的。可以定义一个范围，范围代表采集用户数据的范围
表单项中的数据要想被提交，必须指定其name属性
	属性：
		action：指定提交数据的URL
		method：指定提交方式
			分类：一共7种
			get：
				1、请求参数会在地址栏中显示，会封装在请求行中
				2、url长度/请求长度是有限制的
				3、不太安全
​			post：
​				1、请求参数不会在地址栏中显示，会封装在请求体中
​				2、请求大小没有限制
				3、较为安全
				
< form action="#" method="get">
​    用户名：<input name="username"><br/>
​    密码： <input name="password"><br/>
​        <input type="submit" value="登陆">
​    </form >

表单项标签：
	input：可以通过ytpe属性值，改变元素展示的样式
		type属性：
			text：文本
				placeholder：指定输入框的提示信息
				label标签：指定输入项的文字描述信息
					label的 for 属性一般会和input的 id 属性值对应
					如果对应了，则点击label区域，会获取焦点，下同
			password：密码
			radio：单选框
				要想让多个单选框实现单选的效果，则多个name的属性值必须相同
				一般会给每一个单选框提供value属性，指定其被选中时提供的值
			checkbox：复选框
				checked 默认选中，上同
			file：文件选择框
			hidden：隐藏域，用于提交一些信息
			按钮：
				submit：提交
				button：按钮
				image：图片提交按钮，src指定图片路径
	select：下拉列表
		name：元素名称
		子元素option，指定列表项
	textarea：文本域
​		cols：指定列数，每行多少字符
		rows：指定行数
​			

<form action="#" method="get">
        <label for="username">用户名</label>:
            <input type="text" name="username" placeholder="请" id="username"><br/>
        密码： <input type="password" name="password"><br/>
        性别：
            <input type="radio" name="gender" value="male" checked>男
            <input type="radio" name="gender" value="female">女<br/>
        爱好：
            <input type="checkbox" name="bobby" value="篮球">篮球
            <input type="checkbox" name="bobby" value="JAVA">JAVA<br/>
        图片：
            <input type="file" name="file"><br/>
        隐藏域:
            <input type="hidden" name="id" value="url"><br/>
        按钮
            <input type="button" value="登陆1"><br/>
        登陆
            <input type="submit" value="登陆"><br/>
        图片按钮
            <input type="image" src="HTML.iml"><br/>
        省份
            <select name="province">
                <option value="">--请--</option>
                <option value="1">北京</option>
                <option value="2" selected>上海</option>
            </select><br/>
        自我描述
            <textarea cols="40" rows="5" name="describition"></textarea>
    </form>
##### 详见p588

​			

### CSS
Cascading Style Sheets 层叠样式表
	层叠：多个样式可以作用于一个html的元素（标签）上，同时生效
优点：
	1、功能强大
	2、内容展示和样式控制分离
		降低耦合度
		让分工协作更容易
		提高开发效率

​			
















​			
​		