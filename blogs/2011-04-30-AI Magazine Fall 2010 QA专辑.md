AI Magazine Fall 2010 QA专辑
---
    
> Categories: 笔记, 语义网  
> Time: 2011-04-30  
> Original url: <http://baojie.org/blog/2011/04/30/ai-magazine-fall-2010-qa/>
    
把网上各处的PDF收集在此，和一些阅读笔记

[AI Magazine](www.informatik.uni-trier.de/~ley/db/journals/aim/index.html), Volume 31,  Number 3, Fall 2010   
<http://www.informatik.uni-trier.de/~ley/db/journals/aim/aim31.html>

David Gunning, [Vinay K. Chaudhri](http://dblp.uni-trier.de/db/indices/a-tree/c/Chaudhri:Vinay_K=.html), [Chris Welty](http://dblp.uni-trier.de/db/indices/a-tree/w/Welty:Chris.html):  Introduction to the Special Issue on Question Answering. 11-12   
<http://www.allbusiness.com/science-technology/computer-science/15271882-1.html>

Douglas B. Lenat, [Michael J. Witbrock](http://dblp.uni-trier.de/db/indices/a-tree/w/Witbrock:Michael_J=.html), [David Baxter](http://dblp.uni-trier.de/db/indices/a-tree/b/Baxter:David.html), [Eugene Blackstone](http://dblp.uni-trier.de/db/indices/a-tree/b/Blackstone:Eugene.html), [Chris Deaton](http://dblp.uni-trier.de/db/indices/a-tree/d/Deaton:Chris.html), [Dave Schneider](http://dblp.uni-trier.de/db/indices/a-tree/s/Schneider:Dave.html), [Jerry Scott](http://dblp.uni-trier.de/db/indices/a-tree/s/Scott:Jerry.html), [Blake Shepard](http://dblp.uni-trier.de/db/indices/a-tree/s/Shepard:Blake.html):  Harnessing Cyc to Answer Clinical Researchers’ Ad Hoc Queries. 13-32    
<http://www.cyc.com/technology/whitepapers_dir/Harnessing_Cyc_to_Answer_Clincal_Researchers_ad_hoc_Queries.pdf>

CYC是传统逻辑主义方法的代表。这个方法可以达到很高的准确度，但是recall很低，成本很高，基本只能在少数行业用户中使用，如国防、银行和医疗。

David Gunning, Vinay K. Chaudhri, Peter Clark, Ken Barker, Shaw Yi Chaw, Mark Greaves, Benjamin N. Grosof, Alice Leung, David D. McDonald, Sunil Mishra, John Pacheco, Bruce W. Porter, Aaron Spaulding, Dan Tecuci, Jing Tien:  Project Halo Update – Progress Toward Digital Aristotle. 33-58  
<http://www.cs.utexas.edu/users/pclark/papers/AURA-AIMag.pdf>   
【项目主页】<http://www.ai.sri.com/project/aura>   
【参考】

- 2011-04-29 [语义网的公司（5）Vulcan: Project Halo](http://baojie.org/blog/2011/04/29/vulcan/)
- 2011-04-30 [笔记: Inquire for iPad （平板上的教科书)](http://baojie.org/blog/2011/04/30/aura-inquire-for-ipad/)
- 2011-05-01 [笔记：AURA](http://blog.baojie.org/2011/05/01/aura/)


Halo计划分为三大部分：问答系统Aura，知识库构造Semantic MediaWiki，知识推理SILK。Aura本身也是强调形式化知识和利用推理，但是问题还是成本太高，无法扩展。这个项目现在已经终止了。

David A. Ferrucci, Eric W. Brown, Jennifer Chu-Carroll, James Fan, David Gondek, Aditya Kalyanpur, Adam Lally, J. William Murdock, Eric Nyberg, John M. Prager, Nico Schlaefer, Christopher A. Welty:  Building Watson: An Overview of the DeepQA Project. 59-79   
<http://www.stanford.edu/class/cs124/AIMagzine-DeepQA.pdf>

【参考】

- 2011-03-23 [张雷谈沃森，及我的感想](http://baojie.org/blog/2011/03/23/waston/)
- 2011-04-30 [IBM沃森系统摘要的摘要的摘要](http://baojie.org/blog/2011/04/30/watson/)
- 2011-04-30 [笔记：DeepQA (IBM沃森)（1）概览](http://blog.baojie.org/2011/04/30/deep-qa/) （和这里面的引用）
- 2011-05-01 [DeepQA (IBM沃森)（2）问题之分析](http://baojie.org/blog/2011/05/01/deep-qa-2/)
- 2011-05-01 [DeepQA (IBM沃森)（3）答案之生成](http://baojie.org/blog/2011/05/01/deep-qa-3/)
- 2011-05-01 [DeepQA (IBM沃森)（4）结果与心得](http://baojie.org/blog/2011/05/01/deep-qa-4/)     

William Tunstall-Pedoe:

True Knowledge: Open-Domain Question Answering Using Structured Knowledge and Inference. 80-92   
【公司网址】<http://www.trueknowledge.com/>   
【一个2008年的PPT】  <http://www.ai.sri.com/~nysmith/slides/aic-seminars/081023-tunstall-pedoe.pdf>

【参考】

- 2012-02-06 [语义网的公司 True Knowledge](http://baojie.org/blog/2012/02/06/true-knowledge/)


P.S. 2014-09-03 True Knowledge推出了个Siri类似的产品叫Evi。TK的强点在知识库构造，自然语言界面只是一层皮肤。它的问答在百科知识上表现不错，当时能回答一些Siri回答不了的问题（如需要path query和一些推理的）。2012年我就觉得谁要是把他买下来就赚大了。最后居然是Amazon出手，只花了区区2400万美元。TK的商业化一直没做好，把自己贱卖了。

Stephen Soderland, Brendan Roof, Bo Qin, Shi Xu, Mausam, Oren Etzioni:  Adapting Open Information Extraction to Domain-Specific Relations. 93-102   
<http://www.cs.washington.edu/homes/mausam/papers/aimag10.pdf> 

PS 2014-09-03 Oren Etzioni现在跑去Vulcan领导Allen Institute for Artificial Intelligence. 其实在这之前Halo项目已经开始吸取以前的教训，向知识提取和自然语言处理转型了。但Paul Allen显然觉得Etzioni更有潜力来领导这个项目，就换血让他来做了。

PS. 一些其他相关的博文：

- 2013-01-17 [Facebook Graph Search笔记](http://baojie.org/blog/2013/01/17/facebook-graph-search/)
- 2011-05-01 [语义网的公司（6）Siri](http://baojie.org/blog/2011/05/01/siri/)
- 2011-11-16 [SIRI的贡献和价值](http://baojie.org/blog/2011/11/16/siri-2/)
- 2011-11-27 [Watson和SIRI](http://baojie.org/blog/2011/11/27/watson-and-siri/)
- 2011-12-17 [Siri Patents](http://baojie.org/blog/2011/12/17/siri-patents/)
- 2011-12-18 [SIRI背后的关键人物Adam Cheyer](http://baojie.org/blog/2011/12/18/adam-cheyer/)
    