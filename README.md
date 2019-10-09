# html-summary 常用知识点回顾

## 一. HTML基础(1-9)

### 1. doctype 有什么作用？怎么写？
定义文档类型,建立符合网页标准的文档
</br>`<!DOCTYPE html>`

### 2. 列出常见的标签，并简单介绍这些标签用在什么场景？        
- 文档结构标签: 主要用来标识文档的基本结构</br>`<html></html>;<head></head>;<body></body>==`    
- 文本格式标签: 主要用来标识文本区块,并附带一定的显示格式</br>`<title></title>;<hi></hi>;<p></p>;==`        
- 字符格式标签:部分文本的语义</br>`<sup></sup>;<sub></sub>==  `      
- 列表标签: 有序列表和无序列表        
- 链接标签:</br>`<a></a> `      
- 多媒体标签:引入外部多媒体文件</br>`<img>;==  `      
- 表格标签:用来组织和管理数据</br>`<table></table>;<th></th>;==  `      
- 表单标签:制作交互式表单</br>`<form></form>;<input></iuput>;== ` 

### 3. 页面出现了乱码，是怎么回事？如何解决？        
- 当我们保存一个写好的 HTML 文件，编码方式会保存为 UTF-8；        
- 一个文件就是一堆的数据，即我们写的内容变成了一堆的数据。那这个数据到底是变成了 123，还是 456 呢？        
- 这里我们就用到了“编码”，用的编码方式不一样，那么数据呈现的状态就不一样；        
- 然后，当我们把这个以适当编码方式保存好的数据再次展示在浏览器页面上时（或用其他编辑器打开时），这个数据还要再恢复出来；        
- 这时候，浏览器（或编辑器）需要使用相同的、与文件相对应的编码方式去解码（但浏览器不是万能的，你不告诉他，他就不知道用什么方式去解码，他会随意选择）； 
- 这时，当编码是一种方式，而解码又是另一种方式时，页面就会出现“乱码”；        
- 而解决乱码的方式就是：只需要知道我在编辑器保存这个 HTML 文件时，保存的什么编码格式，然后在头部 <meta charset="?">中告诉浏览器用什么方式来解码。        
### 4. title 属性和 alt 属性分别有什么作用？    
- title 属性有一个很好的用途：即为链接添加描述性文字，特别是当链接本身并不是十分清楚的表达了链接的目的。    
另外一个潜在的应用就是为图像提供额外的说明信息，比如日期或者其他非本质的信息。    
- alt 这个属性主要是为了规避例如：因网速差、硬件设备限制等外部因素，我们的浏览器不能很好的显示出图像，那 alt 后边的文本将会取代图像告诉用户这里会是什么东西。 

### 5. html 的注释怎样写？   
`<!-->`</br>`<!DOCTYPE html>`      

### 6. HTML5 为什么只写 <!DOCTYPE HTML> ？        
HTML5 不基于 SGML，因此不需要对 DTD 进行引用，但是需要 doctype 来规范浏览器的行为（让浏览器按照他们应该的方式来运行）。    
而 HTML4.01 基于 SGML，所以需要对 DTD 进行引用，才能告知浏览器文档所使用的文档类型。

### 7. data- 属性的作用？    
- 作用：当没有合适的属性和元素时，自定义的 data 属性是能够存储页面或 App 的私有的自定义数据。        
- data- 为 H5 新增的为前端开发者提供自定义的属性，这些属性集可以通过对象的 dataset 属性获取；    
不支持该属性的浏览器可以通过 getAttribute 方法获取 。    
- 需要注意的是：data- 之后的以连字符分割的多个单词组成的属性，获取的时候使用驼峰风格。所有主流浏览器都支持 data-  * 属性。    

### 8. WEB 标准以及 W3C 标准是什么？   
标签闭合、标签小写、不乱嵌套、使用外链 css 和 js、结构行为表现的分离。        

### 9. HTML 全局属性（global attribute）有哪些？        
- class：为元素设置类标识；        
- data-*：为元素增加自定义属性；        
- draggable：设置元素是否可拖拽；        
- id：元素 id，文档内唯一；        
- lang：元素内容的的语言；        
- style：行内 css 样式；        
- title：元素相关的建议信息
---
## 二. HTML属性(1-3)(/br)    
### 1.meta 有哪些常见的值？        
-  指定文档编码：</br>`<meta charset="UTF-8">   `  
- 适配移动端页面：
```
<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
```
- 定制页面图标：(/br>
```
<link rel="shortcut icon" href="favicon.ico" type="image/x-icon"> 
<!-- 注释：href="favicon.ico" 这里边放这个图标的图形文件地址。--> 
```
- 设置 referer：(/br)
```
<meta name="referer" content="never">    
```
- 添加页面描述：(/br)
```
<meta name="description" content="注册即代表你同意《知乎协议》注册机构号……">     
```

### 2. 你是如何理解 HTML 语义化的？
- 内容结构化:html 语义化就是让页面的内容结构化，便于对浏览器、搜索引擎解析；在没有样式 CSS 情况下也以一种文档格式显示，并且是容易阅读的；        - - 利于 SEO:搜索引擎的爬虫依赖于标记来确定上下文和各个关键字的权重，利于 SEO；       
- 便于维护和理解:使阅读源代码的人对网站更容易将网站分块，便于阅读维护理解。        
比如，标题可以用 `<h1> ~ <h6>`；边栏用`<aside>；`头部用 `<header>；`主体内容用`<main>；`页脚用`<footer>；`等等。         
  
### 3. 前端需要注意哪些 SEO?    
1. 合理的 title、description、keywords：搜索对这三项的权重逐个减小        t
- title 关键词靠前排列,重复不超过两次,不同页面关键词要有所不同.        
- description 高度概括页面内容，长度合适(0-28)，不同页面 description 有所不同；       
- keywords 列举出重要关键词即可。   
2. 语义化的 HTML 代码，符合 W3C 规范：语义化代码让搜索引擎容易理解网页。    
3. 重要内容 HTML 代码放在最前：搜索引擎抓取 HTML 顺序是从上到下，有的搜索引擎对抓取长度有限制，保证重要内容一定会被抓取。    
4. 重要内容不要用 js 输出：爬虫不会执行 js 获取内容。    
5. 少用 iframe：搜索引擎不会抓取 iframe 中的内容    
6. 非装饰性图片必须加 alt。    
7. 提高网站速度：网站速度是搜索引擎排序的一个重要指标       
---
## 三. HTML表单(1-9)    
### 1.post 和 get 方式提交数据有什么区别？        
- GET方法是从服务器上获取数据,而POST是向服务器传递数据 *        
- GET请求会被浏览器主动缓存，并保留历史记录而POST不会，除非手动设置 *       
- GET请求在URL中传送的参数是有长度限制的，而POST没有限制 *        
- 对参数的数据类型，GET只接受ASCII字符，而POST没有限制       
- GET方法所传递的数据通过浏览器地址栏公共传递,因此不安全,POST传递的数据对用户来说是不可见的,相对安全            

### 2. 在 input 里，name 有什么作用？        
name属性定义了表单对象的名称,后台服务器能够利用该属性值来读取其中的数据.除了按钮之外,其他表单对象都应该设置name属性.   

### 3. label 有什么作用？如何使用？        
Label是标签的意思,即为表单域定义域提示信息.label元素最有用的是使用for属性使其与表单域绑定在一起,形成关联.对快速输入信息有很大帮助.
(/br>
示例代码:
```
   <form action="action.asp" name="register" id="login">         
  <!--   <fieldset> 默认显示边框效果,可通过css改变样式 -->           
     <fieldset>             
  <!-- <legend> 标签为 fieldset 元素定义标题,默认位于左上角,可通过css改变样式 -->  
          <legend>基本信息(必填)</legend>                
            <ul> 
                 <li>
                     <!-- for 用于和用户名和输入框关联,一个for必须有对应的id --> 
                        <label for="username">用户名</label>
                        <input type="text" id="username" name="username"> 
                        <span>注册用户名长度限制为3-12个字节</span> 
                  </li>  
                 <li>                        
                    <label for="psw">论坛密码</label>                        
                    <input type="password" id="psw" name="psw">                     
                </li>                
            </ul>           
 </fieldset>           
 <p><input name="" type="submit" value="提交"></p>        
</form>
```

### 4. radio 如何分组？       
type="radio" ，单选按钮,设置不同的 name 属性即可分组，同一 name 属性的属性属于同一组选项。
`<input name="radio1" type="radio" value=""> `
`<input name="radio1" type="radio" value="">`  

### 5. placeholder 属性有什么作用？    
placeholder 属性提供可描述输入字段预期值的提示信息（hint）。该提示会在输入字段为空时显示，并会在字段获得焦点时消失。    
```
注释：placeholder 属性适用于以下的 <input> 类型：text, search, url, telephone, email 以及 password。<!-- placeholder 在输入框中显示的提示信息 -->   
```
`<input type="search" name="user_search" placeholder="Search W3School" >  `              
`<input type="submit" >`

### 6.type=hidden 隐藏域有什么作用？举例说明。    
在实际应用中,很多数据不需要用户输入,但是需要作为参数传递给服务器,使用隐藏域可以避免这些数据对表单交互行为的干扰.    

### 7. CSRF 攻击是什么？如何防范？   
#### (1). 是什么：
CSRF（Cross-site request forgery），中文名称：跨站请求伪造。攻击者盗用了你的身份，以你的名义发送恶意请求。        
CSRF 能够做的事情包括：以你名义发送邮件，发消息，盗取你的账号，甚至于购买商品，虚拟货币转账......造成的问题包括：个人隐私泄露以及财产安全。例如通过 QQ 等聊天软件发送的链接(有些还伪装成短域名，用户无法分辨)，攻击者就能迫使 Web 应用的用户去执行攻击者预设的操作。例如，当用户登录网络银行去查看其存款余额，在他没有退出时，就点击了一个 QQ 好友发来的链接，那么该用户银行帐户中的资金就有可能被转移到攻击者指定的帐户中。      

#### (2). 如何防范：        
采用 anti-csrf-token 方案。        
1. 服务端在收到路由请求时，生成一个随机数，在渲染请求页面时把随机数埋入页面（一般埋入 form 表单内，`<input type="hidden" name="_csrf_token" value="xxxx">`）；       
2. 服务端设置 setCookie，把该随机数作为 cookie 或者 session 种入用户浏览器；        
3. 当用户发送 GET 或者 POST 请求时带上_csrf_token参数（对于 Form 表单直接提交即可，因为会自动把当前表单内所有的 input 提交给后台，包括_csrf_token）；       
4. 后台在接受到请求后解析请求的cookie获取_csrf_token的值，然后和用户请求提交的_csrf_token做个比较，如果相等表示请求是合法的。

