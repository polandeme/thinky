thinky
======

test

弄了两天没有弄成功的页面  
####原因  
+ 本质就没有弄对，明明想建的是个人主页，却在开始的时候就在github上建的是项目页  
+ 再者对基本概念不太懂，git的基本使用的不太会如 `git reset`  `git add .` 最基本的`git commit` `git pull`  `git push` 都  
不太会，还有对git历史版本回复，git分支概念，git合并分支都不太了解。  
+ 由于第一个原因所以导致再怎么弄都没有办法，本地和远端只能有一个可以的，因为本地可以算是根目录，而远端是二级目录[http://polandeme.github.io/thinky/](http://polandeme.github.io/thinky/)，虽然  
首页可以但是，生产的内容页面的地址是把二级的`thinky`省略掉了，而在本地是可以的（本地是根目录），试了很多配置都不可以，问了一个qq上的朋友也是，也没有成功。  
最后在wx学长的帮助下知道了问题所在（新建的就不对，个人页面而非项目页面），所以就想是否可以判断是在本地还是远端，不过至今没解决。wx学长也提供了很多方法想  
用js等页面加载完后将 `/thingy` 补上去或者直接在生产的这里`{{ post.url }}`加上`/thinky`。但是感觉都麻烦，就会到了本质，做个人页面。  
+ 好了问题发现了，就回到个人页面上了，折腾了两天了不想再折腾了，就用`jekyll new` 新建了一个简单的页面，又遇到问题了。
`jekyll server`无法启动，[具体问题](http://stackoverflow.com/questions/16498287/jekyll-liquid-exception-cannot-load-such-file-yajl-2-0-yajl)  
按照上面的安装了ruby1.9然后重新安装jekyll（有时一串问题），在重重艰难下，jekyll重要成功了。OMG高兴早了，
启动后`http://localhost:4000/`是空白的，看见后才发现又有问题了:  
> 下载DevKit解压到某个目录，比如 E:\devkit , 在该目录中运行如下命令：
  ruby dk.rb init
  Read more: http://blog.chengyunfeng.com/?p=437#ixzz2dS2CEetk
