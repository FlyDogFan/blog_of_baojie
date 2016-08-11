URL, URN, URI, IRI
---
    
> Categories: Web, 笔记, 语义网  
> Time: 2012-01-14
    
“网址”到底是什么？一般的理解是URL（Uniform resource locator）在RDF/OWL1/OWL2中却使用了不同的概念RDF和OWL 1使用了URI （Uniform resource identifier，也就是最初的语义网层次蛋糕的第一层）OWL 2使用了IRI（Internationalized Resource Identifier）还有一个相关概念 URN（Uniform Resource Name）。他们有什么区别？简述如下：URL是这样的形式：scheme://domain:port/path?query_string#fragment_id如本页的编辑页面是  https://blog.baojie.org:80/wp-admin/post-new.php?post_type=post#URI是URL的扩展，形式是：     <scheme name> : <hierarchical part> [ ? <query> ] [ # <fragment> ]例： foo://username:password@example.com:8042/over/there/index.dtb?type=animal&name=narwhal#nose Wikipedia上列有官方和非官方的URI scheme，如about, ed2k, doi, skype，都是。URI不一定指向一个网址URN是一种URI，形式如 urn:isbn:0451450523（书号），urn:mpeg:mpeg7:schema:2001（MPEG-7标准）。URN使我们可以描述一个资源而不必关系它的具体存档地址。IRI是URI的扩展：URI只能用ASCII，而IRI可以用Universal Character Set (USC), Unicode——比如中文。所以RDF和OWL里的资源，都不只是用“网址”来命名的。理论上，每个人都可以自己定义一个scheme来唯一确定自己的资源，不一定要放在网上，比如对我的冰箱，我可以命名为urn:baojie-bengbu-iowa:冰箱:2012更多关于URL/URI/IRI的请看W3C官方网页：Naming and Addressing: URIs, URLs, …另参Tim Berners-Lee的Design Issues，Document Naming （1991）     
    