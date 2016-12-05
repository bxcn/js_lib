#Snippet

创建方法：Tools > Developer > New Snippet

创建快捷键：ctrl+shift+p

我们在编写代码的时候，总会遇到一些需要反复使用的代码片段。这时候就需要反复的复制和黏贴，大大影响效率。我们利用Sublime Text的snippet功能，就能很好的解决这一问题。通俗的讲，就是把我们常用的代码分别保存起啦，然后通过插件的形式来反复调用。

创建snippet模板
```html
<snippet>
  <content><![CDATA[
| title | title |
|-------|-------|
|content|content|
]]></content>
  <!-- Optional: Set a tabTrigger to define how to trigger the snippet -->
  <tabTrigger>mdtable</tabTrigger>
  <!-- Optional: Set a scope to limit where the snippet will trigger -->
  <!-- <scope>source.python</scope> -->
</snippet>
```

模板说明：
```html
<content><![CDATA[ 这里放模板内容 ]]></content>
<tabTrigger>这里放需要在编辑器输入的内容</tabTrigger>
```