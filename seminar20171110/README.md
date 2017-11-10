## Online Tracking: 1 million site tracking measurement

[论文PDF](http://randomwalker.info/publications/OpenWPM_1_million_site_tracking_measurement.pdf)

[人家的网站](https://webtap.princeton.edu/)

[人家的Github](https://github.com/citp/OpenWPM)

[CCS 2016 Video (youtube)](https://www.youtube.com/watch?v=_mEIv9wOkro)

[Georgia Video 1h](https://smartech.gatech.edu/handle/1853/56426)

----

OpenWPM 对1百万网站使用的跟踪技术的测量
====
@(信息安全paper)[OpenWPM|tracking]

## Background

### 之前的发现

指纹技术（无状态）：在10万个浏览器中，80~90%的桌面浏览器和81%的手机浏览器有独一无二的指纹

### 可能被用来干啥 Personalization measurement

个性化广告；价格歧视，给不同的人不同的价格；搜索商品得到不同价格的结果；展示用户喜欢的资讯

Web security measurement. 类似的技术还可以用来评估web安全、找安全弱点、扩展插广告的行为……


## OpenWPM


特点：支持模块化、综合性和可持续性的测量；不改浏览器内核代码，容易维持

### 组件

#### Browser driver 
用selenium控制firefox，与使用PhantomJS相比，有更多真实浏览器的特性 如HTML5存储 视频音频、浏览器扩展如Flash、CSS 3-D、WebGL。否则就发现不了新的跟踪技术 用AudioContext API

使用真实的浏览器还能测试浏览器扩展和浏览器隐私保护设置的效果

#### Browser managers 

对Selenium再封装一层 将高层次的控制命令转为特定的Selenium子程序；也支持在没有图形界面的容器中用Xvfb跑

#### Task manager

当browser manager崩溃、超时或超内存的时候，保存浏览器的状态（cookie、浏览历史记录），kill进程，用相同的配置启动新的进程并载入状态

#### Data Aggregator

得到的数据标准化 就方便不同的研究人员分享数据和用到的代码

现在用SQLite存关系型数据（来自proxy和扩展），LevelDB存去重后的web内容

#### Instrumentation 
为研究人员提供三个层次的数据：

Disk Access（cookie、Flash存储）
HTTP Data（python Mitmproxy中间人 https自己签个证书加入信任）
Javascript Access ：基于Fourthparty，对各种接口改原型getter setter； 为了记录是哪个js调用的，抛出异常来检查stack trace，这种方法对99.9%的js文件都有效，即使minified或eval都行，这种方法改自Privacy Badger Firefox Extension




## 没看懂的
to emulate users browsing malicious web shells with the goal of detecting client-side homephoning [55]