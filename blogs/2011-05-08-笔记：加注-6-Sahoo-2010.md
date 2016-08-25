笔记：加注(Annotated) RDF (6) Sahoo 2010
---
    
> Categories: 笔记, 语义网, 逻辑  
> Time: 2011-05-08  
> Original url: <http://baojie.org/blog/2011/05/08/sahoo-2010/>
    
S.S. Sahoo, O. Bodenreider, P. Hitzler, A. Sheth, K., Thirunarayan, [“Provenance Context Entity (PaCE): Scalable provenance tracking for scientific RDF data.”](http://knoesis.wright.edu/library/download/ProvenanceTracking_PaCE.pdf),in the 22nd International Conference on Scientific and Statistical Database Management (SSDBM) 2010

讲RDF的Context（或者annotation）建模的文章虽多（几十篇总是有的），涉及语义的很少。这一篇，定了“源谱域实体”Provenance Context Entity (PaCE) [注：[provenance=源谱](http://knoesis.wright.edu/library/download/ProvenanceTracking_PaCE.pdf), [context=域](http://baojie.org/blog/2011/04/05/context/)]。

语法：Provenance当然是很重要的一种context。本文中，provenance用[provenir](http://wiki.knoesis.org/index.php/Provenir_Ontology)来建模，本身就是一个RDF/OWL文档。[Provenir是Sahoo自己提出来的。关于不同的源谱模型的比较，参Li Ding和我的[这篇文章](www.cs.rpi.edu/~baojie/pub/2010-05-16_IPAW2010.pdf) (IPAW2010)]

语义：是对[RDF语义](http://baojie.org/blog/2011/04/21/rdf-semantics/)的一个扩展。大意是如果两个triple有某种共同的源谱，那它们其他的源谱可能也是也是共同的。具体来说，if pc (s1, p1, o1) = pc (s2, p2, o2), then (s1 p v) = (s2 p v) 其中pc是triple的源谱域，p是一个源谱property（比如createdBy）,v是一个值（比如“张三”）。

【评价】我认为这语义只适用于一些特定的场合，或者可用于启发式推理。但是，很难扩展到一般的情况，而且不适合做基于模型论的逻辑推理。当然，工程上可能需要这种简单的框架。     
    