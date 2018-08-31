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

___
###7.什么是`em`和`rem`，他们的区别？

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

___
###20. 怎么处理移动端兼容性问题？

___
###21. 怎么的命名方式比较规范？

___
###22. 平时浏览的网站？

___
###23. `1==2==0`, `1===2===0`的结果？
`值比较和类型比较`  


