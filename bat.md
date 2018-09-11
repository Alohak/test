###1.有哪些方式可以对一个DOM设置它的CSS样式？     
①外部样式表：引入一下外部CSS文件；     
②内部样式表：把CSS代码放在`<head>`标签内部；   
③内联样式：将CSS样式直接定义在HTML元素内部。   
   
###2.CSS有哪些选择器？   
①派生选择器（用HTML标签声明）；   
②id选择器（用DOM的ID声明）；   
③类选择器（用一个样式类名申明）；   
④后代选择器（用空格隔开，比如div&nbsp;&nbsp;.a{ }）;   
⑤群组选择器（用逗号隔开，比如p,div,#a{ }）。   
  
css选择器的优先级：  
*用1表示派生类选择器的优先级    
*用10表示类选择器的优先级   
*用100表示ID选择器的优先级    
*div .test1 .span var 优先级 1+10+10+1   
*span #xxx .songs li 优先级 1+100+10+1   
*#xxx li 优先级 100+1   
`<style>`   
    `.classA{color:blue;}`     
    `.classB{color:red;}`      
`</style>`      
`<body>`     
    `<p class='classB' classA>123</p>`    
`</body>`    
颜色为red，与样式定义在文件中的先后顺序有关，即后面的覆盖前面的，    
与在`<p class='classB' classA>`中的先后无关。     
###3.CSS中可以通过哪些属性定义，使一个DOM元素不显示在浏览器的可视范围内？     
基本：设置display属性为none，或设置visibility属性为hidden。     
技巧：设置宽高为0，透明度为0，z-index位置在-1000。    
###4.超链接访问过后hover样式就不出现的问题是什么？如何解决？   
被点击访问过的超链接样式不再具有hover和active了，   
解决办法是改变CSS属性的排列顺序：L-V-H-A(link,visited,hover,active)。   
###5.行内元素和块级元素的具体区别是什么？行内元素的padding和margin可设置吗？     
块级元素(block)特性：    
*总是独占一行，表现为另起一行开始，而且其后的元素也必须另起一行显示；    
*宽度，高度，内边距(padding)和外边距(margin)都可控制；    
    
内联元素(inline)特性：    
*和相邻的内联元素在同一行；    
*高度，宽度，内边距和外边距的top/bottom都不可改变(也就是padding和margin的left和right可以设置)；     
    
浏览器默认的天生inline-block有哪些？(拥有内在尺寸，可设置宽高，但不会自动换行)     
`<input>`  `img` `button` `textarea` `label`    
###6.rgba()和opacity的透明效果有何不同？    
opacity作用于元素，以及元素内的所有内容的透明度；    
而rgba()只作用于元素的颜色或背景色。    
*设置rgba透明的元素的子元素不会继承透明效果。   
###7.CSS中可以让文字在垂直和水平方向上重叠的两个属性是什么？   
垂直方向：line-height;   
水平方向：letter-spacing。   
*letter-spacing可以用于消除inline-block元素间的换行符空格间隙问题。    
###8.px和em的区别？
