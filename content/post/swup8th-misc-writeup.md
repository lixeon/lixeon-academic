---
title: "SWPU 第八届CTF Web社工题Write Up"
date: 2017-11-06T12:00:06+09:00
summary:  " "
tags: 
- ctf
- misc
- sec
---

作为一个小菜鸡跟着大佬们打了一场ctf，感谢西南石油大学提供的平台、耐心的客服和优质的题目。

除了签到题外，我只做出了一道社工题。其他的题对于我这样的萌新实在是太不友好了！

那么题目如下：

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106124548-300x203.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106124548-300x203.png)

打开链接后是一个黑页，而且还带有BGM。

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106124631-300x191.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106124631-300x191.png)

上面有一段英文，特别是还留了昵称和一串数字，不用想，是QQ号，那么就准备社工这个QQ号。

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106124748-300x233.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106124748-300x233.png)

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106124803-300x115.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106124803-300x115.png)

在个性签名和QQ空间里的一条说说中分别发现了密文，base64解码后，个性签名得到题目名（估计是嘲讽用的），说说里的得到一个链接，就是网站后台的链接。即所谓的小金库。

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106130114-300x224.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106130114-300x224.png)

嗯，是一个类似空间的东西，而且好多妹子图，出题人大概是没有女朋友吧。

用御剑扫目录，发现了后台。

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171102212739-300x187.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171102212739-300x187.png)

用户名很快就得到了，因为在邮件联系那写着sonic2011，然后就是找密码。

其实我早发现了邮件联系那对应的邮箱是sonic@163.com，然后去163找回密码，输入后说没有该用户名，我以为是出题人的烟雾弹，就没再管这个邮箱。

然后继续找密码，首先是妹子图对应的源码有一个瀑布流，然后还有一个tips，以为是照片顺序的数字的排列组合，被坑了好久。

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106130527-300x203.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106130527-300x203.png)

接着又被黑页的BGM坑了好一会，因为网站关闭了右键，那么就简单的加上view-source查看html源代码。

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106124712-300x243.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171106124712-300x243.png)

发现了这个BGM，以为是MP3隐写，然后并没有发现什么，倒是在MP3属性里发现了一串163key，在知乎上看到说这是网易云音乐的特定加密，这才认为这个BGM是正常的，密码并在这里。

最后还是队友提示，利用社工库社工了一下上面说的邮箱，这个社工库未注册只能查到，但不能全部显示，故要注册一个账号。

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171102213234-300x54.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171102213234-300x54.png)

注册界面藏在这里。有了账号再查询一次。

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171102212727-264x300.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171102212727-264x300.png)

啊哈，清楚的找到了密码，一看便知是MD5加密的，找了几个在线解密，得到了密码2010sonic。

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171102213046-300x137.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E6%88%AA%E5%9B%BE20171102213046-300x137.png)

成功登录，拿到了flag。

![http://lixeon.site/wp-content/uploads/2017/11/QQ%E5%9B%BE%E7%89%8720171106131113-300x207.png](http://lixeon.site/wp-content/uploads/2017/11/QQ%E5%9B%BE%E7%89%8720171106131113-300x207.png)

最终团队得分。

第一次完整的按照预期的做出一道CTF的Web题，开心。

完结，撒花\\~

萌新在这里给师傅们加油。