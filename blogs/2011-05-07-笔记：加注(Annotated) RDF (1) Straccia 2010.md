笔记：加注(Annotated) RDF (1) Straccia 2010
---
    
> Categories: 笔记, 语义网, 逻辑  
> Time: 2011-05-07  
> Original url: <http://baojie.org/blog/2011/05/07/annotated-rdf/>
    
Umberto Straccia, Nuno Lopes, Gergely Lukacsy and Axel Polleres. A General Framework for Representing and Reasoning with Annotated Semantic Web Data. In Proceedings of the Twenty-Fourth AAAI Conference on Artificial Intelligence (AAAI-10). 

[Abstract](gaia.isti.cnr.it/~straccia/papers/AAAI10/abstract.html) . [Bibitem](gaia.isti.cnr.it/~straccia/papers/AAAI10/bibitem.html) . [Paper](gaia.isti.cnr.it/~straccia/download/papers/AAAI10/AAAI10.pdf) . [Slides](gaia.isti.cnr.it/~straccia/download/papers/AAAI10/SLIDESAAAI10.pdf)

读这系列的文章，是为了扩展做Contextual RDF。

RDF的Annotation: (s, p, o) : t  – t可以是时间（time），置信度（trust），源谱（provenance）

形形色色的Annotated RDF, contextual RDF, temporal RDF，无非是要描述

- context域上的关系，有人称为meta-knowledge。比如时间。比如域的分类(hierarchy)
- context上的知识转移。传统的（McCarthy式）说法是shifting。也就是，真值如何在context间转移。如 (a sc b): [1,3] and (b sc c): [2,4]推理出 (a sc c) : [2,3] – sc = rdfs:subClassOf

[Straccia 2010]中，annotation可以组成一个Lattice（格）——如果忘了格是什么，通俗的说，一个格里部分元素间可以比大小（偏序关系），而且任意多个元素都有一个共同的上界和一个共同的下界。

语义：标准的[RDF语义](blog.baojie.org/2011/04/21/rdf-semantics/)，略，这里只提和annotation有关的变化。标注（annotation）有一个annotation domain。一个annotated interpretation对每个class，指定一个annotation。也就是一个函数ΔR ->L，其中ΔR是所有资源（resource）的集合，L是所有标注的集合。对property，类似，ΔR x ΔR ->L。

令I是从ΔR 到ΔR 到的“释名”函数（就是把RDF里的名字资源映射到其他资源）。IA(.)是从资源到标注的函数，那(s,p,o):v 的语义是 IA\[I(p)] (I(s),I(o)) ≥ v，这里≥代表偏序关系。注意，IA[I(p)]本身是一个函数。通俗来说，就是p在一个情况下包含(s,o)，而这个情况比v一般（general, wider, broader）。     

在格上，最大下界inf的作用类似于全称量词（universal quantifier）；最小上界sup的作用类似于存在量词（existential quantifier）。具体语义条件看文中Table 2。【注：这也类似[连续信号的逻辑](http://baojie.org/blog/2011/04/11/%e8%bf%9e%e7%bb%ad%e4%bf%a1%e5%8f%b7%e7%9a%84%e9%80%bb%e8%be%91%ef%bc%882%ef%bc%89/)中，用min和max做量词。在普通逻辑中，我们隐含假设T>F,所以 T^F=F, 也即 inf(T,F)=F, min(T,F)=F】【又注：在多值逻辑里，比如4-valued paraconsistent logic, 或者LP的良基语义well-founded semantics，都有这种类似的真值结构和变量词为比大小的办法】

**关键**：和经典逻辑比，在经典逻辑里，只有两个标注值，0或者1。所有的资源，要么属于一个class，要么不属于（L={0,1}）。在Annotated RDF里，有多种“属于”的形式。

**疑问**：它这种定义，一个资源只能有一个标注类型。更一般的，应该是映射mapping而不是函数function。另外，用格代数限制很大。不过，因为其简单，推理才可能用Table 3 里的区区几条规则来表示。

**应用1**：模糊（Fuzzy）RDF。L=[0,1]（0到1的实数）≤是实数上的大小关系，x是实数上的乘法。我们有(a sp b):0.8, (b sp c):0.7 -> (a sp c):0.56 【注：注意和概率RDF的区别——不具有模型论语义。】

**应用2**：时态（Temporal）RDF。L={所有的时段集}。一个时段集（set of temporal interval）是若干个时段，每个时段如[t1, t2]，其中t1,t2是整数（含无穷大和无穷小）。≤是时间轴上的子集关系。

**多种标注的综合**：(CountryXXX  type Dangerous) : <[1975, 1983], 0.8, 0.6> Time x Fuzzy x Trust

**最终评价**：本文其实很简单，思路很清晰。Annotation（标注）定义为一种代数结构（格）。这使annotation域的表达力弱，同时也推理简单。代数结构不需要一种模型论语义，反而适合工程的应用。

**后续阅读**：Nuno Lopes, Axel Polleres, Umberto Straccia, and Antoine Zimmermann. [AnQL: SPARQLing up annotated RDFS](http://iswc2010.semanticweb.org/pdf/51.pdf). In Proceedings of the 9th International Semantic Web Conference (ISWC 2010), Shanghai, China, November 2010. Springer 【对本文加注RDF的一个查询语言】     
    