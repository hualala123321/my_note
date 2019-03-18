# js补充
## arguments对象

## 绑定监听
+ 使用 对象.事件=函数 的形式绑定响应函数，只能为一个元素的一个事件绑定响应函数。如果绑定多个则后面的会覆盖掉前面的。
比如：
一个对象 只能通过 onclick绑定一个事件
```
obj.onclick = function(){
	alert('hello!');
}
obj.onclick = function(){
	alert('world!');
}
```
+ 通过addEventListener()为元素绑定响应式函数。
+ addEventListener参数：
	- 事件的字符串，不要on。
	- 回调函数 当事件被触发时该函数会被调用。
	- 是否在捕获阶段触发事件，需要一个布尔值，一般都传false。
+ 使用addEventListener()可以同时为一个元素绑定多个响应函数。当事件触发时，会按响应函数的函数绑定顺序执行。
+ 形式：
`addEventListener(event,funtionName,useCapture)`
1. event:事件的类型如 “click”
2. funtionName：方法名
3. useCapture(可选)：布尔值，指定事件是否在捕获或冒泡阶段执行。   true  事件句柄在捕获阶段执行    
false  默认。事件句柄在冒泡阶段执行
```
obj.addEventListener('click',function(){
//do something
});
```