# GGMod
提供GameGuardian的MOD教程和代码，如luajava库、修复os.execute函数、完善String库、添加Canvas等。

2021.10.01开始不定时更新

# 手机端工具
<p>MT文件管理器.apk</p>
<p>AIDE.apk</p>
<p>GameGuardian.apk</p>

# 语言
主要涉及以下语言
<p>Lua</p>
<p>LuaJ</p>
<p>LuaJava</p>
<p>Java</p>

# 模板
<p>由于luajava没法提供方便的String类都交互，所以我们需要对String类中的一些方法进行封装，并将它加入_G全局表中的string库里</p>
<p>StringLib.java类为luaj原String库编写方式的模板（不是我封装好的那个StringLib的源码），参考该编写方式可有效学习函数封装方法</p>
<p>https://github.com/JealousCat/GGMod/blob/main/StringLib.java</p>

# 美化教程
注：指对非函数库类功能或UI界面等进行更改，使得修改器使用体验更好，界面更美观

<p><a href="https://alywp.net/35mDO4">一、更改安装包包名，同时可以起到去除随机安装的作用</a></p>
<p><a href="https://alywp.net/5bzBxRoW">二、更换修改器图标</a></p>
<p><a href="https://alywp.net/VYt9B">三、桌面图标两个变一个</a></p>
<p><a href="https://alywp.net/2i2gJg">四、通过arsc文件精简安装包大小</a></p>
<p><a href="https://alywp.net/3olKpw">五、通过res文件精简安装包大小</a></p>
<p><a href="https://alywp.net/46L2QB">六、通过dex文件精简安装包大小</a></p>
<p><a href="https://alywp.net/3FI6PT">七、去除脚本执行结束时的“脚本已结束：”字样，方便复制结束内容</a></p>
<p><a href="https://alywp.net/3mSuk5">八、UI图标美化</a></p>
<p><a href="https://alywp.net/6XmSy4">九：设置彩色描边透明背景弹窗</a></p>
<p><a href="https://alywp.net/2EKe3V">十、去除搜索列表、保存列表的说明文字</a></p>



# 函数添加教程
注：指将编译好的函数文件添加到GG修改器的函数库中
<p><a href="https://github.com/JealousCat/GGMod/blob/main/Luajava.dex">luajava.dex文件下载</a></p>
LuaJava库将原官方的Loadlib更换为LoadDex，新增luajava.astable、luajava.toArray、luajava.methods。具体用法在后续教程中体现，或使用jadx查看java代码
<p><a href="https://alywp.net/2KzA5a">一、添加luajava库，用于lua与java交互，并可使用java方法</a></p>
<p><a href="https://alywp.net/7I7PeA">二、添加String库，在原有基础上完善</a></p>

# 函数编写教程
注：指函数源码编写过程，可学习LuaJ和luajava的API
<p><a href="https://alywp.net/19f22g">一、安装手机端AIDE</a></p>
<p><a href="https://alywp.net/6sngOO">二、编写一个StringUtils调试luajava库</a></p>
三、String库的完善与相关函数编写
<p><a href="https://alywp.net/4woqss">①主要讲解LuaValue.valueOf的使用</a></p>
<p><a href="https://alywp.net/6DceDH">②展示一些函数的编写过程</a></p>
<p><a href="https://alywp.net/7I7PeA">③教学封装StringLib的函数如何与原库合并</a></p>
新增内容如下：
<p></p>string.compare、string.endsWith、string.equals、string.hashCode、string.intern、string.startsWith、string.split、string.toCharArray、string.trim、string.delet、string.insert、string.setCharAt、string.newString、string.isLetter、string.isDigit、string.isUpper、string.isLower、string.toUpper、string.toLower<p></p>
用法可参考Java原方法，或者查看StringLib.dex的源码来学习函数用法
