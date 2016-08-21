语义网的公司（5）Vulcan: Project Halo
---
    
> Categories: 语义产业  
> Time: 2011-04-29  
> Original url: <http://baojie.org/blog/2011/04/29/vulcan/>
    
[Vulcan Inc.](https://en.wikipedia.org/wiki/Vulcan_Inc.)是一家投资公司，由微软的共同创始人[Paul Allen](https://en.wikipedia.org/wiki/Paul_Allen)创建，在西雅图（Seattle, Washington）。

Vulcan投资很多事情，比如宇宙飞船。Allen的钱已经足够多，有些投资看起来纯粹是兴趣或者好奇，并不打算挣更多的钱。他对语义网和知识管理的投资，大概就属于这一类。

![](http://baojie.org/blog/wp-content/uploads/2011/04/halo.jpg)

这个方向，主要是一个[Project Halo](https://en.wikipedia.org/wiki/Vulcan_Inc.#Project_Halo)，主页在<http://www.projecthalo.com/>。长期目标是开发一个数字亚里斯多德（Digital Aristotle）系统，一个可以解决复杂的科学问题或者日常问题的推理系统（a reasoning system capable of answering novel questions and solving advanced problems in a broad range of scientific disciplines and related human affairs.）现在，它的主要应用域是教育，并试图解决知识获取和自动推理中的若干问题。

Halo是一个很宏伟的计划，从2003年开始，已经8年了。项目的总负责人是[Mark Greaves](www.linkedin.com/pub/mark-greaves/1/479/b66)（之前他是DARPA的Program Manager，负责过DAML）。主要分三块，每个项目上人也不多，核心就几个人，很多研究靠外包。

- AURA ( [Automated User-Centered Reasoning and Acquisition System](www.ai.sri.com/project/aura)): 面向用户的自动推理和获取系统。主要是做教科书的形式化，集中在生物、化学、物理三个专业。方法目前主要是逻辑的，用描述逻辑（description logic），逻辑规划（logic programming）等。Vulcan自己这边的主管是David Gunning，他以前在DARPA管PAL（见[对Siri公司的介绍](blog.baojie.org/2011/05/01/siri/)）。工作外包给SRI International 来做。负责人是[Vinay K Chaudhri](http://www.ai.sri.com/people/chaudhri) 。【这个项目很有趣，我以后可能会深入介绍】

- SMW([Semantic MediaWiki](smwforum.ontoprise.com))+。SMW自己是开源的，SMW+对SMW做的了很多扩展，统称为[Halo Extension](https://www.mediawiki.org/wiki/Extension:Halo_Extension)。比如一些标注工具，本体编辑器，可视化，项目管理插件等等。Vulcan自己这边主要是Jesse Wang（中国人）在负责。有些任务外包到[Ontoprise](www.ontoprise.de/en/)（一个德国公司）。这一块以后也会详细讲。

- SILK（[Semantic Inferencing on Large Knowledge](http://silk.semwebcentral.org/) ），主要是研究表达力很强的规则语言（rule language）。SILK是一种default LP，基于良基语义（well-founded semantics），里面集成了强否定，弱否定（NAF）和高阶逻辑（HiLog）。他们还定义了一个RIF的非官方方言，[RIF SILK](http://silk.semwebcentral.org/RIF-SILK.html)。主要的负责人是[Benjamin Grosof](http://www.mit.edu/~bgrosof/)，以前是MIT的研究员和RuleML的一个主要设计者。合作伙伴是BBN Technologies（这个公司我以后也会深入介绍）,主要是和[Mike Dean](http://home.comcast.net/~mdeanbbn/)，一个非常资深的语义网专家和DAML的设计者之一。

所有这些，都不直接挣钱，纯研究。     
    