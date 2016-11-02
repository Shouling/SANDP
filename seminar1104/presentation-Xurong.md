##[The Cracked Cookie Jar: HTTP Cookie Hijacking and the Exposure of Private Information](http://www.cs.columbia.edu/~angelos/Papers/2016/cookiejar.pdf)
#####*---IEEE Symposium on Security and Privacy 2016*
###authors: *Suphannee Sivakorn, Iasonas Polakis and Angelos D. Keromytis*
###speaker: *Li Xurong*
###slides:you can click [here](https://www.blackhat.com/docs/us-16/materials/us-16-Sivakorn-HTTP-Cookie-Hijacking-In-The-Wild-Security-And-Privacy-Implications.pdf)

###abstract: 
   * 随着人们对在线隐私的重视，而对流行网站进行**session** 劫持的攻击层出不穷，这也催生了*HTTPS*的部署。然而，许多网站出于性能和兼容性的考虑仍然不采用无处不在的加密。一般采取的做法是对部分关键功能和敏感数据访问进行加密连接，对于其他的一些无关紧要的功能或数据通过*HTTP*访问。实际上，这种做法是容易产生缺陷导致敏感信息和功能泄露给第三方。

* 这篇文章中，作者对不同主要网站集合进行了一个深度评估，并调查分析了攻击者可以利用用户*http cookie*劫持获得的一些敏感信息和功能。很多网站部分部署HTTPS，个性化服务不经意地泄露隐私信息，同样的，多个不同范围的*cookie*和内部依赖的功能隔离使得情况更加复杂。文中的*cookie*劫持研究显示了很多缺陷：攻击者可以获取用户的家庭和工作地址，谷歌，必应，和百度的浏览网站暴露了用户的完整的搜索历史，以及雅虎允许攻击者抽取联系人名单，并用用户的账户发邮件。此外，像亚马逊和eBay这样的电子商务平台部分或者全部地泄露用户的购买记录,几乎每个网站泄露用户名和邮箱地址。广告网络像**Doubleclick**也泄露用户浏览过的网页。为了评估*cookie*劫持的实际情况和程度，作者研究了在线系统的多个方面，包括移动应用，浏览器安全机制，插件，和搜索栏。作者在大学校园的公共无线网络的子网上进行了30天的数据搜集和安全评估，检测出了超过**282K**个账户泄露了攻击者可以用来攻击的*cookie*，文中也研究了用户保护自己的方式。但是尽管像**HTTPS everywhere extension**可以减少攻击面，但是*http cookie*仍然可以泄露。当这些攻击的隐私问题可以用来对Tor用户进行去匿名化时，这个问题变得更加严重。这篇论文的评估显示很大一部分Tor用户或许被*cookie*劫持攻击。


###thinking:
日常上网的各种服务都可能存在cookie劫持和个人隐私信息泄漏的情况，尽管存在一些安全机制，如HTTPS，[HSTS](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security)，[HPKP](https://en.wikipedia.org/wiki/HTTP_Public_Key_Pinning)，cookie的secure安全属性，但是由于各种实际情况的考虑，如性能下降，成本剧增，为了兼容老用户等等方面，实际部署中存在很多问题，使得这些安全机制没有达到预期的功效。这篇论文就是从一些现象深度挖掘用户隐私泄露的现象，揭露了这一严重的安全隐患。安全机制的设计固然很难直接找到问题，但是在实际部署中包括实现就存在很多的问题，这是一种思路，如[TLS证书认证的实现](http://www.cs.utexas.edu/~shmat/shmat_ccs12.pdf)，[cookie安全属性的实现](https://www.usenix.org/system/files/conference/usenixsecurity15/sec15-paper-zheng-updated.pdf)，[HTTPS的部署代理问题](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.156.6830&rep=rep1&type=pdf)等。