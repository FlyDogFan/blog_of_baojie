笔记：加注(Annotated) RDF (7) Guha 2004
---
    
> Categories: 笔记, 语义网, 逻辑  
> Time: 2011-05-08
    
Ramanathan V. Guha, Rob McCool, Richard Fikes: Contexts for the Semantic Web. International Semantic Web Conference 2004: 32-46Guha是Context建模的先驱。这个文章，无非是McCarthy和Guha的博士论文工作在语义网上的自然应用。我感兴趣的，是第六节Model Theory。在一般的RDF语义中， IS是一个从URI到IR v IP 的映射（我把它称为“释名函数”）。Guha的语义里，IS是一个从URIxURI到IR v IP 的映射，第一个URI是资源（class, property等），第二个URI是context. 最关键的语义条件是这一条：If E is a ground triple (s p o) in the context c then I(E,c) = true if c, s, p and o are in V, IS(p,c) is in IP and < IS(s, c), IS(o, c) > is in IEXT(IS(p,c)). Otherwise I(E,c)= false.注意，IEXT（外延函数）并不是contextual的，上面的条件中，和普通RDF语义唯一的区别是IS（释名函数）。在不同的context中，一个URI可以映射到不同的资源上，所以可以对应到不同的外延上。这里Guha没有具体说context本身之间是不是可以有关系，比如context的层次关系，如果< IS(c1, u), IS(c2, u) > is in IEXT(IS(narrower,u)) then IS(x,c1)(如果存在)= IS(x,c2)。或可定义contex上的一阶关系     
    