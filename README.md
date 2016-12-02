clone地址：
```bash
git clone git://github.com/bxcn/sublime_plugins_config.git
```

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

#常用插件导航
- [emmet ](#emmet)
- [terminal](#terminal)
- [snippet ](#snippet)
- [http requester ](#http-requester)
- [jsformate ](#terminal)
- [cssformate](#terminal)
- [csscomb](#csscomb)
- [sublimelinter](#sublimelinter)
- [sass build](#sass-build)
- [sidebarenhancements ](#sidebarenhancements)
- [nettuts fetch](#nettuts-fetch)
- [plaintasks](#plaintasks)
- [sublime codeintel](#sublime-codeintel)
- [bracket highlighter](#bracket-highlighter)
- [trmmer](#trmmer)
- [filediffs](#filediffs)
- [gbk support](#gbk-support)
- [jquery package](#jquery-package)
- [docblock](#terminal)
- [autofilename](#autofilename)
- [advancenewfile](#terminal)
- [babel](#terminal)
- [clipboard history](#clipboard-history)
- [imesupport](#imesupport)
- [trailing spaces](#trailing-spaces)


#常用插件

##Emmet 

概括地说，Emmet（译者注：前身就是以前大名鼎鼎的Zen Coding，这个如果你没听说和使用过，就悲哀了）是一个可以让你更快更高效地编写HTML和CSS，节省你大量时间的插件。怎么使用？你只需按约定的缩写形式书写而不用写整个代码，然后按“扩展(Tab)”键，这些缩写就会自动扩展为对应的代码内容。 比如，你只需要输入 ((h4>a[rel=external])+p>img[width=500 height=320])*12 ，然后它会被扩展转换成12个列表项和紧随其后的图像。然后你就可以在此基础上再填写内容，就这么简单。

##Terminal

这个插件可以让你在Sublime中直接使用终端打开你的项目文件夹，并支持使用快捷键。

##Snippet 
创建方法：Tools > Developer > New Snippet
创建快捷键：ctrl+shift+p

我们在编写代码的时候，总会遇到一些需要反复使用的代码片段。这时候就需要反复的复制和黏贴，大大影响效率。我们利用Sublime Text的snippet功能，就能很好的解决这一问题。通俗的讲，就是把我们常用的代码分别保存起啦，然后通过插件的形式来反复调用。

##Http Requester 

请求URL地址的插件


##jsFormate 

js格式化

##cssFormate

css格式化


##CSSComb

这是用来给CSS属性进行排序的格式化插件。如果你想保持的代码干净整洁，并且希望按一定的顺序排列（是不是有点强迫症了？），那么这个插件是一种有效解决的方案。特别是当你和其他有自己代码编写风格的开发者一同协作的时候。



##SublimeLinter

这个插件最近才为SublimeText3重建和发布。新版本显然带来了很多新的有所不同的功能，而不是简单地把所有的Linter 放在一个包中，开发者允许用户在升级时选择并安装自己经常使用的Linter。很明显，这可以节省磁盘空间。“更多的定制”，这对用户是很友好的。


##SASS Build

SASS Build 是一个编写CSS的预处理器。这个特别的插件将帮助你妥善构建包括压缩选项在内的SASS文件。一旦你安装了这个插件，你可以很容易地通过按Ctrl+ B（MAC系统是 Command +B）来启动它。


##SideBarEnhancements 

SideBarEnhancements是一个可以自定义打开方式快捷键的工具包。他可以定义不同的快捷键打开不同的浏览器。接下来，我们先安装它


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



##Nettuts Fetch

如果你在用一些公用的或者开源的框架，比如 Normalize.css或者modernizr.js，但是，过了一段时间后，可能该开源库已经更新了，而你没有发现，这个时候可能已经不太适合你的项目了，那么你就要重新折腾一遍或者继续用陈旧的文件。Nettuts Fetch可以让你设置一些需要同步的文件列表，然后保存更新


##plaintasks
PlainTasks 支持通过快捷键来添加任务、标记完成、归档，支持添加标签等等功能，且充分利用了 Sublime Text 2 的一些功能优势.

##Sublime CodeIntel

代码自动提示.

##Bracket Highlighter

类似于代码匹配，可以匹配括号，引号等符号内的范围。


##Trmmer

你知道当你编写代码时，由于错误或别的某些原因，会产生一些不必要的空格。需要注意的是多余的空格有时也会造成错误。这个插件会自动删除这些不必要的空格。

##FileDiffs

这个插件允许你看到SublimeText中两个不同文件的差异。你可以比较的对象可以是从剪贴板中复制的数据，或工程中的文件，当前打开的文件等

##GBK Support

对应gb2312来说，Sublime Text 2 本生不支持的，我们可以通过Ctrl+Shift+P调出命令面板或Perferences->Package Contro,输入install 调出 Install Package 选项并回车，在输入“GBK Support”选择开始安装，左下角状态栏有提示安装成功。这时打开gbk编码的文件就不会出现乱码了，如果有需要转成utf-8的可以在File-GBK to UTF8-选择Save with UTF8就偶看了。

##jQuery Package

##DocBlockr 

注释插件 DocBlockr这个插件可以很好的生成js ,php 等语言函数注释,只需要在函数上面输入/** ,然后按tab 就会自动生成注释

##AutoFileName

快捷输入文件名，自动完成文件名的输入，如图片选取，输入”/”即可看到相对于本项目文件夹的其他文件


##AdvanceNewFile
ST本来自带的创建新文件的快捷键是ctrl+n。但是用户需要保存时才可修改名称以及文件路径。但是安装完AdvanceNewFile插件后，一切都会变得相当容易。
按着ctrl+alt+n ,下方会出现一个填写路径的框，你可在内直接填写文件名，将文件保存在默认路径；也可自己编写路径保存

##babel
支持ES6， React.js, jsx代码高亮，对 JavaScript, jQuery 也有很好的扩展。

##Alignment
使”=”号对齐，变量定义太多，长短不一，可一键对齐,默认快捷键Ctrl+Alt+A和QQ截屏冲突，可设置其他快捷键如：Ctrl+Shift+Alt+A；先选择要对齐的文本

##Clipboard History
**功能：**粘贴板历史记录.

**简介：**方便使用复制/剪切的内容.

**使用：**.

Ctrl+alt+v：显示历史记录.

Ctrl+alt+d：清空历史记录.

Ctrl+shift+v：粘贴上一条记录（最旧）.

Ctrl+shift+alt+v：粘贴下一条记录（最新）.


##IMESupport
**功能：**sublime中文输入法.

**简介：**还在纠结 Sublime Text 中文输入法不能跟随光标吗？试试「IMESupport 」这个插件吧！目前只支持 Windows，在搜索等界面不能很好的跟随光标.

**使用：**Ctrl + Shift + P →输入pci →输入IMESupport →回车.



##Trailing spaces
**功能：**检测并一键去除代码中多余的空格.

**简介：**在纠结代码中有多余的空格而显得代码不规范？或是有处女座情节？次插件帮你实现发现多余空格、一键删除空格、保存时自动删除多余空格，让你的代码规范清爽起来.

**使用：**安装插件并重启，即可自动提示多余空格。一键删除多余空格：CTRL+SHITF+T（需配置），更多配置请点击标题。快捷键配置：在Preferences / Key Bindings – User加上代码（数组内）.
