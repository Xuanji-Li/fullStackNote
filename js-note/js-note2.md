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
	      宏任务 微任务
[详解](https://juejin.cn/post/6844903512845860872)

## 7 

	promise 函数。 有点类似if else，去执行不同的方法。 把异步任务改为同步任务。async 改成awaite ，只有promise可以改

	特殊的case：
	setTimeout。        异步任务， 宏任务
	promise 是微任务     异步任务       
	


	string -0 - number
	
