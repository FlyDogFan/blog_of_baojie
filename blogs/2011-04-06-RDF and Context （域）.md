RDF and Context （域）
---
    
> Categories: 幻灯片, 思路, 语义网, 逻辑  
> Time: 2011-04-06  
> Original url: <http://baojie.org/blog/2011/04/06/rdf-and-context/>
    
昨天决定把[Context翻译成域](http://blog.baojie.org/2011/04/05/context/)。今天接着说说用RDF来表示Context，主要是帮我自己理清思路。

去年做了一点这个方向的工作，参加了[RDF Next Step Workshop](http://www.w3.org/2009/12/rdf-ws/)。这是幻灯片：

[slideshare id=4624693&doc=2010-06-24rdfcontext-100626175833-phpapp01]

现在有很多人研究怎么做RDF的时域（Temporal）和空域（Spatial）扩展，文章很多。一部分我认为重要的Temporal RDF的文章待会列到回复里。Spatial RDF我不很熟悉。比如[一种建议](http://www.w3.org/2009/12/rdf-ws/papers/ws09)是这样的:

```
:stmt2 rdf:subject <s>;  
rdf:predicate <p> ;  
rdf:object <o> ;  
tmp:interval [  
tmp:initial "t1"ˆˆxsd:dateTimeStamp ;  
tmp:final "t2"ˆˆxsd:dateTimeStamp ] .
```

也就是用Reification.

用[Gutierrez等](http://ieeexplore.ieee.org/xpl/freeabs_all.jsp?arnumber=4039284)(2007)提出的抽象语法是

s p o [t1 t2]     

那如果我们要表示空间域，比如“布什是总统”这句话在2002-2009时间域为真，在美国空间域为真。那我们就要再加一维

s p o [t1 t2] \<s>


那如果有更多的其他context呢？比如情绪、上下文、背景数据（比如，“高个子”在NBA和武大饼屋含义不同）。那一个triple上加的注释（annotation）就会越来越多，不胜其烦。

一个办法就是把这些context通通包装起来，放在一个“context document”里面。一个triple，或者一组triple，在某些context里是真的，在其他一些context里为假。在查询的时候，首先指定我们感兴趣的context，则只有相关的triple被返回。

用抽象语法

s p o @c  
c  [t1 t2] \<s>

看起来差别不大。但是这样有几个好处:

- 域可以被重用。如果有很多triple共享空间和时间，那不必重复
- 域可以被推理。一个triple可以属于多个域，或者根据推理的结果属于某个域（域本身可以是变量，在具体语法上是空节点blank-node）
- 域之间可以有关系。比如我们对谁是总统这种论断制定空域的封闭世界假设，那一旦知道且仅知道“布什是总统”这句话在2002-2009时间域为真，那在2010年“布什是总统”并为假。反之，“今天下雨了”这句话在Boston为真，在NYC可能也为真（开放世界假设）。又，“今天下雨了”这句在曼哈顿为真，这在NYC也为真。

为什么不仅是用Named Graph（名图）？名图只是表示了一种语法上的包含关系。你无法说，或者推理出，(s p o)属于名图g这种关系。名图可以用来做语法上的陈述，但是需要新的语义才能表示context（域）。

未完，下次讲域的不确定性（uncertainty）模态（modal property）。     
    