 	# js note


## 1
```html
<body>
	<script type="text/javascript">
		btn.addEventLisenter("click", function abc(){
			console.log(btn.tagName);
		})
		btn.addEventLisenter("click", function(){
			console.log(btn.tagName);
		})

		// btn.addEventLisenter("click", (){
		// 	console.log(btn.tagName);
		// })

		btn.addEventLisenter("click", ()=>{
			console.log(btn.tagName);
		})
	</script>
</body>
```
以上三者的区别

## 2

function (){} //报错
(function(){}) //不报错
function f(x) {return x+1} ()  //报错
function f(x) {return x+1} (1) //不报错，为什么返回1 

## 3 

箭头函数是什么
为什么要用

 + 箭头函数是匿名函数，不能作为构造函数，不能使用new
 +  1）箭头函数没有自己的this对象
 + （3）不可以使用arguments对象，该对象在函数体内不存在。如果要用，可以用 rest 参数代替

## 4
	
	touch index.html   
	npm init   
	npm install --save-dev -parcel   
	npx parcel index.html   

   ### dev & build
	<script>
	 "dev": "parcel   index.html --port 8080",
    "build": "parcel build index.html",
	</script>

    npm run dev	启动本地开发环境服务
    npm run build 打包


## 5 

	ES6  javascript 完整版详解

[ES6](https://es6.ruanyifeng.com/#docs/promise)

## 6 
	
	js 的 同步任务 异步任务  
	              异步任务又分为：宏任务 微任务  

	典型的宏任务 包括整体代码script，setTimeout() setIntervel()  ，I/O  
	微任务是Promise，process.nextTick  
	微任务的执行时机要比宏任务来的早
[bilibili ](https://www.bilibili.com/video/BV1CA411V791?from=search&seid=13959033135384420900&spm_id_from=333.337.0.0)
[详解](https://www.jianshu.com/p/0652db9cfb46)	
[详解](https://juejin.cn/post/6844903512845860872)

## 7 

	promise 函数。 有点类似if else，去执行不同的方法。 把异步任务改为同步任务。async 改成awaite ，只有promise可以改        
	
## 8 
	string转换数字直接-0  
	
## 9 
	常用的js方法 对数组进行操作的方法，for循环等  
   ![](pic/4.jpeg)  

## js的按对象引用传值

	如果
	var a=b={}
	a="str"
	a和b都会变成“str”

	但是如果是number类型
	var a=b=0 
	a=1
	不会引用传值

	尽量避免引用传值

## js事件冒泡和事件捕捉

### 往父级元素冒泡
```javascript
<div class="out">out
        <div class="middle">midlle
            <p class="inner" >inner<p>
        </div>
</div>
<script type="text/javascript">
        let clickOut= document.querySelector(".out")
        let clickMiddle=document.querySelector(".middle");
        let clickInner=document.querySelector(".inner")
        clickOut.onclick=function(){
            console.log('this is out');
        };
        clickMiddle.onclick= function(){
            console.log('this is middle')
        }
        clickInner.onclick=function(event){
            event.stopPropagation();
            console.log('this is inner');
        };
</script>
```
点击inner 依此打印inner middle out

### 事件捕获

	js事件捕获一般通过DOM2事件模型addEventListener来实现的：   
	target.addEventListener(type, listener, useCapture)  
	第三个参数是是否用事件捕捉    
```javascript
<div class ="out2">out2
        <p class="middle2">middle2
            <p class="inner2">inner2</p>
        </p>
</div>
<script type="text/javascript">
 		let clickOut2=document.querySelector(".out2");
        let clickMiddle2=document.querySelector(".middle2");
        let clickInner2=document.querySelector(".inner2");
        clickOut2.addEventListener("click",function(){console.log('out2')},true);
        clickMiddle2.addEventListener("click",function(){console.log('middle2')},true);
        clickInner2.addEventListener("click",function(){console.log('inner2')},true);
</script>



	
	
