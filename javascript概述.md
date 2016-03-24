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

> 按照我们正常编程思路
> 第一步就是找出元素
> 我们从document对象开始，利用它身上的方法
> 找出我们需要的元素（dom元素 或 dom集合）

### 选取元素
*  var el= document.creatElement();
*  var el= document.getElementById()
*  var el= document.querySelector()           //传进的是CSS选择器

*  var el= document.getElementsByClassName()
*  var el= document.getElementsByTagName()
*  var el= document.getElementsByName()
*  var el=document.querySelectorAll()          //ie8

经过这一步我们会得到一个dom元素或dom集合

dom对象
js会用一个很大的对象来代表页面中我们看到的那个元素
```javascript
{
  offestHeight:11111
  offsetLeft:1111
  offsetTop:111
  offsetWidth:12222

}
```
dom集合
在一个类数组对象中存储很多dom对象构成一个集合
```javascript



```

### 筛选元素
>从一个dom对象开始，根据逻辑关系再去寻找dom对象

>父元素
* el.parentNode
* el.parentElement

>子元素
* el.children
* el.childNodes

* el.firstChild
* el.firstElementChild

* el.lastChild
* el.lastElementChild

>兄弟元素
* el.nextSibling
* el.nextElementSibling

* el.previousSibling
* el.previousElementSibling

### 属性操作  (Element)

* el.setAttribute()
* el.getAttribute()
* el.removeAttribute()
* el.hasAttribute()
* el.className
* el.id
* el.classList

### 节点操作  (NOde)

* el.appendChild()
* el.removeChild()
* el.isertBefore()
* el.cloneNode()
* el.replaceChild()

### 获取元素信息  (HTMLElement)

* el.offsetTop
* el.offsetLeft
* el.offsetWidth
* el.offsetHeight
* el.offsetParent      //具体定位属性的父元素
* el.getBoundingClietRect()   //计算元素距离窗口的位置
* el.innerHTML
* getComputedStyle(el,null).width

### 样式操作
* el.style.color (读取行内样式的值，设置行内样式的值)

### get和set 在dom对象中的使用

```javascript
var obj= {
	a:1,
	b:2,
	set c (x){ console.log(111)},
	get c () { return 5;}
}
```