<h1 align="center">🔍 如何捕捉 NSO Group 的 Pegasus</h1>


### 简介

NSO Group 声称其 Pegasus 间谍软件仅用于“调查恐怖主义和犯罪”，并且“不留任何痕迹”。
这份取证方法报告表明，这两项声明均不属实。本报告随 Pegasus Project 的发布而公布，
该项目是一项协作调查，涉及来自 10 个国家、17 家媒体组织的 80 多名记者，由 Forbidden Stories 协调，并由“国际特赦组织安全实验室 (Amnesty International’s Security Lab)”* 提供技术支持。

### 为什么？

然而，在进一步分析中，我们* 还注意到了可疑的重定向。通过取证工作，我们至少可以利用这些信息来拦截某些域名和 DNS。这将增加 Pegasus 与 NSO Group 的 C&C 服务器通信的难度。


### 目的？

这是一个从国际特赦组织安全实验室收集的域名和 DNS 列表。

🔗 您可以在此处查看详细的分析报告：

    https://www.amnesty.org/en/latest/research/2021/07/forensic-methodology-report-how-to-catch-nso-groups-pegasus/

### PiHole/Adguard Home

该列表可以添加到 pihole 中，从而提供一定程度的保护，以防止遭受攻击或接收来自其相应服务器的任何其他数据包。


## 其他来源

🔗    https://github.com/Red-Laboratory/NSO-hosts

🔗    https://github.com/jjjxu/NSO_Pegasus_Blocklist

🔗    https://github.com/AmnestyTech/investigations
