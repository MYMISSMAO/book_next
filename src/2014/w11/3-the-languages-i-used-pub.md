---
title: 那些年，我追过的语言
author: [程序君]
keywords: [技术, 编程语言]
---

# 那些年，我追过的语言

程序君也年轻过，年轻的代价就是盲目追随。

从MS-DOS6.0开始，程序君就是微软的狂热拥趸。

这种狂热自win95走上高潮（有谁还记得win95光盘里带的Good Times的MV，请举手），历经《未来之路》，windows2000，最后在dotnet发布后到达顶峰。

那段时间，只要微软反对的，就是我反对的。

不喜欢Netscape Navigator，只因为IE；诅咒过SUN，对Java深恶痛绝，因为NC是PC的死敌，SUN妄图革微软的命；使用Visual Basic，啃MFC，不为别的，就因为powered by Microsoft。

但VB功能太弱（其实还是我水平太差），MFC太乱，以至于大二时，我在给人打工做软件的时候无奈地选择了Delphi。

虽然不怎么喜欢严谨的pascal，但Delphi有让我不得不用的理由。用它写代码清新明快，效率上甩了笨重的MFC几条街，速度上让VB相形见拙。在那个Wake On LAN才兴起不久的年代，我用dephi做的印象最深刻的一个小feature，是通过一台电脑打开（或者关闭）局域网内几十台电脑。看着自己的软件能『神奇』地唤醒机房里的一群电脑，别提多自豪了。

在我上大学的期间，做客户端软件（或者C/S结构的软件）虽然能赚钱，但已经渐渐不酷了，ASP的出现，让我的兴趣移师到web（那时时髦的叫法是：B/S）。ChinaRen的崛起让我萌生了做自己的班级主页的想法，但做出来的东西只能躺在硬盘上，在参加比赛的时候演示两下 —— 那时几乎没有免费的提供MSSQL的服务器，而我做的『网站』，无一不基于MSSQL或者其简化版。我像一只把头埋在沙子里的鸵鸟，把自己限制在自己构筑的程序世界。

后来DotNet带着微软的万千宠爱出炉，我第一时间接受了它。我一边玩着C#代码，一边继续无视如日中天的Java 2及NB哄哄的J2EE。C#很迷人，一下子让我有种想要扔掉delphi的赶脚，但无奈dotnet framework太大（而且相对较慢，当时），还在使用赛扬的客户无法接受。

程序员在世最痛苦的莫过于最爱的语言(C#)赚不了钱，不喜欢的语言（Pascal）却为你解决生计问题。

C#无法在我的兼职生涯中施展拳脚，只能作为又一个参赛语言或者研究院语言，被我拿着招摇撞骗（那时讲dotnet就好比现在的云计算，大数据，很容易把不懂的人侃晕），写着连我自己也不相信的虚拟企业信息集成系统，混各种核心期刊论文。

毕业后，本来想找份C#相关的工作，却阴差阳错地做了通讯领域，让C取代C#，成了我的主流语言。大学时我的C也就是个习题水平，做过最难的习题不过实现inode模拟一个简单的unix文件系统，然后提供几个shell命令能创建目录，创建和修改文件。到了工作岗位，socket，timer，hash table，ring才真正走出教科书；而伴随着通讯领域的工作，Linux则正式走入我的生活。

认识到了linux的强大和从骨子里透出来的美感，我从此与微软的技术渐行渐远，也离开了混迹多年的codeproject。

写C的日子是枯燥的，尤其是用C写protocol。完整写过的IGMPv3，大部分代码几乎都是不用太动脑子的从协议语言到C的翻译。

那两年正是互联网方兴未艾的时候。google正飞速发展，百度从新浪的搜索提供商（2B）开始寻求面向大众（2C），3721是浏览器的标配，而mediaWiki也随着wikipedia的走红而走红。写出mediaWiki的php，成了我闲暇研究的对象。那时LAMP开始成为时髦词汇，WAMP/Apache Friends为还在使用windows的人们上提供全套互联网开发环境。

后来我在做一个自动化测试系统时感受到了php的力不从心 —— 我缺一门好的胶水语言，在web和system间游刃。正巧坊间一直流传『真正的程序员用C，聪明的程序员用python』的偈子，于是我又学习了python。这下拼图完成了：我用php在前端接受用户提交的任务，用python读出任务，从clearcase中checkout对应的全套路由器代码，编译出image，然后使用pyserial（一个串口库，可以连路由器的串口）和pyexpect（expect的python封装）连上测试环境中的路由器加载编好的image，然后调用测试团队提供的自动测试脚本测试。

那时没有rabbitMQ这样的杀器，php和python之间的任务同步做得很土：php把任务插入到数据库，python程序死循环每30s从数据库中读任务。

后来我换到了现在所在的外企，很快在同事的推荐下小试了一阵QT，QT的slot和signal做得真心漂亮 —— 可惜那时客户端软件彻底从我的技能清单里被移除，我也就没有继续在QT上发力。

那段时间，C让我糊口，php让我保持和web的连接，而python，一直是我做各种小工具的最爱。

期间玩过drupal，symfony。看symfony的作者的screencast，才知道有种开发神器叫TextMate，有个程序员的电脑叫macbook。

symfony对我而言是个很好的布道师，它让我认识了Ruby on Rails和django（源自symfony和二者的对比）。

它的一个联系项目jobeet还为我日后为创业项目起名提供了思路 —— 对，toureet就是这么出来的，而且07年前后这个名字就横亘在我的脑海。这不算个很接地气的名字，但就像初恋一样让人挥之不去。

知道了Ruby on Rails后，我才意识到如今已经是RoR横扫一切的时代，几乎是个创业公司就在用RoR。JavaEye的Robin称自己几天就搭了JavaEye出来，我虽然不怎么混JavaEye，但这还是大大刺激了我一下，让我对Robin和RoR好顿膜拜。

但那时RoR内部分裂了有一段时间，社区正在开始思考如何让分裂的两个分支摒弃前嫌，在RoR3.0大一统。这让我好生郁闷：究竟是等还是不等那遥遥无期的RoR3？毕竟，之前symfony2已经狠狠地摆了我一道 —— 我在1.x上写的代码在2里无法运行，而且2的改动之大让我一时间无法适应。如果现在入手学习RoR2.x，会不会重蹈覆辙？

两权相害取其轻，我最终选择了django。

然后机缘巧合加各种必然，我走向了创业之路。

等我『毕』业时，我已经算是django和javascript的熟手。

javascript是个很有意思的存在。我大概在2000年左右抄（对，抄的）的第一段js是一个问候的代码，大致是检查当前时间，然后提供不同的问候语。很傻很天真。

那时的javascript恶名远扬。除了好玩，没人严肃看待它。

直到几年后prototype.js和script.aculo.us出现（谁还记得你们呢？sigh），javascript才开始自我正名。

然后是神一样的jquery。

接下来羽翼丰满的javascript开始玩MVC，代表作是backbone.js。

还玩函数式编程，如underscore.js。

总之到我创业时，javascript的生态圈已经无比繁荣。途客圈的第一个产品的计划编辑器使用了backbone.js，第二个产品前端全面采用ember.js，而且用coffeescript撰写。

我写了个makefile把所有的coffeescript整合编译打包。

我好像没提makefile吧？程序员最好会makefile，减轻很多事务性工作。

然后javascript在V8的基础上开启了nodejs时代，nodejs让javascript登堂入室，成为后端的一股劲旅。

从此前端工程师开始屌丝逆袭，成了香饽饽。会Python的不见得敢写前段代码，但会javascript的已经在后端开疆拓土。

笨重的XML此时已经向JSON让路，前后两端的数据通讯被javascript把持。

mongodb的出现进一步助长了javascript的气焰 —— 连数据库都是JSON（BSON）存储，javascript作为存储过程（这么说好理解些），javascript还有什么不可以？

几乎在一两年间，LAMP改朝换代成了MEAN（MongoDB，Express，Angular，Nodejs/Nginx），nodejs大有当初RoR横扫一切之势。

构建在nodejs上，提倡react的meteor.js向整个互联网刮了一阵清风 —— 原来网站的代码还能这么轻巧地让一切动起来！草草学习了花了几个晚上，我写了teamspark，成为了途客圈团队内部的标准沟通工具。可惜不知怎么的，meteor.js的发展渐渐受到瓶颈，打下的良好用户和市场基础在这两年的缓慢更迭中一点点被消磨。

后来我从互联网回到了通讯领域，趁着一段难得的清闲，好好研究了下concurrency。concurrency自然少不了Joe Amstrong的erlang。erlang相对于我理解的那些语言，有点不食人间烟火的意味。

在erlang身上我贪婪地攫取了很多知识。erlang适应起来很难，尤其你想表达 ``x=x+1``时会感觉那么地痛苦与无助。我颇花了一些时间才搞明白 ``atoi()`` 在erlang中究竟怎么实现。

尽管我尚未用erlang写过什么像样的系统，但它对我思想的冲击是巨大的。

最终，我从erlang延伸到了go。go是门优点与缺点同样突出的语言。本来我正是把它当作一个带并发支持的"modern C"来看的，但深入下去后发现，go和C是两个世界的人。go只能在某些场景下替换C，但无法取代C。soft realtime是个魔咒，把几乎一切有GC支持的语言挡在了C的另一侧。现在看来，也许只有rust能从理论上取代c/c++。

go已经发展到1.2版本，但依旧任重道远。首先，它的编译速度比宣称的慢不少，执行速度更是比C差了不少，很多场景下（尤其GC相关），要比JVM下的语言（如scala）差。

go也有不少bug，连我都能发现一个严重的导致可执行文件好几百兆的问题（没处理好bss段）。

但go精巧的语法，简洁的思想，语言内置的并发支持，让它还是我不断学习的对象。

人的精力毕竟是有限的。很多语言看了看思想，写了写简单的例子（上百行代码）就搁在一边了。在此鸣谢：ruby，elixir，io，emacslisp，scala，nimrod，rust，clojure，lua，我从你们那里吸收了不少有意思的知识，却浅尝辄止，没有深入和你们互动下去。

也许你会问：一门语言究竟多久能掌握？

学精一门语言，也许需要花上三五年的功夫，也许还要更长。

但学精了一门语言后，学第二门一周也就该能入门了（erlang, haskell, lisp除外）。

现在我不再会对某个公司的技术有特殊的偏见。我拥抱一切能提高生产力的技术。

也许你会问：学那么多语言有什么用？

如果用来养活自己，一门学精了就足够。其它的没什么用，也就消遣消遣。我看中语言背后的思想，会比较用不同语言开发的乐趣。另外，当你喜爱的语言添加了新的特性（或者你用到了某个高级特性），你可以一下子就想到了背后的逻辑：啊，原来这是xxx的思想。于是，你对这两门语言的掌握又加深了一层。

我目前最大的遗憾，是没有静下心来好好看看java。

虽说对技术没有偏见，但我依然痛恨恶心的IE6/7；同时，我打心底喜欢一样东西：MAC。

如果说对程序员有什么忠告，那就是：Every programmer should use MAC。