# JB.js
一个基于jQuery的前端渲染框架

## 用法
引用了**jb.min.js**就不用引入jQuery了，其中已经包含了jQuery。

```
<html>

<head>
	<title>demo</title>
	<script src="./jb.min.js"></script>
</head>
<body>
	
	<div class="test">
		<h2>{{name}}</h2>
		<p>{{content}}</p>
		<ul>
			{{if isShow}}
			
			{{each users item idx}}
				<li>{{idx}} {{item.name}}</li>
			{{/each}}
			
			{{/if}}
		</ul>
	</div>
	
	<script>
		$(function(){
			
			JB.render({
				element:".test",
				data:{
					name:"我的简介",
					content:"我们是XXXXX，自从1998创立年以来...",
					users: [{name: 'juincen'},{name: 'mike'},{name: 'candy'}],
					isShow:true
				}
			});
		});
	</script>
</body>
</html>

```

## 注意

向上面这样用JB这个对象，使用render方法，传入参数后即可自动渲染，请不要直接传body
建议使用id选择器，或者类选择器。</br>
QQ：709197459
