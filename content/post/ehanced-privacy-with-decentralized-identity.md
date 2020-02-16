+++
authors = []
date = 2019-11-16T16:00:00Z
draft = true
excerpt = "2019 年 11 月 17 日，Dimension 受邀参加了 2019 成都 Web 全栈大会，Jack Works（ Dimension 现代前端魔法使 ）在全栈大会上发表了“ Enhanced Privacy with Decentralized Identity ”的演讲，向前来现场的程序员小哥哥，小姐姐们从技术角度讲解了 Maskbook 的技术原理。"
hero = "/uploads/hero-3.jpg"
title = "Ehanced Privacy with Decentralized Identity"
+++

2019 年 11 月 17 日，Dimension 受邀参加了 2019 成都 Web 全栈大会，Jack Works（ Dimension 现代前端魔法使 ）在全栈大会上发表了“ Enhanced Privacy with Decentralized Identity ”的演讲，向前来现场的程序员小哥哥，小姐姐们从技术角度讲解了 Maskbook 的技术原理。

Maskbook 是一个浏览器插件，可以让用户在正常使用 Facebook 、Twitter 等社交网络的情况下，保护用户的个人隐私。为此，Maskbook 使用了密码学原理（对称加密和非对称加密），帮助 Maskbook 的用户对他们的数据进行加密处理，避免大平台滥用用户的数据隐私以达到盈利的目的。同时使用了许多前端技术来确保去中心化和隐私安全，包括了 GunDB （一个去中心化图数据库），@holoflows/kit （一个自己造的浏览器扩展开发工具包）、ShadowRoot（ Web 标准 ）。

Maskbook 是由 Dimension 公司开发的开源浏览器插件，是不受政府，组织控制的。当初想要开发 Maskbook 的原因是因为 Facebook 窃取用户数据，贩售数据以达到谋取利润的目的，更甚的是利用这些数据影响政治，操控大选。所以 Dimension 想在 Facebook 上添加一层，用科技手段来组织头部的互联网企业滥用用户隐私，将数据的控制权回归于用户自己。当然 Maskbook 的使用者也无需担心开发人员会在背后使用用户的数据隐私，整个开发的过程也是透明公开的。

Maskbook 的原理 Maskbook 使用了 对称加密 和 非对称加密 的组合。在图中可以看到，比如 Alice 在 Facebook 上创建了一条 post，在 Maskbook 使用过程中，每一条 post 都由一个 AES key 用来加密，最后呈现在 Facebook 主页上的就是一段加密的文字。每一个 AES key 都由 ECDH 加密给指定的接收人，最后在 GunDB 中同步。

注：ECDH ( Elliptic Curve Diffie Hellman )是一种能够让拥有各自的椭圆曲线私钥并知道对方公钥的两方在不安全信道中计算出同一个密文的方法。
