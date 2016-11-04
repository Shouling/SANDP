# Paper: Forwarding-Loop Attacks in Content Delivery Networks
> NDSS 2016

# Speaker: Xiang LING

# introduction
CDN（Content Delivery Networks）目前被广泛运用于互联网中，用来解决网站的性能、安全和可靠性等问题。更具体地讲，CDN通过缓存网站内容提升网站性能；通过过滤恶意请求来提升网站安全性(Web应用防火墙，即 WAF)；并通过提供丰富的带宽和计算资源来化解分布式拒绝服务（DDoS）攻击。CDN 已经逐渐演化成互联网重要的基础设施，承载着主流网站的Web访问流量。然而，CDN本身的安全，尤其是 CDN 本身的可用性（Availability) 没有被系统地研究过。

作者对 CDN 本身的可用性做了系统的研究。通过对16个商业CDN厂家的大量实际测试，他们发现，作为目前网站加速和防范 DDoS 攻击的最佳实践，CDN本身存在着严重的结构性问题，使得CDN本身可以成为DoS 攻击的对象。由于CDN的客户可以控制CDN转发的目标，恶意的客户可以利用该控制权来配置恶意的转发规则，让CDN在转发用户请求时形成环路，从而消耗CDN的资源（如可用TCP端口、CPU、带宽等）。利用转发循环攻击的放大效应（Amplification），攻击者只需要非常有限的网络带宽就可能大量消耗CDN的资源从而影响它的可用性。研究者发现，目前尽管有部分 CDN厂商已采取了一些措施防止循环攻击，但这些防御措施都可以被绕过。研究者把这种攻击称为CDN转发循环（Forwarding Loop）攻击，从简单到复杂可以构造CDN节点自循环（Self Loop）、同一CDN内的多节点循环（Intra-CDN loop)、多CDN厂商多节点循环（Inter-CDN loop）以及高级的大坝攻击（Dam flooding attack)和gzip炸弹攻击，最终可能导致对多个CDN厂商大规模的拒绝服务攻击，从而严重威胁互联网基础设施的安全。
# Thinking
这篇文章跟今年该团队在CCS上发表的思想一致，致力于发现和解决协议的实际实现中出现的各种问题，佐以充分的攻击设计于实验去证明。