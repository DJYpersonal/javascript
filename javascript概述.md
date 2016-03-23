# javascript概述

## 基础逻辑处理部分

> 变量 数据类型    (数据存储)
> 分支和循环、运算符      (逻辑操作)
> 函数（对语言的扩展）

### 变量类型

```javascript
var vr=[1,2,3];     //Array
var vr=1.2;         //Number
var vr='1';         //String
var vr={a:1,b:2}    //Object
var vr=function(){} //Function
var vr=false        //Boolean
var vr=null         
var vr=undefined   


### 运算符
```javascript
+ - * / %
===  !==  >  <  >=  <=
&&  ||  !
```


### 分支语句
```javascript
if()
if() else
if() else if()else if()
switch(x){
	case1:	
	break;
	case2:
	break;
	default:
	break
}
```

### 循环语句
```javascript
for(var i=0,k=1; i<100; i++){
	
}
while(){
	
}
do{
	
}while()
```

### 函数
```javascript
function xx(){
	
}
var fn=function(x1,x2){
	// arguments
}
fn(a,b)

function A(c){
	this.x=c;
}
A.prototype.console = function(){
	console.log(this.x);
}
var obj=new A(1);
obj.console();
```
### 数组的常用方法
### 字符串中的常用方法
### 函数对象中的方法  bind apply call
### 对象的增删改查 原型链
### 数字对象身上的方法  toFixed()
### Math对象身上的方法



## 针对特定用途的部分

> 当js来浏览器运行的那一刻
> 浏览器会创建一个window对象
> window对象中很多属性和方法
> 这些属性和方法不用加window.就可以调用和使用

dom对象  dom集合
  

### 选取元素


*  var el= document.getElementById()
*  var el= document.getElementsByClassName()
*  var el= document.getElementsByTagName()
   var all=document.getElementsByTagName("*")  //获取页面中所有的元素
*  var el= document.getElementsByName()

### 筛选元素

* el.parentNode
* el.childNodes
* el.firstChild
* el.lastChild
* el.nextSibling
* el.previousSibling

### 操作样式
el.style.color='red';
el.currentStyle.width=200;      //IE
el.offsetWidth
el.offsetHeight


### 获取元素信息
el.style.offsetTop
el.style.offsetLeft
el.style.offsetWidth
el.style.offsetHeight

### 操作属性

document.title
<!-- document.bgColor
document.fgColor
document.URL -->
el.setAttribute("aa","bb")  //添加自定义属性
el.getAttribute("aa")       //获取自定义属性

### 节点操作

document.createElement("")


### 其他
innerHTML
innerText
textContent
