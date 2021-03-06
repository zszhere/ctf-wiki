# CTF 竞赛模式简介

## 解题模式 - Jeopardy

解题模式（Jeopardy）常见于线上选拔比赛。在解题模式 CTF 赛制中，参赛队伍可以通过互联网或者现场网络参与，参数队伍通过与在线环境交互或文件离线分析，解决网络安全技术挑战获取相应分值，与 ACM 编程竞赛、信息学奥赛比较类似，根据总分和时间来排名。

相不同的是解题模式一般会设置**一血**、**二血**、**三血**，也即最先完成的前三支队伍会获得额外分值，所以这不仅是对首先解出题目的队伍的分值鼓励，也是一种团队能力的间接体现。

当然还有一种流行的计分规则是设置每道题目的初始分数后，根据该题的成功解答队伍数，来逐渐降低该题的分值，也就是说如果解答这道题的人数越多，那么这道题的分值就越低。最后会下降到一个保底分值后便不再下降。

题目类型主要包含 **Web 网络攻防**、**RE 逆向工程**、**Pwn 二进制漏洞利用**、**Crypto 密码攻击**、**Mobile 移动安全**以及 **Misc 安全杂项**这六个类别。

## 战争分享模式 - Belluminar

在 2016 年世界黑客大师挑战赛（WCTF）国内首次引入韩国 POC SECURITY 团队开创的 BELLUMINAR CTF （战争与分享）赛制，从此国内陆陆续续也有开始 BELLUMINAR 模式的比赛，目前采取这一赛制的有 2016 年诸葛建伟老师集合的 XMan 夏令营分享赛以及同年 9 月的「百度杯」CTF 比赛。

同时这里也有 BELLUMINAR 赛制的介绍官网：[http://belluminar.org/](http://belluminar.org/)

### 赛制介绍

> Belluminar, hacking contest of POC, started at POC2015 in KOREA for the first time. Belluminar is from 'Bellum'(war in Latin) and 'seminar'. It is not a just hacking contest but a kind of festival consisted of CTF & seminar for the solution about challenges. Only invited teams can join Belluminar. Each team can show its ability to attack what other teams want to protect and can defend what others want to attack.

如官网介绍这样，BELLUMINAR CTF 赛制由受邀参赛队伍相互出题挑战，并在比赛结束后进行赛题的出题思路，学习过程以及解题思路等进行分享。战队评分依据出题得分，解题得分和分享得分进行综合评价并得出最终的排名。

### 出题阶段

> Each team is required to submit 2 challenges to the challenge bank of the sponsor.

首先各个受邀参赛队伍都必须在正式比赛前出题，题量为 2 道。参赛队伍将有 12 周的时间准备题目。出题积分占总分的 30%。

> Challenge 1: must be on the Linux platform; 
>
> Challenge 2: No platform restriction(except Linux) No challenge type restriction (Pwn, Reverse…)

传统的 BELLUMINAR 赛制要求出的两道题中一道 Challenge 必须是在 Linux 平台，另外一个则为非 Linux 平台的 Challenge。两个 Challenge 的类型则没有做出限制。因此队伍可以尽情展现自己的技术水平。

为使比赛题目类型比较均衡，也有采用队伍抽签出题的方式抽取自己的题，这要求队伍能力水平更为全面，因此为了不失平衡性，也会将两道 Challenge 的计入不同分值（比如要求其中一道 Challenge 分值为 200，而另外一道分值则为 100）。

### 提交部署

题目提交截止之前，各个队伍需要提交完整的出题文档以及解题 Writeup，要求出题文档中详细标明题目分值，题面，出题负责人，考察知识点列表以及题目源码。而解题 Writeup 中则需要包含操作环境，完整解题过程，解题代码。

题目提交之后主办方会对题目和解题代码进行测试，期间出现问题则需要该题负责人配合解决。最终部署到比赛平台上。

### 解题竞技

进入比赛后，各支队伍可以看到所有其他团队出的题目并发起挑战，但是不能解答本队出的题目，不设置 First Blood 奖励，根据解题积分进行排名。解题积分占总分的 60%。

### 分享讨论

比赛结束后，队伍休息，并准备制作分享 PPT （也可以在出题阶段准备好）。分享会时，各队派 2 名队员上台进行出题解题思路，学习过程以及考察知识点等的分享。在演示结束后进入互动讨论环节，解说代表需要回答评委和其他选手提出的问题。解说没有太大的时间限制，但是时间用量是评分的一个标准。

### 计分规则

出题积分（占总分 30%）有 50%由评委根据题目提交的详细程度，完整质量，提交时间等进评分，另外 50%则根据比赛结束后最终解题情况进行评分。计分公式示例：Score = MaxScore – | N – Expect＿N |。这里 N 是指解出该题的队伍数量，而 Expect＿N 则是这道题预期应该解出的题目数量。只有当题目难度适中，解题队伍数量越接近预期数量 Expect＿N，则这道题的出题队伍得到的出题积分越高。

解题积分（占总积分 60% ）在计算时不考虑 First Blood 奖励。

分享积分（占 10% ）由评委和其他队伍根据其技术分享内容进行评分（考虑分享时间以及其他限制），计算平均值得出。

### 赛制总评

赛制中将 Challenge 的出题方交由受邀战队，让战队能尽自己所能互相出题，比赛难度和范围不会被主办方水平限制，同时也能提高 Challenge 的质量，每个战队都能有不一样的体验与提升。在”分享”环节，对本队题目进行讲解的同时也在深化自己的能力水平，在讨论回答的过程更是一种思维互动的环节。在赛后的学习总结中能得到更好的认知。


## 攻防模式 - Attack & Defense

攻防模式常见于线下决赛。在攻防模式中，参赛队伍在网络空间互相进行攻击和防守，挖掘网络服务漏洞并攻击对手服务来得分，修补自身服务漏洞进行防御来得分（当然有的比赛在防御上不设置得分，防御只能避免丢分）。攻防模式 CTF 赛制可以实时通过得分反映出比赛情况，最终也以得分直接分出胜负，是一种竞争激烈，具有很强观赏性和高度透明性的网络安全赛制。在这种赛制中，不仅仅是比参赛队员的智力和技术，也比体力（因为比赛一般都会持续 48 小时及以上），同时也比团队之间的分工配合与合作。

接下来讲讲攻防模式的具体情况：

一般比赛的具体环境会在开赛前约半小时由比赛主办方给出（是一份几页的小文档）。在这半小时内，你需要根据主办方提供的文档熟悉环境并做好防御。

首先需要接入比赛环境，主办方会提供网线与网线接口转换器（比如 Mac 电脑需要使用，如果主办方没有提供的话，那就需要你自备了。存在此问题的小伙伴可以注意一下）。文档上会提供网线连接需要填写的 **IP 地址、网关、掩码、DNS 服务器地址**用于连接网络。

文档上会明确给出**参赛队伍所在 IP 网段**、**比赛答题平台**、**己方 Gamebox 的 IP 地址**、**登录用户名密码**以及**敌方 Gamebox 所在 IP 网段**。

文档上一般都会有比赛环境的**网络拓扑图**（如下图），每支队伍会维护若干的 **Gamebox（己方服务器）**，Gamebox 上部署有存在漏洞的服务。参赛队伍使用文档提供的用户名密码登录比赛答题平台和 Gamebox。

![攻防模式网络拓扑](/introduction/images/network.jpg)

在比赛开始前半小时，这半小时内是无法进行攻击的，各支队伍都会加紧熟悉比赛网络环境，并做好防御准备。至于敌方 Gamebox 的 IP 地址，则需要靠你自己在给出网段中发现。

比赛过程中，一般每轮大约是 3 - 5 分钟时间。你需要写脚本自动提交到答题平台（手动提交也行）上得分。每支队伍都会有一定的初始得分（一般初始得分相同，如果赛前会相应考核，那么会根据赛前考核成绩设置攻防赛的初始得分）Gamebox 状态分为三种， **正常、攻陷、不可用**。Gamebox 中的 flag 也会每轮进行刷新。

比赛过程中有裁判系统每轮都会进行评定。


* 如果一轮过去，Gamebox 表现正常，那么裁判系统会根据本轮未被攻陷的 Gamebox 情况给予防御得分
* 如果防御过于严格，无法通过裁判系统的**漏洞服务可用性判定**的话，该轮会被裁判系统认定为该 Gamebox 不可用（视为宕机）。本轮直接失分。
* 如果 Gamebox 被攻陷（有队伍提交了你们队 Gamebox 上随机生成的 flag），那么裁判系统会给予该队攻击得分。
* 一轮下来，由成功攻陷该 Gamebox 的队伍平分攻陷得分。

如果是分为上午下午两场攻防赛的话，那么上午和下午的 Gamebox 漏洞服务会更换（避免比赛中途休息时选手交流），但管理时要用的 IP 地址什么的不会改变。也就是**下午会换新题**。
