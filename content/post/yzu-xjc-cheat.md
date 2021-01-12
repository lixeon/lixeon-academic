---
author: "82Flex"
title: "新锦成就业创业教育平台视频观看时长自动化方法 - From 82Flex"
date: 2017-09-24T12:00:06+09:00
summary: "扬州大学新锦成自动化学习方法"
tags: 
- yzu
- sec
---

又双叒叕到了一年一度锦成网创业教育学习的时间啦！～

同学们开不开森！

但是要学习这么多的视频，还不能加速、快进真的很难受啊～虽然没有广告这点还算良心。

但是我们是谁？之前就有学长为普渡天下苍生，公布了失传已久的武林秘籍，然而原网页404失踪多时，故小弟在此将其抄录，以供大家传阅。

大家在享受幸福生活的同时，勿忘学长无私奉献。

ps: 视频中的习题，常识题，不会百度即可；课后习题，点开后右键网页，查看源代码，Ctrl+F搜索table，然后你就能看到答案了

---

学长的秘籍如下：

# 半自动考试助手

[https://pan.baidu.com/s/12TSvpgQ0DRLdOwh-svb0Yg](https://pan.baidu.com/s/12TSvpgQ0DRLdOwh-svb0Yg) 密码：pdqh

**使用方法：**

运行程序，在地址栏中填写自己学校的锦成网分站地址，进入期末考试页面。
点击左下角分析答案，稍等片刻后答案会出现在左侧，按顺序填写并提交试卷即可。

# **刷视频代码**

```jsx
 **javascript:eval(function(p,a,c,k,e,r){e=function(c){return c.toString(a)};if(!''.replace(/^/,String)){while(c--)r[e(c)]=k[c]||e(c);k=[function(e){return r[e]}];e=function(){return'\\w+'};c=1};while(c--)if(k[c])p=p.replace(new RegExp('\\b'+e(c)+'\\b','g'),k[c]);return p}('n=c;1=4();i=3;e=0;5(i--){6.7({8:"9",b:"/2/d.f"+"?"+1,g:"h",j:k,l:m(a){o(a);e++;p(e>q){r.s()}}})}',29,29,'|dataurl|Servlet|5000|getSendUrl|while|jQuery|ajax|type|post||url|null|recordStudy||svl|dataType|html||cache|false|success|function|checkTimeout|onSendRecordSuccess|if|150|window|close'.split('|'),0,{}))**
```

**使用方法：**
登录 [http://yzu.njcedu.com/](notion://www.notion.so/lix3on/522bc9f5eb1146b2ae71b90f6429090d?v=daf7e23925ae4b428a999a22340b9703&p=83feb18457ac49209e857caf14fe0caf#)，选择视频打开，开始播放后，在地址栏粘贴代码。回车，若干秒后视频自动关闭，刷新任务，视频已看完。课间习题拖动进度条到指定位置，题目会自己蹦出来。

注意事项：

- 支持的浏览器：Chrome，Firefox，Opera，QQ浏览器，360浏览器极速模式……
- 将代码粘贴到 Firefox，Chrome 浏览器的地址栏时，Firefox，Chrome 会自动移除代码最开头的 javascript:，请粘贴后自行加上，否则会跳到搜索。
- 键入代码后回车会导致视频卡住但声音继续，可能会持续 5 - 30 秒左右，视频标签自动关闭后即代表刷视频完成。
- 如果键入代码回车后视频卡住超过 30 秒，标签仍未关闭，则表明刷视频失败。

原理：

该劫持手段利用了后端数据库记录验证时：

1. 比较的时间精确度不足（可在1秒钟内插入多条数据）。
2. 没有限制客户端请求频率。
3.  提交报告时间基准及终止时间计算逻辑有误。

缺点在于，刷视频过程中会向服务器后端发送大量垃圾请求，造成服务器负载加重，易被运维察觉。

解决方案：

限制来自客户端的请求频率。