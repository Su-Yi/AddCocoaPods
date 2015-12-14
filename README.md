# AddCocoaPods
CoacoPods 安装流程

【CocoaPods是什么】

当你开发iOS应用时，会经常使用到很多第三方开源类库，比如JSONKit，AFNetWorking等等。可能某个类库又用到其他类库，所以要使用它，必须得另外下载其他类库，而其他类库又用到其他类库，“子子孙孙无穷尽也”，这样手动一个个去下载所需类库十分麻烦。而且，你项目中用到的类库有更新，你必须得重新下载新版本，重新加入到项目中，十分麻烦。CocoaPods的出现，就很好的解决了这些繁琐的问题。

【CoacoPods安装】

如果你在天朝，在终端中敲入下面这个命令之后，会发现半天没有任何反应。原因是GFW那堵墙阻挡了cocoapods.org。

sudo gem install cocoapods



但是，我们可以用淘宝的Ruby镜像来访问cocoapods。按照下面的顺序在终端中敲入依次敲入命令：

gem sources --remove https://rubygems.org/



等有反应之后再敲入以下命令   ps：很多文章用的是http的地址，现在用这个会变成404，所以要用https。

gem sources -a https://ruby.taobao.org/ 




为了验证你的Ruby镜像是并且仅是taobao，可以用以下命令查看：

gem sources -l




只有在终端中出现下面文字才表明你上面的命令是成功的：

*** CURRENT SOURCES ***

http://ruby.taobao.org/




这时候，你再次在终端中运行：

sudo gem install cocoapods




等上十几秒钟，CocoaPods就可以在你本地下载并且安装好了，不再需要其他设置。




如果gem太老，可以用如下命令升级gem：

sudo gem update —system
