###1. 三种meta标签？
`meta标签的常用用法`        
   
1)可解决移动适配    
meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1"    
`width=device-width`与`initial-scale=1`，     
作用相同，但作用的机型不同，前者可用于IE，后者用于chrome,ios，      
若设计图与移动端不匹配(如设计图20px，移动端10px)，       
可直接/2或将initial-scale=0.5；     
     
2)编码     
 charset=UTF-8 / gb2312    
    
3)seo优化(搜索引擎)      
meta name="keywords" content="关键字1，关键字2"    
meta name="description" content="150 words"     
meta name="robots" content="index,follow"    
all:文章将被检索，且页面上的链接不可以被查询；   
none：文件将不被检索，且页面上的链接不可以被查询；   
index:文件将被检索；   
follow:页面上的链接可以被查询；    
noindex:文件将不被检索；    
nofollow:页面上的链接不可以被查询；     
    
3)忽略手机自动识别电话，邮箱    
meta content="telephone=no" name="format-detection"   
meta content="email=no" name="format-detection"   
    
4)选择浏览器默认内核   
meta name="renderer" content="webkit" //默认webkit内核    

___
###2. 常用的五个标签和应用场景？
`注意代码的语义化和书写规范`        
    
div:div中不要直接套文字，div中加span,p,label都可以      
span:主流框架对span都没有更改，不管应用哪一款框架，span标签都不会被更改   
label:框架一般对label都有定制   
input   
i:图标中i标签常用（http://www.iconfont.cn） //图标库    
p:段落标签    
button:按钮标签(某些网站的标签用span代替)

___
###3. box-sizing的取值和相应的作用？
`用知识点引导盒子模型`     
     
标准盒子模型的width和height是content的宽高；    
IE盒子模型的width和height是content+pandding+border。     
W3C定义box-sizing根据开发者的需要进行两种取值。

___
###4.让子元素`position:absolute`生效，父元素应该怎么设置？     
父级position设置为absolute,fixed,relative都可以。     
transform:translate也能移动。     
relative和transform实现的都是初始位置在文档中不消失，     
但本身脱离文档流偏移，不占偏移后的位置，保留原始位置。    
transform：scale   缩放     
圆的放大缩小以圆心为基准。

___
###5.`position`设置为`absolute`的`div`和`span`分别是什么样子？
`用知识点引导position的具体作用`      
    
一样的，都是设置多高就是多高。    
position设置为absolute后，display属性全部失效，    
position是布局里最高级的。  （position>float>display）

___
###6. `margin`穿透问题怎么解决？
`详细说明BFC`     
    
两个div，一个margin-bottom:100px;下面一个margin-top:200px;     
他们的中间距离是多少？（200）     
原因：子元素和父元素margin穿透（两个同级元素margin折叠）     
     
BFC:block formatting context，块级元素格式化上下文。      
形成BFC的条件：     
①浮动元素：float除none意外的值；     
②绝对定位元素：position(absolute,fixed);     
③display的值为以下之一：inline-blocks,table-cells,table-captions；     
④overflow除visible以外的值(hidden,auto,scroll)。     
父元素设置为overflow:hidden，子元素即使浮动，父元素也会被撑开。     
BFC是一个完全独立的空间，它会把内部的浮动元素的高度也计算在内，内部元素不会影响到外部元素。     
把一个元素的display设置为block，width为100%（效果与display:inline-block width:100%一样）。      
同在一个BFC的两个margin元素也会折叠。    
IFC：inline-block的格式化上下文。

___
###7.什么是`em`和`rem`，他们的区别？     
    
em相对于父元素，rem相对于根元素。     
em首先根据自己的font-size大小，本身没有设置就向上级查找。

___
###8. 简单说下`bootstrap`栅格系统的实现原理？
`栅格系统的原理被应用到目前所有流行的UI框架，引发问题，如：哪个属性让一个col及时没有内容也会占据它的位置？`     
    


___
###9. 如何阻止冒泡事件？

___
###10.【代码量】变量提升？

___
###11. 如何实现原型替换？
`什么是原型？`

___
###12. `this`指向的具体规则？

___
###13. 什么是闭包？
`组建封装的先行者`        

能够读取其他函数内部变量的函数。    
```
var func = function(){
    var a = 1;
    return function(){  //匿名函数  闭包
        a++;
        console.log(a);
    }
};
var f = func();
f();
f();
f();
```
这里的闭包因为调用了外部作用域的变量a,三个f分别输出的是2,3,4。     
    
怎么清理闭包：    
把用到这个函数的变量做一个内存的重新指向。

___
###14. `let`和`var`有什么区别？举例说明。

___
###15. 模块在同一个页面引入两次，会引起几次js渲染？为什么？

___
###16. 如何统一管理promise的错误处理函数？

___
###17. promise的`resolve`中最多能携带几参数？

___
###18. 在工作中如何应用promise？
`原理和其他用法`

___
###19. 从哪些方面可以提升前端性能？      
①CSS放在头部，JS放在body最下方；     
②长篇的CSS或JS代码放在CSS或JS文件内；     
③get和post的区别：    
get参数在url上，post在body上，   
get能被缓存，post不能缓存，浏览器会默认缓存get请求，     
get有长度限制，post没有，     
get只发送一次请求，post发送两次，因为get发送的数据是URL的一部分；     
④img和a标签的src不要写空的；     
⑤使用压缩工具压缩CSS,JS,HTML代码；     
⑥服务器渲染；

___
###20. 怎么处理移动端兼容性问题？

___
###21. 怎么的命名方式比较规范？

___
###22. 平时浏览的网站？

___
###23. `1==2==0`, `1===2===0`的结果？
`值比较和类型比较`  


