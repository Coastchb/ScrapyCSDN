# ScrapyCSDN
### Why write the script？

主要是因为看到有部分博主为了刷访问量，都在写一些很通俗易懂的博客，希望可以通过写刷浏览量的脚本，告诉大家其实还是应该回归写博客的初心。

-------------------------------------------------------------

### How to use it ?

首先需要有python3版本及以上和pip

安装相关库命令如下：

```pip install pyquery```

```pip install requests```

```pip install bs4```

然后调用该类的代码如下：

```python
mycsdn = ScrapyMyCSDN('') #初始化类 参数为博客名
cur_write_nums = mycsdn.getOriginalArticalNums() #得到写了多少篇文章
cur_blog_page = mycsdn.getScrapyPageNums(cur_write_nums) #cur_blog_page:返回需要爬取的页数

# range为次数，这个由自己定 本人不建议写太多次，担心封号
for i in range(1,60):
    mycsdn.beginToScrapy(cur_blog_page) #进行访问
    time.sleep(10) # 给它休息时间 还是怕被封号的
```



### What it can improve?

这个是V1.0.0版本 还存在一些有待完善的地方，比如如何设置不同ip 以及访问时长的限制。 这个还是等以后再完善。

希望被引用的话 可以附上本人的相关github账号。分享不易，且珍惜！ 