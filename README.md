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

1、Emmet插件 (*)
```
概括地说，Emmet（译者注：前身就是以前大名鼎鼎的Zen Coding，这个如果你没听说和使用过，就悲哀了）
是一个可以让你更快更高效地编写HTML和CSS，节省你大量时间的插件。怎么使用？你只需按约定的缩写形式
书写而不用写整个代码，然后按“扩展(Tab)”键，这些缩写就会自动扩展为对应的代码内容。 比如，你只需
要输入 ((h4>a[rel=external])+p>img[width=500 height=320])*12 ，然后它会被扩展转换成12个列表项
和紧随其后的图像。然后你就可以在此基础上再填写内容，就这么简单。
```
2、Terminal
```
这个插件可以让你在Sublime中直接使用终端打开你的项目文件夹，并支持使用快捷键。
```
3、Snippet (*)
创建方法：Tools > Developer > New Snippet
创建快捷键：ctrl+shift+p
```
我们在编写代码的时候，总会遇到一些需要反复使用的代码片段。这时候就需要反复的复制和黏贴，
大大影响效率。我们利用Sublime Text的snippet功能，就能很好的解决这一问题。通俗的讲，就是
把我们常用的代码分别保存起啦，然后通过插件的形式来反复调用。
```
4、Http Requester (*)
```
请求URL地址的插件
```

5、jsFormate (*)
```
js格式化
```
6、cssFormate
```
css格式化
```

7、CSSComb
```
这是用来给CSS属性进行排序的格式化插件。如果你想保持的代码干净整洁，并且希望按一定的顺序排列（是不是有点强迫症了？），
那么这个插件是一种有效解决的方案。特别是当你和其他有自己代码编写风格的开发者一同协作的时候。
```


8、SublimeLinter
```
这个插件最近才为SublimeText3重建和发布。新版本显然带来了很多新的有所不同的功能，而不是简单地把所有的Linter 
放在一个包中，开发者允许用户在升级时选择并安装自己经常使用的Linter。很明显，这可以节省磁盘空间。“更多的定制”，
这对用户是很友好的。
```

9、 SASS Build
```
SASS Build 是一个编写CSS的预处理器。这个特别的插件将帮助你妥善构建包括压缩选项在内的SASS文件。一旦你安装了这个插件，
你可以很容易地通过按Ctrl+ B（MAC系统是 Command +B）来启动它。
```

10、SideBarEnhancements (*)
```
SideBarEnhancements是一个可以自定义打开方式快捷键的工具包。他可以定义不同的快捷键打开不同的浏览器。接下来，我们先安装它
```
```
[
    { "keys": ["ctrl+shift+c"], "command": "copy_path" },
    //chrome
    { "keys": ["f1"], "command": "side_bar_files_open_with",
        "args": {
            "paths": [],
            "application": "C:\Program Files (x86)\Google\Chrome\Application\chrome.exe",
            "extensions":".*" //匹配任何文件类型
        }
    },
    //firefox
    { "keys": ["f2"], "command": "side_bar_files_open_with",
        "args": {
            "paths": [],
            "application": "D:\Program Files\Mozilla Firefox\firefox.exe",
            "extensions":".*"
        }
     },
    //ie
    { "keys": ["f4"], "command": "side_bar_files_open_with",
        "args": {
            "paths": [],
            "application": "C:\Program Files\Internet Explorer\iexplore.exe",
            "extensions":".*"
        }
    },
    //safari
    { "keys": ["f5"], "command": "side_bar_files_open_with",
        "args": {
            "paths": [],
            "application": "D:\Program Files\Safari\safari.exe",
            "extensions":".*"
        }
    }
]

```

11、Nettuts Fetch
```
如果你在用一些公用的或者开源的框架，比如 Normalize.css或者modernizr.js，但是，过了一段时间后，可能该开源库已经更新了，
而你没有发现，这个时候可能已经不太适合你的项目了，那么你就要重新折腾一遍或者继续用陈旧的文件。Nettuts Fetch可以让你设置
一些需要同步的文件列表，然后保存更新
```

12、SublimeLinter
```
这个插件最近才为SublimeText3重建和发布。新版本显然带来了很多新的有所不同的功能，而不是简单地把所有的Linter
放在一个包中，开发者允许用户在升级时选择并安装自己经常使用的Linter。很明显，这可以节省磁盘空间。“更多的定制”，
这对用户是很友好的。
```

14、Sublime CodeIntel (*)
```
代码自动提示
```

15、Bracket Highlighter
```
类似于代码匹配，可以匹配括号，引号等符号内的范围。
```

16、Trmmer
```
你知道当你编写代码时，由于错误或别的某些原因，会产生一些不必要的空格。需要注意的是多余的空格有时也会造成错误。
这个插件会自动删除这些不必要的空格。
```

17、FileDiffs
```
这个插件允许你看到SublimeText中两个不同文件的差异。你可以比较的对象可以是从剪贴板中复制的数据，
或工程中的文件，当前打开的文件等
```








