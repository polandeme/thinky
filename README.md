thinky
======


弄了两天没有弄成功的页面  
---------------------------

####原因  
+ 本质就没有弄对，明明想建的是个人主页，却在开始的时候就在github上建的是项目页  
+ 再者对基本概念不太懂，git的基本使用的不太会如 `git reset`  `git add .` 最基本的`git commit` `git pull`  `git push` 都不太会，还有对git历史版本回复，git分支概念，git合并分支都不太了解。  
+ 由于第一个原因所以导致再怎么弄都没有办法，本地和远端只能有一个可以的，因为本地可以算是根目录`http://localhost:4000/`，而远端是二级目录[http://polandeme.github.io/thinky/](http://polandeme.github.io/thinky/)，虽然首页可以，但是生成的内容页面的地址是把二级的`/thinky`省略掉了，而在本地是可以的（本地是根目录），试了很多配置都不可以，问了一个qq上的朋友也是，也没有成功。  
最后在wx学长的帮助下知道了问题所在（新建的就不对，个人页面而非项目页面），所以就想是否可以判断是在本地还是远端，不过至今没解决。wx学长也提供了很多方法想  
用js等页面加载完后将 `/thingy` 补上去或者直接在生产的这里`{{ post.url }}`加上`/thinky`。但是感觉都麻烦，就回到了本质，做个人页面。  
+ 好了问题終於发现了，就回到个人页面上了，折腾了两天了不想再折腾了，就用`jekyll new` 新建了一个简单的页面，又遇到问题了。
`jekyll server`无法启动，[具体问题](http://stackoverflow.com/questions/16498287/jekyll-liquid-exception-cannot-load-such-file-yajl-2-0-yajl)  
按照上面的安装了ruby1.9然后重新安装jekyll（有时一串问题），在重重艰难下，jekyll重要成功了。OMG高兴早了，
启动后`http://localhost:4000/`是空白的，发现又有[问题](https://github.com/mojombo/jekyll/issues/1376)了o(╯□╰)o：  

> 下载DevKit解压到某个目录，比如 E:\devkit , 在该目录中运行如下命令：
  ` ruby dk.rb init `
  [Read more](http://blog.chengyunfeng.com/?p=437#ixzz2dS2CEetk)  
> 然后按照上面的方法删除一个版本。  

成功后有点小兴奋差点没跳起来-:D。  

+ 有高兴早了，不支持中文，如果页面中有中文就无法启动`liquid error: incompatible character encodings: UTF-8 and GBK `。
解决方法将jekyll安装目录中的convertible.rb文件中的`self.content = File.read(File.join(base, name))`(31行左右）改成`self.content = File.read(File.join(base, name), :encoding => "utf-8")`

这次总算是真的成功了。
####总结  

1. 遇到问题先找到问题，弄清楚出来什么问题将问题明确再去找解决方法  
2. 不要慌一步一步来，一次解决一个问题，最后就会全部解决掉的
3. 学会看文档，看别人的方法，昨天问的朋友是个就业的大神，问他的时候，他不是急于回答而是自己先找打方法，他给我发了github issue上的和我一样的问题，感觉很有帮助。仔细分析，看到别人的答案不要一闪而过，你是来找答案的，不是收集答案的，这样这个答案看一下，那个看一下最后越弄问题越多。先找到一个和自己问题一样的从头解决，实在不可以再找其他方法。
4. 学好英语，包括那位大神在内贺自己找的机会都是国外的解决方法，其实没有解决的很大的原因就是英语不好，今天慢慢的看下去几个，感觉真的很有帮助，虽然以前也知道看英语文档很重要，但今天体会更深，英语真的很重要。国外的环境真的很好，這次遇到的问题 有好几个都是jekyll[作者](https://github.com/parkr)参与讨论的。  
5. 不要太相信权威，一开始看的是教程，按照上面建的，但是更笨就不可以，耽误了很长时间，他们的不一定是对的，即使是对的也不一定适合你。有自己的思想，了解本质才是最重要的。  

####關鍵

`思考` `总结` `淡定` `专注`  `step by step`



