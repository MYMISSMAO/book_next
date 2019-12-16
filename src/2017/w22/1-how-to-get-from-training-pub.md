---
title: '当我参加培训的时候，我在学什么？'
authors: [程序君]
keywords: [成长, 学习]
---

# 当我参加培训的时候，我在学什么？

在旧金山举行的 erlang/elixir 2017 大会上周结束。这次，我并未参加 —— 权衡再三，我选择了这周的 complete OTP 培训，毕竟大会的视频 youtube 上找得见，可以慢慢补，培训错过了就没了。

参加一次技术培训，代价往往不菲，像这样一个四天的培训，价格是两千多刀，你很难说出它有多值 —— 培训的主题有一半都是我已经了解或掌握的内容，在过去的一两个月，我还给我的 team 培训过；另一半，其实给我空出来四天的时间，我自己看书或者读 erlang 的文档，获取到的知识也未必比参加培训少，那么，花这样的大价钱参加的意义是什么？

自己先想想看。

寻找合适的，志同道合的工程师？No。通过参加培训达到这样的目的，既不规模，也不经济，还不如去相关的 meetup 上勾搭呢。

跟讲师套磁，建立关系？hmmm... 你觉得四天能套出什么结果？大家都是实诚的程序员，讲究以德胡人，活好的自然互相倾慕（我跟讲师约了五月份他来湾区有机会喝个咖啡聊聊）；活不好，培训完就是路人。

朝着这些方向想，too simple, sometimes naive。

其实，花钱参加培训的终极意义是（敲黑板）：你购买了一次 __附带培训的咨询服务__。

就拿我参加的 complete OTP 培训来说吧。讲师 Francesco 是 Erlang Solutions 的 founder。Erlang Solutions 是一个咨询公司，很多著名的开源项目（比如：RabbitMQ，Riak，MongooseIM）来源于他们，他们还是 erlang/elixir 大会的发起人。考虑到这样的 profile，你去 Erlang Solution 买个四天的咨询服务试试看？不定给你派个什么水平的咨询师来，而且起价没个几万肯定下不来。两千？做梦去吧。

可惜似乎没人懂这个理。也幸好没人懂这个理，这样一门课程，冷清到全世界的 erlang/elixir 程序员（虽然基数很小）加起来，包括我也就只有九个人参加。而时时刻刻都在提问的，只有我和一个 apple 的工程师（是的，apple 内部有项目在用 elixir 做，yeah，erlang/elixir 程序员可以嗨森一下，然后该干嘛干嘛去了）。而提问的方向聚焦在平时工作中遇到的问题的，和公司业务相关的，基本就是我。

这个 complete OTP 的课程内容不算特别紧凑，其中，做一个 ebank 项目的练习时间，快占了一半。这个宝贵的问各种二逼问题的时间，你造么 —— 绝大多数工程师都在寂静无声地吭哧吭哧写代码，偶尔遇到问题了问问 Francesco 这怎么回事，那里为什么编不过去？

这就好比你守着扁鹊，不让他给你问诊，却让他给你剪指甲。

或者，说个程序员熟知的段子：妹子对序员说你要是能让论坛的人都吵起来，我今晚就归你。序员在论坛里说：PHP 是世界上最好的语言。。。

暴殄天物啊。

exercise 没有价值么？非也。这个培训使用的 exercise 非常经典，从 ``gen_server``，``gen_fsm``，``gen_event``，一路练习到 ``supervisor``，``application``，以及使用 ``sasl`` 深入了解 release 的过程，如果谁能把整个 exercise 独立完成，我觉得他/她就能击败 80% 的 elixir 程序员，真可以在简历上号称一下掌握 OTP 了。

很有价值，但实现这个价值的时机不对。

全班同学仿佛只有我预先（或者之后）把 exercise 做完，而在 exercise 的时候，问课程中各种没有来得及问的问题，以及工作中踩到的各种坑。

你看我都问了哪些很 "silly" 的问题：

* 为什么说 ``start_link`` 是个同步的过程？
* application 为什么会起两个 process，再启动 supervisor？（其实这个问题我在书中看到答案，只是为了引出更多的问题来确保我理解对了）
* group_leader 的意义何在？（我觉得我懂了，但我不知道我是不是真的懂了）
* 使用 global process 是不是个好的做法（这次我干脆无耻地打开我工作中写的 auto compiler 的代码跟他探讨）

等等。在 Francesco 的推荐下，我甚至还读了一些 OTP 的源码，和他探讨源码里的细节。

这才是有效地利用这样的「附带培训的咨询服务」。

如果你觉得我说的对，那么接下来我们看看如何从一次培训中收到最大的收益？

## 选择合适的讲师

如果抱着上述所说的目的，那么，培训的内容其实是次要的。既然把它当做是「咨询」，那么，我们需要选择合适的「咨询师」。

前面说了，这次的讲师是 Francesco Cesarini，我们前面介绍过他是 Erlang Solutions 的 founder（这个身份暂且放在一边不提），他的其他身份（吸引我的身份）是：Designing for Scalability with
Erlang/OTP 一书的作者，erlang/OTP R1 的开发人员。

也就是说，可能除了 erlang 的几个 founder 外，如果在全球范围内海选十个有资格讲 OTP 的人，他必定是其中之一，而且排位靠前。

我知道大部分读者不知道 erlang/OTP，大概也搞不清 Francesco 和 San Francisco 有什么区别。我们换个角度说 ——

如果你做微信服务，你平日烧香供着的姓张的舅舅开个小班培训，谈谈如何做微信下的服务，票价一万；而程序君也同时做几乎相同的培训，吐血白菜价一百，你参加哪个？

搞清楚了这道选择器后，我们再出一道题：Rich Hickey 有个 clojure 的 培训，或者 Guido van Rossum 讲 dive into Python，面向中级水平的程序员，而作为 clojure 或者 python 的高手高手高高手，你参不参加这个培训？

## 做足功课

培训上可能讲到的内容，是不是先自己过一遍，把所有自己没搞明白的问题整理出来，在培训的过程中随时发问呢？

工作中，我们在一个方向上工作久了，业务熟悉了，就会成为所谓的「专家」，如果周围的人在你的领域都远不如你，便会自以为是。是不是可以趁着这样的机会把自己工作中遇到的问题，不懂的，似懂非懂的，以为自己懂的，以为自己对的，都拎出来跟讲师辩一下呢？

## 用这样的机会跨越平台期

程序员估计都知道一万小时理论 —— 足够长时间（一万是个约数）在某个领域的刻意训练（deliberate training）能够让你成为专家。我们据此坚信，24小时学会 C++ 是错误的，肤浅的；相反，只要功夫深，就能学精 C++。

也似乎不太对。

因为我遇到太多干了十几年的平庸程序员了。他们似乎困在一个无论怎么努力也很难跨越的平台期 —— 这是一万小时理论里的禁飞区。

这次培训，同学们的 erlang/elixir 的工作经验都远高于我 —— 我 elixir 三个月，三千行代码经验，erlang 零工作经验。在做 exercise 前，我都搞不清楚写代码的时候什么时候该用分号，什么时候该用逗号。

但四天下来，我觉得我写 erlang 代码的水平（虽然还是比较慢，还会漏句号）已经并不比有好几年 erlang 经验的同学差多少了。

这是为啥？

我想，很多人误解了 deliberate training 的含义了 —— 朝着目标头悬梁锥刺股是对的，但要知道该如何跨越平台期而进阶。我最近每周六晚都带着小丫头溜冰。我知道她跟我溜得再努力，每次一刻都不停歇一个小时滑一百圈也不可能成为下一个关颖姗。我的上限就决定了她的上限；可是，她要是有幸跟着关颖姗滑上一年，接受指点，同样的努力程度，往大了不敢说，一年后制霸 Cupertino 同年龄段应该不成问题。

所以 deliberate training 很重要的组成部分是 feedback loop。对，我又要灌 build - measure - learn 的鸡汤了。你光是机械地 build build build，没有 measure，哪来 learn 呢？measure 很重要。更重要的是，怎么 measure，谁来 measure？用什么 criteria 来 measure？这很有讲究。

跟着一个高手学几天，即便不能功力大涨，但起码知道自己应该突破的脉门何在。我们不是都读过令狐冲和风清扬在思过崖上的故事么？

善用你的老师。老师不光是有血有肉的，由碳基构成的那些位，还有无色无味的，从 0 和 1 演化而成的源代码们。

Linus 说：read the F**KING code!

我们读一本优秀的书，就像是和作者在进行心与心的交流；我们读一段美妙的源代码，如同长辈和晚辈间的薪火相传。这世上，也许只有写作和编码，能够像无崖子渡让内力给虚竹那样，并不太费力就能完成知识和经验的传承。

我问的好些问题，Francesco 建议我去 xxx 目录下读源码。比如 application master，比如 gen_server，我就着源码，在纸上画着流程，嘴里喃喃自语道：bravo!

读到不通处，再和他探讨。

你看，傻小子郭靖，不就在七公手下，这么成长的么？