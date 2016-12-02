# sublime插件配置说明文档

# 安装Sublime Package Control 安装步骤

* 第一步：打开sublime 找到View > Show Console这个菜单或 ctrl+` 打开 console它;

* 第二步：根据版本不同把下面的代码粘贴到console中回车

Sublime Text 2
```
import urllib2,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')
```


Sublime Text 3
```
import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```


#常用插件
------------------------------------------------------------

1、Emmet插件
```
概括地说，Emmet（译者注：前身就是以前大名鼎鼎的Zen Coding，这个如果你没听说和使用过，就悲哀了）是一个可以让你更快更高效地编写HTML和CSS，节省你大量时间的插件。怎么使用？你只需按约定的缩写形式书写而不用写整个代码，然后按“扩展(Tab)”键，这些缩写就会自动扩展为对应的代码内容。 比如，你只需要输入 ((h4>a[rel=external])+p>img[width=500 height=320])*12 ，然后它会被扩展转换成12个列表项和紧随其后的图像。然后你就可以在此基础上再填写内容，就这么简单。
```
2、Terminal
```
这个插件可以让你在Sublime中直接使用终端打开你的项目文件夹，并支持使用快捷键。
```
3、Snippet
创建方法：Tools > Developer > New Snippet
创建快捷键：ctrl+shift+p
```

我们在编写代码的时候，总会遇到一些需要反复使用的代码片段。这时候就需要反复的复制和黏贴，大大影响效率。我们利用Sublime Text的snippet功能，就能很好的解决这一问题。通俗的讲，就是把我们常用的代码分别保存起啦，然后通过插件的形式来反复调用。
```



