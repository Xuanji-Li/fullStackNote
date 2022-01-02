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

		btn.addEventLisenter("click", (){
			console.log(btn.tagName);
		})

		btn.addEventLisenter("click", ()=>{
			console.log(btn.tagName);
		})
	</script>
</body>
```
以上三者的区别

## 2

function(){} //报错
(function(){}) //不报错
function f(x) {return x+1} ()  //报错
function f(x) {return x+1} (1) //不报错，为什么返回1 

## 3 

箭头函数是什么
为什么要用