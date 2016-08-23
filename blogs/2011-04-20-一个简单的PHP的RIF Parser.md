一个简单的PHP的RIF Parser
---
    
> Categories: 编程, 语义网  
> Time: 2011-04-20  
> Original url: <http://baojie.org/blog/2011/04/20/php-rif/>
    
目前支持了RIF-Core

代码很简单，目前乱七八糟的。可以读XML格式的输入，做presentation syntax的输出。正在做LP（logic program）格式的输出（这样就可以用LP的推理机来做推理），还没搞完。

使用的例子：

```
require_once("../rif2pres.php");
require_once("../rif2lp.php");

// parse XML syntax
$rifdoc = new RifDocument();
$rifdoc->load("ex8.rif");

// write in presentation syntax
$writer = new Rif2Presentation();
$writer->writeAnnotation = true;
$syntax = $writer->toPresentationSyntax($rifdoc);
echo $syntax;

//write in LP syntax
$writer = new Rif2LP();
$writer->toLP($rifdoc);
//print_r($writer->getLP());
echo $writer->getLP()->toString();

```


如果有兴趣参与，请和我联系（baojie@gmail.com）

SVN在这里 <http://php-rif.svn.sourceforge.net/>
    