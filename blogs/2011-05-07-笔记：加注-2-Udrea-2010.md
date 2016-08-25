笔记：加注(Annotated) RDF (2) Udrea 2010
---
    
> Categories: 笔记, 语义网, 逻辑  
> Time: 2011-05-07  
> Original url: <http://baojie.org/blog/2011/05/07/udrea-2010/>
    
Octavian Udrea, Diego Reforgiato Recupero, V. S. Subrahmanian: [Annotated RDF](http://tocl.acm.org/accepted/364subrahmanian.pdf). ACM Trans. Comput. Log. 11(2): (2010) 【本文的会议版在ESWC2006】

这个文章里，annotation也是一种偏序结构。也提到有不确定性uncertainty（模糊fuzzy？）, 时态temporal and 源谱provenance等几种应用。

aRDF = annotated RDF

历史：Annotated logic [Kifer ans Subramanian 1992] （要求标注是一个半格semilattice）[Leach and Lu 1996] [Fitting 1991]

语法：每个property属于某个偏序关系。一个aRDF triple是(s, p:a, o)。例如(Jie memberOf:[2001,2008], IowaStateUniversity)。画成图，就是每条边上多出来个annotation：例如（文中Fig 1(a)）

![](http://baojie.org/blog/wp-content/uploads/2011/05/ardf.gif)

语义：一个aRDF解释（interpretation）是一个从资源到标注的映射。I满足(s p:a o) 如果 a≤ I(s p o).

一个aRDF系统(theory)是可能inconsistent的([Straccia 2010](http://blog.baojie.org/2011/05/07/annotated-rdf/)就不会）– 大概是偏序关系弱于格关系的缘故。不过我不认为这在工程上有什么影响。

后面和查询及实验相关的细节略过。（他们的实验说能处理10million triples）

【评价】本文和[Straccia 2010](http://blog.baojie.org/2011/05/07/annotated-rdf/)方法完全类似。区别在于S文标注在triple上，U文标注在property上。S文要求标注为格，U问要求为偏序。两者的语义，都是从triple映射到标注，再做标注的“大小”比较。这一点应做扩展，从大小比较变成entailment的关系。这就变成了有完整表法力的[域态逻辑](http://blog.baojie.org/2011/04/11/context-model/)（contextual logic）。     
    