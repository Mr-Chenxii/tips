## 什么是cookie

Cookies就是服务器暂存放在你的电脑里的资料（.txt格式的文本文件），好让服务器用来辨认你的计算机，某些网站为了辨别用户身份、进行[session](https://baike.baidu.com/item/Session/479100)跟踪而储存在用户本地终端上的数据（通常经过加密）。定义与RFC2109和2965都已废弃，最新取代的规范是RFC6265。本文简单介绍什么是cookies,cookies有什么作用，以及网站利用cookie存在什么问题。

1. 什么是Cookies呢？

什么是Cookies（“小甜饼”）呢？简单来说，Cookies就是服务器暂存放在你的电脑里的资料（.txt格式的文本文件），好让服务器用来辨认你的计算机。当你在浏览网站的时候，Web服务器会先送一小小资料放在你的计算机上，Cookies 会帮你在网站上所打的文字或是一些选择都记录下来。当下次你再访问同一个网站，Web服务器会先看看有没有它上次留下的Cookies资料，有的话，就会依据Cookie里的内容来判断使用者，送出特定的网页内容给你。

2. cookies有什么作用呢？

现在上许多网站都有新用户注册这一项，有时注册了一下，等到下次再访问该站点时，会自动识别到你，并且向你问好，是不是觉得很亲切？当然这种作用只是表面现象，更重要的是，网站可以利用cookies跟踪统计用户访问该网站的习惯，比如什么时间访问，访问了哪些页面，在每个网页的停留时间等。利用这些信息，一方面是可以为用户提供个性化的服务，另一方面，也可以作为了解所有用户行为的工具，对于网站经营策略的改进有一定参考价值。例如，你在某家航空公司站点查阅航班时刻表，该网站可能就创建了包含你旅行计划的Cookies，也可能它只记录了你在该站点上曾经访问过的Web页，在你下次访问时，网站根据你的情况对显示的内容进行调整，将你所感兴趣的内容放在前列。这是高级的Cookie应用。**目前Cookies 最广泛的应用是记录用户登录信息**，这样下次访问时可以不需要输入自己的用户名、密码了——当然这种方便也存在用户信息泄密的问题，尤其在多个用户共用一台电脑时很容易出现这样的问题。

3. cookies存在的问题

另外，有人认为网站利用cookies可能存在侵犯用户隐私的问题，但由于大多用户对此了解不多，而且这种对用户个人信息的利用多数作为统计数据之用，不一定造成用户的直接损失，因此现在对于cookies与用户隐私权的问题并没有相关法律约束，很多网站仍然在利用cookie跟踪用户行为，有些程序要求用户必须开启cookie才能正常应用。IE浏览器用户可以通过“隐私”选项中的隐私设置的高低来决定是否允许网站利用cookie跟踪自己的信息，从全部限制到全部允许，或者限制部分网站，也可以通过手动方式对具体的网站设置允许或者禁止使用cookies进行编辑。IE浏览器的默认设置是 “中级”－对部分网站利用cookie有限制。

---

Cookie是由服务端生成，发送给User-Agent，User-Agent会将Cookie的key/value保存到某个目录下的文本文件内，下次请求同一网站是就发送该Cookie给服务器（前提是浏览器设置为启用cookie）。

Cookie 在计算机中是个存储在浏览器目录中的文本文件，当浏览器运行时，存储在 RAM 中发挥作用 （此种 Cookies 称作 Session Cookies），一旦用户从该网站或服务器退出，Cookie 可存储在用户本地的硬盘上 （此种 Cookies 称作 Persistent Cookies） 。

设置浏览器是否启用cookies（默认为启用）

*浏览器>Internet属性>隐私页>高级*

![img](C:\Users\windows\Desktop\新建文件夹\cookie.png)

Cookie名称和值可以由服务器端开发自己定义，对于JSP而言也可以直接写入jsessionid，这样服务器可以知道该用户是否合法用户以及是否需要重新登陆等。

*个人理解为Cookie是用户登录信息的key，需要用key去request服务器。*

---

**PS：**JSP全称JavaServer Pages是由[Sun Microsystems](https://baike.baidu.com/item/Sun Microsystems)公司主导创建的一种[动态网页技术](https://baike.baidu.com/item/动态网页技术/9415956)标准。JSP部署于网络服务器上，可以响应客户端发送的请求，并根据请求内容动态地生成[HTML](https://baike.baidu.com/item/HTML)、[XML](https://baike.baidu.com/item/XML)或其他格式文档的[Web](https://baike.baidu.com/item/Web)网页，然后返回给请求者。JSP技术以[Java](https://baike.baidu.com/item/Java)语言作为[脚本语言](https://baike.baidu.com/item/脚本语言)，为用户的[HTTP](https://baike.baidu.com/item/HTTP)请求提供服务，并能与服务器上的其它Java程序共同处理复杂的业务需求。（Java服务器页面）

**PS：**jsessionid是一个Cookie，Servlet容器（比如tomcat,jetty）用来记录用户session。是创建会话时，即调用request.getSession()时候，种下的一个Cookie，写在内存中。

---

服务器可以利用Cookies包含信息的任意性来筛选并经常性维护这些信息，以判断在HTTP传输中的状态。Cookies最典型的应用是判定注册用户是否已经登录网站，用户可能会得到提示，是否在下一次进入此网站时保留用户信息以便简化登录手续，这些都是Cookies的功用。另一个重要应用场合是“购物车”之类处理。用户可能会在一段时间内在同一家网站的不同页面中选择不同的商品，这些信息都会写入Cookies，以便在最后付款时提取信息。

Cookie可以保持登录信息到用户下次与服务器的会话，换句话说，下次访问同一网站时，用户会发现不必输入用户名和[密码](https://baike.so.com/doc/5387348-5623878.html)就已经登录了（当然，不排除用户手工删除Cookie）。而还有一些Cookie在用户退出会话的时候就被删除了，这样可以有效保护个人隐私。

Cookie在生成时就会被指定一个Expire值，这就是Cookie的生存周期，在这个周期内Cookie有效，超出周期Cookie就会被清除。有些页面将Cookie的生存周期设置为“0”或负值，这样在关闭页面时，就马上清除Cookie，不会记录用户信息，更加安全。

## cookie和session有什么区别

session是一次浏览器和服务器的交互的会话，会话是啥呢？就是我问候你好吗？你回恩很好。就是一次会话，那么对话完成后，这次会话就结束了。session就负责把这次的会话储存下来。

session会在cookie中储存一个Jsessionid的东西来标识每个用户，然后会在本地生成对应ID的文件来储存相应的值，与之前的cookie相比多了不少安全性。

**Session和Cookie的主要区别**

- Cookie是把用户的数据写给用户的浏览器。
- Session技术把用户的数据写到用户独占的session中。
- Session对象由服务器创建，开发人员可以调用request对象的getSession方法得到session对象。