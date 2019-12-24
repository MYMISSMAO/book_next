---
title: 浅谈unix之美
author: [程序君]
keywords: [技术, unix]
---

# 如何从零开始学一门程序语言？

## 如何选择语言？

我的第一门实用型的语言是Visual Basic。看了一段时间的windows编程，在各种句柄，消息循环以及繁复的MFC中迷失后，VB让我见识到了简单，直接了当，以及文档（MSDN）的重要性。学习的门槛是个大问题，有些语言（及其背后的框架）没有一定的基础最好不要碰。

当然，语言总是在发展，现在在dotnet框架下的VB已经失去了那种简单直接的美。

第一门语言最好选择带如下属性的语言：

* 1. 语法简单，结构明晰，写出来的代码相对简洁明了
* 2. 有完善的生态系统，尤其是文档
* 3. 语言最好提供REPL(Read-Evaluate-Print-Loop)和introspection
* 4. 开源社区（如github）有足够多的样本代码
* ...

以python为例，稍微解释一下第三条。python的shell（python或ipython）提供了一个语法和库函数的试验场，对初学这门语言来说帮助很大。想弄通python的数据结构，在shell下练习半小时基本就懂了。另外，在shell里随时可以对任何函数，类库做introspection（内省）—— 通过 ``help``，``dir``，``type``，``inspect（库）``等深入到被调者内部了解其行为，这就进一步降低了初学者的门槛。写C代码的时候，遇到不太明白怎么使用的函数时，要么看其源码，要么找文档，但在python里，方便的内省工具可以随时随地帮助你。

补充一句，这两个语言没有可比性，我仅仅拿来举个例子。也许有人会说我可以用gdb做内省啊，但那已经不是一个层面的解决之道，也不是初学者入门时能掌握的。

第一条不用太解释，没人一开始就喜欢复杂吧？第二条和第四条当你学习时，有什么参考资料，及当你遇到问题时，可以寻求到什么帮助。你可以从某语言的官网上了解其社区文档的完备性，从stackoverflow和github上了解其生态系统和社区力量的强弱。

如果非要让我很主观地推荐，第一门语言我推荐python，它满足上面的所有要求（ruby，scala等也都可以考虑）。

看到这，也许你会问，有REPL岂不是不把大多数static typing的语言给排除在外了？对！

因为标题是从零开始学，学的过程中的互动（和shell），学习者不断构建信心很重要。compiler介入只会给这个阶段的学习带来不必要的负担。

## 如何学习？

学一门语言，要从语言的__历史__和__思想__入手。

从语言的历史中，我们可以了解到语言诞生时的各种因素，以及在之后发展过程中的种种选择。除此之外，你要了解大概该语言的社区中在时间轴上都出过什么样的产品。这些都会加深你对语言的理解和认同感。

学习语言的思想（哲学）很重要，这体现在语言的设计，语法，甚至整个社区的行为。将一个数字转化成字符串，在python里你大概会这么做：

```
In [1]: str(10)
Out[1]: '10'
```

但在ruby里你应该这么做：

```
irb(main):001:0> 10.to_s
=> "10"
```

如果你将其视为语法而死记硬背，那事倍功半。ruby的哲学是，纯粹的OO，告诉object做什么事，而非对object做什么事。

对比ruby和python两种语言很有意思。ruby作者从smalltalk和perl的影响很大，所以ruby里一切都是对象（smalltalk），做一件事可以有多种方法（perl）。ruby的作者赋予了ruby灵活的控制权，让你可以改变系统的行为（比如可以open一个类库中的class修订），又有点像lisp。

python从Abc这门教学语言（Algol）中繁衍出来，对纯粹的OO并不感冒，因此代码可以混用面向过程和面向对象。也许是教学语言的基因，python强调做一件事用一种最清晰的方式完成（"There should be one - and preferably only one - obvious way to do it."），所以社区里有人说某个实现是"pythonic"，说明这个实现清晰，简洁，符合python之道。当然python还吸收了很多其它语言的优点，如list comprehension（haskell），applying function to list（lisp）等等。

了解了历史和思想，你会对语言的行为有一个比较合理的解释，学习起来也比较容易举一反三。当然作为第一门语言，你肯定不知道那么多其它语言的名字，很多我也不知道，但可以wiki一下，当拓展/延伸阅读了。

之后就是看文档书籍，看各种网上的视频教程来学习语言的语法和各种库。这个阶段比较枯燥（REPL能稍稍降低这种枯燥）。不要看教科书学语言，教科书上的习题大多和生活中的问题无关，不要试图去写什么鸽笼问题，八皇后的代码。你在学程序语言，不是在做思维训练或是数学。

注意选择书籍的时候尽量选择该语言作者（或者名家）的书，比如ruby该看『松本行弘的程序世界』，python的 "Programming Python"（python作者做的序），erlang看 "Programming erlang - software for a concurreny world"，等等，他们会将很多知识和思想汇入书中。

另外还有一本无关语言，但关于编程要义的书非常值得一看：[『冒号课堂』](http://book.douban.com/subject/4031906/)。国内的作者多写点这样的书，少做点语法介绍、类库介绍的大砖头，将是中文图书的幸事。

过了语法关之后，有两个学习方法：

* 以练代学
* 和社区互动
* 以教代学

以练代学是找个有意思的项目，甩开膀子边写代码边学。驾校里永远无法让你真正学会开车，但你上路后的一周内，你就基本掌握了驾驶的全部技巧；每天都在各种复杂路况上开一个月，你就是老手了。学语言也是这个理。

学习的过程中总有困惑，多在google groups和stackoverflow里面寻找答案。如果实在找不到，用符合社区标准的方式发问。这也是一个累积经验的过程。

以练代学的基础上，最好教一个不会但又想学的人这门语言，或者找一些志同道合的人一起学。有时候我们的思维会受定势的影响，过滤好多头脑中的『傻』问题。别人一个看上去很简单的问题也许会重新触动你的神经，让你好好思索那些被自己视为『简单』的问题的答案。

不过，教别人某门语言的机会不常见，但在社区里看看别人有什么问题，尝试回答，也实践了以教代学。

## 如何进阶？

当你基本能比较随手用某个语言写出简单的应用后，你该考虑回过头来补补那些之前忽略的环节，重新审视这门语言：

* 它的类型系统有什么特点？
* 内存管理模型是什么样的？
* 语言和库分别有什么并发的手段？
* 对范型的支持？
* 异常处理的机制和社区约定俗成的方式是什么？
* 对OOP都有哪些支持？
* 对FP都有哪些支持？
* 如何进行元编程？
* 与其他语言的互操作（比如C）是怎么样的？
* 语言有什么天然的限制？
* ...

在这个审视的过程中，不断把基础知识补齐 —— 这些都是快速掌握下一门语言的基础。

你也许还应该找些比较有意思的源代码，看看别的程序员都是怎么写代码的。读优秀的代码就像读一本好书，仔细咂吧，其乐无穷。

代码写累了，看看名家的书，修炼一下思想。『黑客与画家』，『松本行弘的程序世界』，『程序员修炼之道』等一众书都可看看。

比如说程序员修炼之道里写到：

**You shouldn't be wedded to any particular technology, but have a broad enough background and experience base to allow you to choose good solutions in particular situations.**

我觉得这就是做软件应该有的态度 —— 没有最完美的语言，只有最合适的工具。

## 结语

说了这么多，似乎跟没说一样。学习语言本就是一个因人而异的东西，没有放之四海皆准的教条。还是那句话：修行靠个人！