## Requests库的详细安装过程

初学python的爬虫小白，认识和使用requests库是第一步。requests库包含了网页爬取的常用方法。

[那么如何安装requests库呢？](https://www.cnblogs.com/yangbiao6/p/11826203.html)

### 1. 检查是否安装过requests库：WIN键+R打开cmd，输入pip install requests，运行后查看。

我本人尝试之后发现失败，结果如图所示

![image](C:\Users\windows\Desktop\新建文件夹\pip1.png)

上网查阅资料后发现，我安装的是Vscode编译器，已经安装python拓展包。在Visual Studio2019中也安装过python，按理来说应该不会出错。

后面发现原因在于我没有将pip安装至系统环境变量中。

从C:\Program Files (x86)\Microsoft Visual Studio\Shared\Python37_64\Scripts中运行cmd，发现`pip install requests`是可用的。

此电脑>属性>高级系统设置>环境变量>path。将上面的地址添加进去即可。

成功后。

![image](C:\Users\windows\Desktop\新建文件夹\pip2.png)



---

PS：自己无意中又调用了一次`pip install requests`，发现电脑上的pip有多个版本，提示需要更新版本。

![image](C:\Users\windows\Desktop\新建文件夹\pip3.png)

​       小结：当电脑上安装的软件过多时，要记得查看是否调用到对应的版本，防止编程时出现意想不到的错误。



### 2.下载安装tar包。

若第一步的操作，回车后显示空格，则说明未安装requests，则前往[官网](https://pypi.org/project/pip/#files)下载安装tar包。

解压下载的tar包，将pip文件放在Python安装目录下的lib包内。

打开cmd命令管理器，输入pip install requests,检测是否安装成功。



## Requests安装成功后的调用

Request库的两个重要对象 Response对象和Request对象。

![img](https://img-blog.csdn.net/20181006141233100?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2tfa29yaXM=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)



Response对象常用的属性：

![img](https://img-blog.csdn.net/20181006141538847?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2tfa29yaXM=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)



分析网站的编码：

![img](https://img-blog.csdn.net/20181006142633106?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2tfa29yaXM=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)



Requests库的7个常用方法

```python
requests.request()  #构造一个请求，支撑以下各方法的基础方法
requests.get()      #获取HTML网页的主要方法，对应于HTTP的GET
requests.head()     #获取HTML网页头信息的方法，对应于HTTP的HEAD
requests.post()     #向HTML网页提交POST请求的方法，对应于HTTP的POST
requests.put()      #向HTML网页提交PUT请求的方法，对应于HTTP的PUT
requests.patch()    #向HTML网页提交局部修改请求，对应于HTTP的PATCH
requests.delete()   #向HTML页面提交删除请求，对应于HTTP的DELETE
```

---

实例调用：访问baidu。pip版本21.0.1，使用软件VScode

![img](C:\Users\windows\Desktop\新建文件夹\request调用成功.png)

