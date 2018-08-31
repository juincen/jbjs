# jbjs
一个基于jQuery的前端渲染框架

## 用法
引用了jb.min.js就不用引入jQuery了，其中已经包含了jQuery。

<div id="test">
  <h2>{{name}}</h2>
  <p>{{content}}</p>
</div>

JB.render({
  element:"#test",
  data:{
    name:"我的简介",
    content:"我们是XXXXX，自从1998创立年以来..."
  }
});

然后即可自动渲染，请不要直接传body
建议使用id选择器，或者类选择器
