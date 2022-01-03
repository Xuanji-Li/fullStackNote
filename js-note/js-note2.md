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

 +  1）箭头函数没有自己的this对象（详见下文）
 + （3）不可以使用arguments对象，该对象在函数体内不存在。如果要用，可以用 rest 参数代替

## 4

touch index.html
npm init
npm install --save-dev -parcel
npx parcel index.html