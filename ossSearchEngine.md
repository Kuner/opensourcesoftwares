**目录**

[TOC]

> **本文档主要是对网络信息的整理汇总，最后给出了参考文献的链接，如有任何问题，请联系本人调整修改**

# 一、工作原理

搜索引擎的工作原理大致可以分为：

1. 搜集信息
   
   ``` 
   搜索引擎的信息搜集基本都是自动的。搜索引擎利用称为网络蜘蛛的自动搜索机器人程序来连上每一个网页上的超链接。机器人程序根据网页链到其中的超链接，就像日常生活中所说的“一传十，十传百……”一样，从少数几个网页开始，连到数据库上所有到其他网页的链接。理论上，若网页上有适当的超链接，机器人便可以遍历绝大部分网页。
   ```
   
2. 整理信息
   
   ``` 
   搜索引擎整理信息的过程称为“创建索引”。搜索引擎不仅要保存搜集起来的信息，还要将它们按照一定的规则进行编排。这样，搜索引擎根本不用重新翻查它所有保存的信息而迅速找到所要的资料。想象一下，如果信息是不按任何规则地随意堆放在搜索引擎的数据库中，那么它每次找资料都得把整个资料库完全翻查一遍，如此一来再快的计算机系统也没有用。
   ```
   
3. 接受查询
   
   ``` 
   用户向搜索引擎发出查询，搜索引擎接受查询并向用户返回资料。搜索引擎每时每刻都要接到来自大量用户的几乎是同时发出的查询，它按照每个用户的要求检查自己的索引，在极短时间内找到用户需要的资料，并返回给用户。目前，搜索引擎返回主要是以网页链接的形式提供的，这样通过这些链接，用户便能到达含有自己所需资料的网页。通常搜索引擎会在这些链接下提供一小段来自这些网页的摘要信息以帮助用户判断此网页是否含有自己需要的内容。
   ```

整理信息及接受查询的过程，大量应用了文本信息检索技术，并根据网络超文本的特点，引入了更多的信息。



# 二、分类

搜索引擎按其工作方式主要可分为三种，分别是全文搜索引擎（Full Text Search Engine）、垂直搜索引擎（Vertical Search Engine）和元搜索引擎（Meta Search Engine）。

1. 全文搜索引擎
   
   ``` 
   全文搜索引擎是名副其实的搜索引擎，欧美具代表性的有Google、Fast/AllTheWeb、 AltaVista、Inktomi、Teoma、WiseNut等，中国著名的有百度（Baidu）。它们都是通过从互联网上提取各个网站的信息（以网页文字为主）而创建的数据库。检索与用户查询条件匹配的相关记录，然后按一定的排列顺序将结果返回给用户，因此他们是真正的搜索引擎。
   ```
   
2. 垂直搜索引擎
   
   ``` 
   垂直搜索引擎是针对某一个行业的专业搜索引擎，是搜索引擎的细分和延伸，是对网页库中的某类专门的信息进行一次集成，定向分字段抽取出需要的数据进行处理后再以某种形式返回给用户。垂直搜索是相对通用搜索引擎的信息量大、查询不准确、深度不够等提出来的新的搜索引擎服务模式，通过针对某一特定领域、某一特定人群或某一特定需求提供的有一定价值的信息和相关服务。例如，著名的百度图片搜索，互联统计网等都是针对某一领域而采用的垂直搜索引擎。
   ```
   
3. 元搜索引擎
   
   ``` 
   元搜索引擎在接受用户查询请求时，同时在其他多个引擎上进行搜索，并将结果返回给用户。著名的元搜索引擎有InfoSpace、Dogpile、Vivisimo等（元搜索引擎列表），中文元搜索引擎中具代表性的有搜星搜索引擎。在搜索结果排列方面，有的直接按来源引擎排列搜索结果，如Dogpile，有的则按自定的规则将结果重新排列组合，如Vivisimo。
   ```



# 三、开源搜索引擎

开源搜索引擎项目一览



| 项目名称                                     | 简介                                       |
| :--------------------------------------- | :--------------------------------------- |
| [Lucene](http://lucene.apache.org/java/docs/index.html) | Apache Lucene 是一个纯Java 编写的高性能、全功能的文本搜索引擎。它使用几乎所有需要全文检索的应用，尤其是跨平台应用。 |
| [Solr](http://lucene.apache.org/solr/)   | Solr是一个高性能，采用Java开发，基于Lucene的全文搜索服务器。文档通过Http利用XML加到一个搜索集合中。查询该集合也是通过http收到一个XML/JSON响应来实现。它的主要特性包括：高效、灵活的缓存功能，垂直搜索功能，高亮显示搜索结果，通过索引复制来提高可用性，提供一套强大Data Schema来定义字段，类型和设置文本分析，提供基于Web的管理界面等。 |
| [Compass](http://www.compass-project.org/) | Compass是一个强大的,事务的,高性能的对象/搜索引擎映射(OSEM:object/search engine mapping)与一个Java持久层框架。Compass包括: 1）搜索引擎抽象层(使用Lucene搜索引荐), 2） OSEM（Object/Search Engine Mapping）支持, 3） 事务管理, 4） 类似于Google的简单关键字查询语言, 5） 可扩展与模块化的框架, 6） 简单的API。 |
| [Sphinix](http://www.sphinxsearch.com/)  | Sphinx是一个基于SQL的全文检索引擎，可以结合MySQL,PostgreSQL做全文搜索，它可以提供比数据库本身更专业的搜索功能，使得应用程序更容易实现专业化的全文检索。Sphinx特别为一些脚本语言设计搜索API接口，如PHP,Python,Perl,Ruby等，同时为MySQL也设计了一个存储引擎插件。 |
| [Nutch](http://nutch.apache.org/)        | Nutch is open source web-search software. It builds on Lucene Java, adding web-specifics, such as a crawler, a link-graph database, parsers for HTML and other document formats, etc. |
| [Katta](http://katta.sourceforge.net/)   | Katta是一个可扩展的、故障容错的、分布式实施访问的数据存储。Katta可用于大量、重复、索引的碎片，以满足高负荷和巨大的数据集。这些索引可以是不同的类型。当前该实现在Lucene和Hadoop mapfiles。 |
| [IndexTank](https://github.com/linkedin/indextank-engine ) | IndexTank是一套基于Java的索引-实时全文搜索引擎实现，它的设计分离了相关性标记和文档内容，因为相关性标记的生命周期和文档本身是不一样的，特别是在用户创建的内容的情况下，例如分享次数，Like按钮，+1按钮等等。 |
| [ElasticSearch](http://www.elasticsearch.com) | ElasticSearch是一个基于Lucene构建的开源，分布式，RESTful搜索引擎。设计用于云计算中，能够达到实时搜索，稳定，可靠，快速，安装使用方便。支持通过HTTP使用JSON进行数据索引。 |
| [Summa](http://wiki.statsbiblioteket.dk/summa/) | Summa是一种由java开发的，快速模块化和可扩展的搜索引擎。Summa有如下特点: 1) 综合搜索Summa能够同时访问许多不同的数据和资料来源,并以一个统一的接口公开, 2) 模块化设计Summa搜索系统由一系列独立模块组成，这样使得它更简单容易地被维护和升级, 3) 可扩展性Summa支持分布式架构而且能够按比例的扩大或缩小以处理任何数量的数据, 4) 开放标准Summa基于现代web技术与标准，不包含任何私有代码或原理, 5) 故障容错如果某单一数据资源或服务出错，Summa将会继续运行而不受出错部分限制。 |
| [Arachnode.net](http://arachnode.net/)   | An open source .NET web crawler written in C# using SQL 2005/2008. Arachnode.net is a complete and comprehensive .NET web crawler for downloading, indexing and storing Internet content including e-mail addresses, files, hyperlinks, images, and Web pages. |
| [Open Search Server](http://www.open-search-server.com/) | Open Search Server is both a modern crawler and search engine and a suite of high-powered full text search algorithms. Built using the best open source technologies like lucene, zkoss, tomcat, poi, tagsoup. Open Search Server is a stable, high-performance piece of software. |
| [Grub](http://grub.org/)                 | Grub Next Generation is distributed web crawling system (clients/servers) which helps to build and maintain index of the Web. It is client-server architecture where client crawls the web and updates the server. The peer-to-peer grubclient software crawls during computer idle time. |
| [Jumper - Collaborative search engine in PHP](http://www.jumpernetworks.com/) | Jumper 2.0 is a collaborative community search platform that revolutionizes search by crowdsourcing knowledge management powered by a shared bookmarking engine. It is easily and quickly deployed into a community of practice that benefits users with complex and specialized search requirements. Jumper delivers universal search of any databases, flat files, fileshares, content systems, web pages, blogs and wikis, even people - through one simple search box. |
| [CLucene - Lucene C Port](http://clucene.sourceforge.net/) | CLucene is a port of the very popular Java Lucene text search engine API. CLucene aims to be a good alternative to Java Lucene when performance really matters or if you want to stick to good old C++. CLucene is faster than Lucene as it is written in C++, meaning it is being compiled into machine code, has no background GC operations, and requires no any extra setup procedures. |
| [Constellio - Enterprise Search engine](http://constellio.com/) | Constellio Open Source Enterprise Search is based on Apache Solr and using Google Search Appliances connectors architecture, it allows, with a single click, to find all relevant content in your organization (Web, email, ECM, CRM etc.). |
| [Xapian - Search Engine Library](http://www.xapian.org/) | Xapian is an Open Source Search Engine Library. It is written in C++, with bindings to allow use from Perl, Python, PHP, Java, Tcl, C# and Ruby. Xapian is a highly adaptable toolkit which allows developers to easily add advanced indexing and search facilities to their own applications. It supports the Probabilistic Information Retrieval model and also supports a rich set of boolean query operators. |
| [Whoosh - Python Search Library](https://bitbucket.org/mchaput/whoosh/) | Whoosh is a fast, featureful full-text indexing and searching library implemented in pure Python. Programmers can use it to easily add search functionality to their applications and websites. It has support of Fielded indexing, search, scoring, text analysis, storage, Pluggable scoring algorithm, Powerful query language and spell-checker. |
| [Zebra - Indexing and Retrieval Engine](http://www.indexdata.com/zebra) | Zebra is a high-performance, general-purpose structured text indexing and retrieval engine. It can index records in XML/SGML, MARC, e-mail archives and many other formats and allows access to them through exact boolean search expressions and relevance-ranked free-text queries. |
| [Lucene.Net - Lucene port in CSharp](http://incubator.apache.org/lucene.net/) | Lucene.Net is a port of the Lucene search engine library, written in C# and targeted at .NET runtime users. The Lucene search library is based on an inverted index. |
| [MG4J - Managing Gigabytes for Java](http://mg4j.di.unimi.it/) | MG4J (Managing Gigabytes for Java) is a free full-text search engine for large document collections written in Java. MG4J is a highly customisable, high-performance, full-fledged search engine providing state-of-the-art features (such as BM25/BM25F scoring) and new research algorithms. The main points of MG4J are Powerful indexing, Multi-index interval semantics, Virtual fields, Clustering and lot more. |

以下重点介绍几个知名的开源搜索引擎：

## 3.1 Lucene

Lucene不是一个完整的全文索引应用，而是是一个用Java写的全文索引引擎工具包，它可以方便的嵌入到各种应用中实现针对应用的全文索引/检索功能。

### 使用案例

已经有很多Java项目都使用了Lucene作为其后台的全文索引引擎，比较著名的有：

- [J](http://www.jivesoftware.com/)[ive](http://www.jivesoftware.com/)：WEB论坛系统；
- [Eyebrows](http://eyebrowse.tigris.org/)：邮件列表HTML归档/浏览/查询系统，本文的主要参考文档“[TheLucene search engine: Powerful, flexible, and free](http://www.javaworld.com/javaworld/jw-09-2000/jw-0915-lucene_p.html)”作者就是EyeBrows系统的主要开发者之一，而EyeBrows已经成为目前APACHE项目的主要邮件列表归档系统。
- [Cocoon](http://xml.apache.org/cocoon/index.html):基于XML的web发布框架，全文检索部分使用了Lucene
- [Eclipse](http://www.eclipse.org/):基于Java的开放开发平台，帮助部分的全文索引使用了Lucene

Lucene的API接口设计的比较通用，输入输出结构都很像数据库的表==>记录==>字段，所以很多传统的应用的文件、数据库等都可以比较方便的映射到Lucene的存储结构/接口中。总体上看：可以先把**Lucene当成一个支持全文索引的数据库系统**。

### 创新之处

大部分的搜索（数据库）引擎都是用B树结构来维护索引，索引的更新会导致大量的IO操作，Lucene在实现中，对此稍微有所改进：不是维护一个索引文件，而是在扩展索引的时候不断创建新的索引文件，然后定期的把这些新的小索引文件合并到原先的大索引中（针对不同的更新策略，批次的大小可以调整），这样在不影响检索的效率的前提下，提高了索引的效率。

### 特点

|           | Lucene                                   | 其他开源全文检索系统                      |
| :-------- | :--------------------------------------- | :------------------------------ |
| 增量索引和批量索引 | 可以进行增量的索引(Append)，可以对于大量数据进行批量索引，并且接口设计用于优化批量索引和小批量的增量索引。 | 很多系统只支持批量的索引，有时数据源有一点增加也需要重建索引。 |
| 数据源       | Lucene没有定义具体的数据源，而是一个文档的结构，因此可以非常灵活的适应各种应用（只要前端有合适的转换器把数据源转换成相应结构）， | 很多系统只针对网页，缺乏其他格式文档的灵活性。         |
| 索引内容抓取    | Lucene的文档是由多个字段组成的，甚至可以控制那些字段需要进行索引，那些字段不需要索引，近一步索引的字段也分为需要分词和不需要分词的类型：   需要进行分词的索引，比如：标题，文章内容字段   不需要进行分词的索引，比如：作者/日期字段 | 缺乏通用性，往往将文档整个索引了                |
| 语言分析      | 通过语言分析器的不同扩展实现：可以过滤掉不需要的词：an the of 等，西文语法分析：将jumps jumped jumper都归结成jump进行索引/检索非英文支持：对亚洲语言，阿拉伯语言的索引支持 | 缺乏通用接口实现                        |
| 查询分析      | 通过查询分析接口的实现，可以定制自己的查询语法规则：比如： 多个关键词之间的 + - and or关系等 |                                 |
| 并发访问      | 能够支持多用户的使用                               |                                 |

## 3.2 Solr

Solr是Apache Lucene项目的开源企业搜索平台。其主要功能包括全文检索、命中标示、分面搜索、动态聚类、数据库集成，以及富文本（如Word、PDF）的处理。Solr是高度可扩展的，并提供了分布式搜索和索引复制。Solr是最流行的企业级搜索引擎，Solr4 还增加了NoSQL支持。

Solr 中存储的资源是以 Document 为对象进行存储的。每个文档由一系列的 Field 构成，每个 Field 表示资源的一个属性。Solr 中的每个 Document 需要有能唯一标识其自身的属性，默认情况下这个属性的名字是 id，在 Schema 配置文件中使用：id进行描述。

Solr是用Java编写、运行在Servlet容器（如 Apache Tomcat 或Jetty）的一个独立的全文搜索服务器。 Solr采用了 Lucene Java 搜索库为核心的全文索引和搜索，并具有类似REST的HTTP/XML和JSON的API。Solr强大的外部配置功能使得无需进行Java编码，便可对其进行调整以适应多种类型的应用程序。Solr有一个插件架构，以支持更多的高级定制。

因为2010年 Apache Lucene 和 Apache Solr 项目合并，两个项目是由同一个Apache软件基金会开发团队制作实现的。提到技术或产品时，Lucene/Solr或Solr/Lucene是一样的。

### Solr的优缺点

**优点**

1. Solr有一个更大、更成熟的用户、开发和贡献者社区。
2. 支持添加多种格式的索引，如：HTML、PDF、微软 Office 系列软件格式以及 JSON、XML、CSV 等纯文本格式。
3. Solr比较成熟、稳定。
4. 不考虑建索引的同时进行搜索，速度更快。

**缺点**

1. 建立索引时，搜索效率下降，实时索引搜索效率不高。



## 3.3 Sphinix

Sphinx是一个基于SQL的全文检索引擎，可以结合MySQL,PostgreSQL做全文搜索，它可以提供比数据库本身更专业的搜索功能，使得应用程序更容易实现专业化的全文检索。Sphinx特别为一些脚本语言设计搜索API接口，如PHP,Python,Perl,Ruby等，同时为MySQL也设计了一个存储引擎插件。

Sphinx 单一索引最大可包含1亿条记录，在1千万条记录情况下的查询速度为0.x秒（毫秒级）。Sphinx创建索引的速度为：创建100万条记录的索引只需 3～4分钟，创建1000万条记录的索引可以在50分钟内完成，而只包含最新10万条记录的增量索引，重建一次只需几十秒。

### 主要特性

* 高速索引 (在新款CPU上,近10 MB/秒)；


* 高速搜索 (2-4G的文本量中平均查询速度不到0.1秒)；


* 高可用性 (单CPU上最大可支持100 GB的文本,100M文档)；


* 提供良好的相关性排名；


* 支持分布式搜索；


* 提供文档摘要生成；


* 提供从MySQL内部的插件式存储引擎上搜索；


* 支持布尔,短语, 和近义词查询；


* 支持每个文档多个全文检索域(默认最大32个)；


* 支持每个文档多属性；


* 支持断词；


* 支持单字节编码与UTF-8编码。



## 3.4 Nutch

Nutch是Apache旗下的Java开源项目，最初是一个搜索引擎，现在是一个网络爬虫。

### 设计初衷

商业搜索引擎不开源，搜索结果不纯粹是根据网页本身的价值进行排序，而是有众多商业利益考虑。Nutch提供了开源的解决方案，帮助人们很容易地建立一个搜索引擎，为用户提供优质的搜索结果，并能从一台机器扩展到成百上千台

### 设计目标

* 每个月抓取几十亿网页


* 为这些网页维护一个索引


* 对索引文件执行每秒上千次的搜索


* 提供高质量的搜索结果


* 以最小的成本运作

### 整体架构

插件机制、数据抓取、数据解析、链接分析、建立索引、分布式搜索等。

对于一个搜索引擎来说，最终可能由成百上千台服务器组成，然而，初创公司最初可能只有几台机器作为尝试，随着公司的发展逐步增加机器，因此，线性可扩展的分布式存储与分布式计算是至关重要的。

Nutch参考了Google的两篇论文：MapReduce计算模型以及GFS存储模型，并做了实现，后来把这两大部分剥离出来形成独立的开源项目Hadoop。由此可知，Hadoop诞生于Nutch，核心由分布式计算和分布式存储组成，是MapReduce和GFS的JAVA开源实现。

Nutch使用HDFS作为存储实现一直持续了很多年，然而使用HDFS有许多限制，后来考虑对存储层进行抽象，剥离并形成了新的开源项目Gora，以支持多种存储技术，包括RDBMS和NoSQL。

对于搜索引擎来说，需要抓取各种各样的文件，解析这些不同格式的文件是一个难题，为了简化设计，也为了重用，于是诞生了Tika，一个专为内容分析而诞生的工具箱。



## 3.5 ElasticSearch

Elasticsearch是一个基于[Apache Lucene(TM)](https://lucene.apache.org/core/)的开源搜索引擎。无论在开源还是专有领域，Lucene可以被认为是迄今为止最先进、性能最好的、功能最全的搜索引擎库。

但是，Lucene只是一个库。想要使用它，你必须使用Java来作为开发语言并将其直接集成到你的应用中，更糟糕的是，Lucene非常复杂，你需要深入了解检索的相关知识来理解它是如何工作的。

Elasticsearch也使用Java开发并使用Lucene作为其核心来实现所有索引和搜索的功能，但是它的目的是通过简单的`RESTful API`来隐藏Lucene的复杂性，从而让全文搜索变得简单。

不过，Elasticsearch不仅仅是Lucene和全文搜索，我们还能这样去描述它：

- 分布式的实时文件存储，每个字段都被索引并可被搜索
- 分布式的实时分析搜索引擎
- 可以扩展到上百台服务器，处理PB级结构化或非结构化数据

而且，所有的这些功能被集成到一个服务里面，你的应用可以通过简单的`RESTful API`、各种语言的客户端甚至命令行与之交互。

上手Elasticsearch非常容易。它提供了许多合理的缺省值，并对初学者隐藏了复杂的搜索引擎理论。它开箱即用（安装即可使用），只需很少的学习既可在生产环境中使用。

Elasticsearch在[Apache 2 license](http://www.apache.org/licenses/LICENSE-2.0.html)下许可使用，可以免费下载、使用和修改。

### 交互方式

#### Java API

Elasticsearch为Java用户提供了两种内置客户端：

**节点客户端(node client)：**

节点客户端以无数据节点(none data node)身份加入集群，换言之，它自己不存储任何数据，但是它知道数据在集群中的具体位置，并且能够直接转发请求到对应的节点上。

**传输客户端(Transport client)：**

这个更轻量的传输客户端能够发送请求到远程集群。它自己不加入集群，只是简单转发请求给集群中的节点。

两个Java客户端都通过9300端口与集群交互，使用Elasticsearch传输协议(Elasticsearch Transport Protocol)。集群中的节点之间也通过9300端口进行通信。如果此端口未开放，你的节点将不能组成集群。

#### 基于HTTP协议，以JSON为数据交互格式的RESTful API

其他所有程序语言都可以使用RESTful API，通过9200端口的与Elasticsearch进行通信，你可以使用你喜欢的WEB客户端，事实上，如你所见，你甚至可以通过`curl`命令与Elasticsearch通信。

> **NOTE**
> 
> Elasticsearch官方提供了多种程序语言的客户端——Groovy，Javascript， .NET，PHP，Perl，Python，以及 Ruby——还有很多由社区提供的客户端和插件，所有这些可以在[文档](http://www.elasticsearch.org/guide/)中找到。

向Elasticsearch发出的请求的组成部分与其它普通的HTTP请求是一样的





### 使用案例

- 维基百科使用Elasticsearch来进行全文搜做并高亮显示关键词，以及提供search-as-you-type、did-you-mean等搜索建议功能。
- 英国卫报使用Elasticsearch来处理访客日志，以便能将公众对不同文章的反应实时地反馈给各位编辑。
- StackOverflow将全文搜索与地理位置和相关信息进行结合，以提供more-like-this相关问题的展现。
- GitHub使用Elasticsearch来检索超过1300亿行代码。
- 每天，Goldman Sachs使用它来处理5TB数据的索引，还有很多投行使用它来分析股票市场的变动。

### Elasticsearch的优缺点

**优点**

1. Elasticsearch是分布式的。不需要其他组件，分发是实时的，被叫做”Push replication”。
2. Elasticsearch 完全支持 Apache Lucene 的接近实时的搜索。
3. 处理多租户（[multitenancy](http://en.wikipedia.org/wiki/Multitenancy)）不需要特殊配置，而Solr则需要更多的高级设置。
4. Elasticsearch 采用 Gateway 的概念，使得完备份更加简单。
5. 各节点组成对等的网络结构，某些节点出现故障时会自动分配其他节点代替其进行工作。

**缺点**

1. 只有一名开发者（当前Elasticsearch GitHub组织已经不只如此，已经有了相当活跃的维护者）
2. 还不够自动（不适合当前新的Index Warmup API）



## 3.6 Xapian

Xapian是一个用C++编写的全文检索程序，他的作用类似于Java的lucene。尽管在Java世界lucene已经是标准的全文检索程序，但是C/C++世界并没有相应的工具，而Xapian则填补了这个缺憾。

Xapian除了提供原生的C++编程接口之外，还提供了Perl，PHP，Python和Ruby编程接口和相应的类库，所以你可以直接从自己喜欢的脚本编程语言当中使用Xapian进行全文检索了。

### 特点

* Xapian是一个允许开发人员轻易地添加高级索引和搜索功能到他们的应用系统的高度可修改的工具，它在支持概率论检索模型的同时也支持布尔型操作查询集
* Xapian和Lucene有点相似，两者都具有Term、Value（在Lucene里称为SortField）、Posting、Position和Document，不过Xapian没有Field的概念

### 性能

> The short answer is "very well" - a previous version of the software powered BrightStation's Webtop search engine, which offered a search over around 500 million web pages (around 1.5 terabytes of database files). Searches took less than a second。
> 
> 5亿个网页共1.5TB的文件，搜索用时小于一秒。
> 
> 当然，这跟运行的平台和机器是密切相关



# 四、相关主题

## 4.1 网络爬虫

网络爬虫（Web crawler），是一种“自动化浏览网络”的程序，或者说是一种网络机器人。它们被广泛用于互联网搜索引擎或其他类似网站，以获取或更新这些网站的内容和检索方式。它们可以自动采集所有其能够访问到的页面内容，以便程序做下一步的处理。

网络爬虫的工作流程如下：

![webcrawlerarchitecture](https://cloud.githubusercontent.com/assets/208154/11891777/a82e3368-a59c-11e5-950b-f2efff7a419f.png)

## 4.2 文本分词

这里主要介绍下中文分词。

中文分词(Chinese Word Segmentation) 指的是将一个汉字序列切分成一个一个单独的词。分词就是将连续的字序列按照一定的规范重新组合成词序列的过程。我们知道，在英文的行文中，单词之间是以空格作为自然分界符的，而中文只是字、句和段能通过明显的分界符来简单划界，唯独词没有一个形式上的分界符，虽然英文也同样存在短语的划分问题，不过在词这一层上，中文比之英文要复杂的多、困难的多。

常用的分词算法如下：

**字符串匹配的分词方法**

这是种常用的分词法，百度就是用此类分词。字符串匹配的分词方法，又分为3种分词方法。

* 正向最大匹配法

``` 
把一个词从左至右来分词。
举个例子：”不知道你在说什么”
这句话采用正向最大匹配法是如何分的呢？“不知道，你，在，说什么”。
```

* 反向最大匹配法

``` 
"不知道你在说什么"反向最大匹配法来分上面这段是如何分的。“不，知道，你在，说，什么”，这个就分的比较多了，反向最大匹配法就是从右至左。
```

* 最短路径分词法。

``` 
说一段话里面要求切出的词数是最少的。
“不知道你在说什么”最短路径分词法就是指，把上面那句话分成的词要是最少的。“不知道，你在，说什么”，这就是最短路径分词法，分出来就只有3个词了。
```

* 双向最大匹配法。

``` 
有一种特殊的情况，就是关键词前后组合内容被认为粘性相差不大，而搜索结果中也同时包含这两组词的话，百度会进行正反向同时进行分词匹配。
```

**词义分词法**

一种机器语音判断的分词方法。很简单，进行句法、[语义分析](http://baike.baidu.com/view/487035.htm)，利用句法信息和语义信息来处理歧义现象来分词，这种分词方法，还不成熟，处在测试阶段。

**统计分词法**

根据词组的统计，就会发现两个相邻的字出现的频率最多，那么这个词就很重要。就可以作为用户提供字符串中的[分隔符](http://baike.baidu.com/view/1268377.htm)，这样来分词。

比如，“我的，你的，许多的，这里，这一，那里”等等，这些词出现的比较多，就从这些词里面分开来。

## 4.3 分布式文件系统

Distributed file systems do not share block level access to the same storage but use a network protocol. These are commonly known as network file systems, even though they are not the only file systems that use the network to send data. Distributed file systems can restrict access to the file system depending on access lists or capabilities on both the servers and the clients, depending on how the protocol is designed. 

**Design goals**

Distributed file systems may aim for "transparency" in a number of aspects. That is, they aim to be "invisible" to client programs, which "see" a system which is similar to a local file system. Behind the scenes, the distributed file system handles locating files, transporting data, and potentially providing other features listed below.

- *Access transparency* is that clients are unaware that files are distributed and can access them in the same way as local files are accessed.
- *Location transparency*; a consistent name space exists encompassing local as well as remote files. The name of a file does not give its location.
- *Concurrency transparency*; all clients have the same view of the state of the file system. This means that if one process is modifying a file, any other processes on the same system or remote systems that are accessing the files will see the modifications in a coherent manner.
- *Failure transparency*; the client and client programs should operate correctly after a server failure.
- *Heterogeneity*; file service should be provided across different hardware and operating system platforms.
- *Scalability*; the file system should work well in small environments (1 machine, a dozen machines) and also scale gracefully to huge ones (hundreds through tens of thousands of systems).
- *Replication transparency*; to support scalability, we may wish to replicate files across multiple servers. Clients should be unaware of this.
- *Migration transparency*; files should be able to move around without the client's knowledge.

## 4.4 SEO(搜索引擎优化)

**搜索引擎优化**（**Search Engine Optimization**，简称**SEO**），是一种通过了解[搜索引擎](https://zh.wikipedia.org/wiki/%E6%90%9C%E5%B0%8B%E5%BC%95%E6%93%8E)的运作规则来调整[网站](https://zh.wikipedia.org/wiki/%E7%B6%B2%E7%AB%99)，以期提高目的[网站](https://zh.wikipedia.org/wiki/%E7%B6%B2%E7%AB%99)在有关搜索引擎内排名的方式。由于不少研究发现，搜索引擎的用户往往只会留意搜索结果最前面的几个条目，所以不少[网站](https://zh.wikipedia.org/wiki/%E7%B6%B2%E7%AB%99)都希望通过各种形式来影响搜索引擎的排序，让自己的[网站](https://zh.wikipedia.org/wiki/%E7%B6%B2%E7%AB%99)可以有优秀的搜索排名。当中尤以各种依靠广告维生的网站为甚。

所谓“针对搜索引擎作最优化的处理”，是指为了要让网站更容易被搜索引擎接受。搜索引擎会将网站彼此间的内容做一些相关性的数据比对，然后再由[浏览器](https://zh.wikipedia.org/wiki/%E7%80%8F%E8%A6%BD%E5%99%A8)将这些内容以最快速且接近最完整的方式，呈现给搜索者。搜索引擎优化就是通过搜索引擎的规则进行优化，为用户打造更好的用户体验，最终的目的就是做好用户体验。

对于任何一个网站来说，要想在网站推广中获取成功，搜索引擎优化都是至为关键的一项任务。同时，随着搜索引擎不断变换它们的搜索排名算法规则，每次算法上的改变都会让一些排名很好的网站在一夜之间名落孙山，而失去排名的直接后果就是失去了网站固有的可观访问流量。所以每次搜索引擎算演法的改变都会在网站之中引起不小的骚动和焦虑。可以说，搜索引擎优化是一个愈来愈复杂的任务。

**白帽方法**

搜索引擎优化的白帽法包括遵循搜索引擎哪些可接受哪些不能接受的指导方针。他们的建议一般是为用户创造内容，而非搜索引擎、是让这些内容易于被蜘蛛机器人索引、并且不尝试对搜索引擎系统耍花招。网站员经常于设计或构建他们的网站时，犯下致命错误、疏忽“毒害”该站以致排名不会很好。白帽法优化员企图发现并纠正错误，譬如机器无法读取的菜单、无效链接、临时改变导向、或粗劣的导引结构。

具体有：

- 在每页使用一个短、独特和相关的标题。
- 编辑网页，用与该页的主题。有关的具体术语替换隐晦的字眼。这有助于该站诉求的观众群，在搜索引擎上搜索而被正确导引至该站。
- 在该站点增加相当数量的原创内容。
- 使用合理大小、准确描述的汇标，而不过度使用关键字、惊叹号、或不相关标题术语。
- 确认所有页可通过正常的链接来访问，而非只能通过[Java](https://zh.wikipedia.org/wiki/Java) 、[JavaScript](https://zh.wikipedia.org/wiki/JavaScript)或[Adobe Flash](https://zh.wikipedia.org/wiki/Adobe_Flash)应用程序访问。这可通过使用一个专属列出该站所有内容的网页达成（[网站地图](https://zh.wikipedia.org/wiki/%E7%B6%B2%E7%AB%99%E5%9C%B0%E5%9C%96)）
- 通过自然方式开发链接：Google不花功夫在这有点混淆不清的指南上。写封电子邮件给网站员，告诉他：您刚刚贴了一篇挺好的文章，并且请求链接，这种做法很可能为搜索引擎所认可。
- 参与其他网站的网络集团（译按：[web ring](https://zh.wikipedia.org/w/index.php?title=Web_ring&action=edit&redlink=1) 指的是有相同主题的结盟站群）──只要其它网站是独立的、分享同样题目和可比较的质量。

**黑帽方法**

与白帽方法的主旨相反，通过一些『非法』手段来提高搜索条目的排名，具体有如下几种：

* [垃圾索引](https://zh.wikipedia.org/w/index.php?title=%E5%9E%83%E5%9C%BE%E7%B4%A2%E5%BC%95&action=edit&redlink=1)（Spamdexing）意指通过*欺骗技术*和滥用搜索算法来推销毫不相关、主要以商业为着眼的网页。许多搜索引擎管理员认为任何搜索引擎优化的形式，其目的用来改进网站的页排名者，都是垃圾索引。然而，随时间流逝，业界内公众舆论发展出哪些是哪些不是可接受的、促进某站的搜索引擎排名与流量结果的手段；


* [斗蓬法](https://zh.wikipedia.org/w/index.php?title=%E6%96%97%E8%93%AC%E6%B3%95&action=edit&redlink=1)（cloaking）简单来讲就是网站站长用了两版不同的网页来达到最优化的效果。一个版本只给搜索引擎看，一个版本给人看。搜索引擎说这种做法是不正规，如发现，该网站会永远从搜索引擎名单中被剔除。但是对于如AJAX所撰写的动态网页，Google也有提出名为HTML Snapshot的作法，以方便搜索引擎进行收录；


* [关键字隐密字](https://zh.wikipedia.org/w/index.php?title=%E9%97%9C%E9%8D%B5%E5%AD%97%E9%9A%B1%E5%AF%86%E5%AD%97&action=edit&redlink=1) （hidden text with keyword stuffing）是另外一欺骗搜索引擎的做法。通常是指设置关键字的颜色和网页背景颜色一样，或通过 css hidden attribute （隐密特性） 来达到优化效果。这种做法一旦被Google发现，遭遇也会是该网站从Google的数据库中除名。


* [桥页](https://zh.wikipedia.org/w/index.php?title=%E6%A9%8B%E9%A0%81&action=edit&redlink=1)（doorway pages）也叫门页，是通常是用软件自动生成大量包含关键词的网页，然后从这些网页做自动转向到主页。目的是希望这些以不同关键词为目标的桥页在搜索引擎中得到好的排名。当用户点击搜索结果的时候，会自动转到主页。有的时候是在桥页上放上一个通往主页的链接，而不自动转向主页。


* [付费链接](https://zh.wikipedia.org/w/index.php?title=%E4%BB%98%E8%B2%BB%E9%80%A3%E7%B5%90&action=edit&redlink=1)（paid link） 是利用支付费用方式要求其他网站提供链接至自身网站，借此伪装高信任网站来欺骗搜索引擎，付费链接类型多为锚点文字（Anchor Text）类型，Google的质量方针也明确指出以金钱交换的链接将可能对网站造成负面影响



# 五、开源搜索引擎的比较

## 5.1 Lucene 和Sphinx

> 著作权归作者所有。
> 
> 商业转载请联系作者获得授权，非商业转载请注明出处。
> 
> 作者：闫涛
> 
> 链接：https://www.zhihu.com/question/19583321/answer/12704316
> 
> 来源：知乎
> 
> 目前主流的开源搜索引擎主要有两个，一个是基于Java的Apache Lucene，另一个是基于C++的Sphinx。
> 
> 在建立索引所需时间方面，Sphinx只需Lucene时间的50%左右，但是索引文件Sphinx比Lucene要大一倍，即Sphinx采用的是空间换时间的策略。在全文检索速度方面，二者相差不大。全文检索精确度方面，Lucene要优于Sphinx。
> 
> 在加入中文分词引擎的难易程度上，Lucene要优于Sphinx。因此，在一般情况下，选择Lucene作为全文搜索引擎是比较好的选择。

## 5.2 ElasticSearch和Solr





* 当单纯的对已有数据进行搜索时，Solr更快。

![search_fresh_index_while_idle](https://cloud.githubusercontent.com/assets/208154/11891739/6c2e035c-a59c-11e5-852a-6b6354281c42.png)

* 当实时建立索引时, Solr会产生io阻塞，查询性能较差, Elasticsearch具有明显的优势。

![search_fresh_index_while_indexing](https://cloud.githubusercontent.com/assets/208154/11891738/6c2c573c-a59c-11e5-95e3-f35ad213fcbe.png)

* 随着数据量的增加，Solr的搜索效率会变得更低，而Elasticsearch却没有明显的变化。

![search_fresh_index_while_indexing2](https://cloud.githubusercontent.com/assets/208154/11891740/6c2e5942-a59c-11e5-95ad-ca3d9e6a5610.png)

综上所述，Solr的架构不适合实时搜索的应用

**比较总结**

- 二者安装都很简单；
- Solr 利用 Zookeeper 进行分布式管理，而 Elasticsearch 自身带有分布式协调管理功能；
- Solr 支持更多格式的数据，而 Elasticsearch 仅支持json文件格式；
- Solr 官方提供的功能更多，而 Elasticsearch 本身更注重于核心功能，高级功能多有第三方插件提供；
- Solr 在传统的搜索应用中表现好于 Elasticsearch，但在处理实时搜索应用时效率明显低于 Elasticsearch。

Solr 是传统搜索应用的有力解决方案，但 Elasticsearch 更适用于新兴的实时搜索应用。



# 六、应用案例

## 6.1 国内开源方案

### 6.1.1 迅搜 - xunsearch

> 免费开源的中文搜索引擎，采用 C/C++ 编写 (基于 xapian 和 scws)，提供 PHP 的开发接口和丰富文档

#### 盈利思路

* 开放代码，培养用户群
* 付费增值服务
  * 更大（千万、亿以上）的数据量
  * 分布式部署
  * 搜索性能优化
  * XSManager
  * 领域专有词库
  * 非结构化数据
  * 特殊检索需求

#### 使用协议

Xunsearch (包含 SDK 在内) 是一个免费开源的全文搜索软件，在以下描述的 GPL 通用许可证的条款下发布。

**官方提供、用户贡献的文档许可证**

* 官方提供以及用户贡献的文档内容以 GNU 自由文档许可证 (GFDL) 向公众授权。 在一般情况下，您可以自由的拷贝、修改、再发布　Xunsearch 文档内容，只要您赋予新版本同样的条款， 并保留文档作者署名。（在文章中添加链接指向原作者，或标明文档出处）。


* 您可以在 GNU 自由文档许可证 1.2 版或由自由软件基金会发布的更新版本条款下拷贝、分布或修改这些文档， 无固定段落，无封面文字，无封底文字。

**第三方组件的许可证**

软件包中包含的其它依赖或组件则保持其原有的方式授权，著作权也归原始作者所有。

* libevent BSD 协议


* xapian-core GPL 协议


* scws-1.x.y 未明确，但与 BSD 协议较为相似

#### 性能

> * 数据来源
>   
>     采集小说书本章节以及章节内容作为源数据,并存储到mysql数据库。100万数据,数据库大小为8.1G。
>   
> * 方法
>   
>     **建立索引时间**：从数据库中循环读取1000条循环建立索引。当$prefix/tmp/booktest_db.rcv、$prefix/tmp/booktest_db.snd文件都不存在时，读取索引日志文件$prefix/tmp/indexd.log最后一行booktest记录作为索引建立完成时间;
>   
>     **搜索速度**：索引建立完成后，执行7次不同任意关键词的第一次搜索，结果去掉最大和最小值，然后取5次的平均值;
>   
>     **索引大小**：获取$prefix/data/booktest/下，db和db_a的目录大小;
>   
> * 结论
>   
>     **建立索引时间**: 每1万条数据花费时间约为4.14分钟;
>   
>     **搜索速度**：100万数据搜索速度在0.5秒左右;
>   
>     **索引大小**：索引大小大约为数据大小的3.5倍;
>   
> * 环境
>   
>     操作系统：Ubuntu 10.04.3 LTS  2.6.32-33-server; 
>   
>     PHP：5.3.6;
>   
>     CPU：Intel(R) Xeon(R) CPU E5504 @ 2.00GHz; 
>   
>     内存大小:7.81G;
>   
> * 备注
>   
>     $prefix表示Xunsearch的安装目录;
>   
>     建立索引时从数据库中循环读取的执行时间，100万条数据约为2分钟(对结果影响不大，忽略此时间);
>   
> * 测试结果仅供参考;
> 
> ![xunsoutestresult](https://cloud.githubusercontent.com/assets/208154/11891785/af7d4500-a59c-11e5-8717-9631b23184fc.jpg)


### 6.1.2 腾讯 - Hermes

实时检索分析平台(Hermes)，旨在为公司大数据分析业务提供一套实时的、多维的、交互式的查询、统计、分析系统，为公司各个产品在大数据的统计分析方面提供完整的解决方案，让万级维度、千亿级数据下的秒级统计分析变为现实。

腾讯的Hermes系统，是**开源的lucene演变**而来，主要用的是搜索和索引技术，所以hermes也叫实时检索分析平台。

#### 技术特点

1. 核心是存储的设计， 通过对数据结构的重新组织，结合分析系统的特点，实现嵌套列存储，充分避开随机读，采用块读取+位图计算大幅度降低耗时弊病，使大数据的统计分析计算耗时缩短至秒级；在词条文件中采用字典排序，并在此基础上实现前缀压缩；在序列文件中采用递增排序，并对序列号采用可变长类型，有效压缩存储空间，便于计算位图的构建；
2. 列式存储；
3. 基于单个实例数据的分析处理，datasource主要包含两类数据：用户导入的数据(位图文件)以及源数据(索引文件)，内核主要根据用户请求逻辑处理索引文件以及位图文件；
4. 整个数据对应多份，按照不同规则均匀分布在各个分析实例中，数据的merge服务在其中的一个分片中进行，每次请求将根据机器负载情况选择负载轻的作为merge服务器

#### 索引特点

1. 大部分的索引处于关闭状态，只有真正用到索引才会去打开；一级跳跃表采用按需load，并不会load整个跳跃表，用来节省内存和提高打开索引的速度。Hermes经常会根据业务的不同去动态的打开不同的索引，关闭那些不经常使用的索引，这样同样一台机器，可以被多种不同的业务所使用，机器利用率高；
2. 排序和统计并不会使用数据的真实值，而是通过标签技术将大数据转换成占用内存很小的数据标签，占用内存是原先的几十分之一。另外不会将这个列的全部值都load到内存里，而是用到哪些数据load哪些数据，依然是按需load。不用了的数据会从内存里移除；
3. 索引存储在hdfs中，理论上只要hdfs有空间，就可以不断的添加索引，索引规模不在严重受机器的物理内存和物理磁盘的限制；
4. 采用yarn进行进程管理，数据在hdfs中，集群规模和扩容都是一件很easy的事情；
5. 如果某个词语存在数据倾斜，则会与其他条件组合进行跳跃合并（参考doclist的skiplist资料）；
6. 采用多级的merger server；数据可以根据业务的不同，采用不同的分区方式。

#### 应用案例

微信数据门户多维分析 (约370亿)

* 提供系统各个性能指标数据的实时分析。

信息安全部回溯项目(目前接入约2300亿)

* 基于全文检索查询、分析、统计并导出相关记录。


* 结果秒级返回。

#### 性能

![hermes-performance](https://cloud.githubusercontent.com/assets/208154/11891742/6c32a1be-a59c-11e5-8921-34eccf49d476.png)

### 6.1.3 一号店

1号店分布式搜索引擎是[Lucene/Solr](http://www.infoq.com/cn/articles/Apache%20Lucene/Solr%20http://lucene.apache.org/)核心的，结合SOA框架Hedwig构建了一层分布式框架，支持搜索请求的分发和合并，并且构建了搜索管理后台，支持多索引管理、集群管理、全量索引切换和实时索引更新。

#### 技术方案

选择自己构建分布式方案，而不是采用开源的SolrCloud或[ElasticSearch](http://www.infoq.com/cn/articles/ElasticSearch%20https://www.elastic.co/)，主要是基于以下几点考虑：

1. ElasticSearch/SolrCloud都**适合于把搜索引擎作为一个黑盒**系统来使用，而1号店搜索业务的展现形式多样性很高，搜索条件有的会很复杂，有的需要通过自定义插件来实现，性能调优时也需要对引擎内部的执行细节进行监控。
2. 将ElasticSearch/SolrCloud与公司内部的发布系统、监控系统和SOA体系结合起来，也是一项比较耗时的工作。
3. 相对于整体使用，我们更倾向于**把Lucene/Solr开源家族中的各个组件按需引入**，一方面降低引入复杂工程的可维护性风险，另一方面逐渐深入理解这些组件，可以在必要时替换为定制化的组件。



# 参考文献

1. [Wikipedia: 搜索引擎](https://zh.wikipedia.org/wiki/%E6%90%9C%E7%B4%A2%E5%BC%95%E6%93%8E)
2. [61 best open source search engine projects.](http://www.findbestopensource.com/tagged/search-engine)
3. [迅搜](http://www.xunsearch.com/)
4. [迅搜 - 性能测试](http://www.xunsearch.com/site/performance)
5. [搜索引擎选择：Elasticsearch与Solr](http://i.zhcy.tk/blog/elasticsearchyu-solr/)
6. [NUTCH公开课：从搜索引擎到网络爬虫](http://yangshangchuan.iteye.com/blog/1941498)
7. [Lucene：基于Java的全文检索引擎简介](http://www.chedong.com/tech/lucene.html)
8. [Hermes实时检索分析平台](http://data.qq.com/article?id=817)
9. [腾讯实时检索分析平台hermes介绍](http://jiezhu2007.iteye.com/blog/2166035)
10. [利用Xapian构建自己的搜索引擎：Xapian简介](http://blog.csdn.net/visualcatsharp/article/details/4176083)
11. [爬虫技术浅析](http://drops.wooyun.org/tips/3915)
12. [如何自己写一个网络爬虫](http://coolshell.cn/articles/27.html)
12. [Wikipedia: Web crawler](https://en.wikipedia.org/wiki/Web_crawler)
13. [Wikipedia: Clustered_file_system](https://en.wikipedia.org/wiki/Clustered_file_system)
14. [百度百科: SEO](http://baike.baidu.com/view/1047.htm)
15. [Wikipedia: 搜索引擎优化](https://zh.wikipedia.org/wiki/%E6%90%9C%E5%B0%8B%E5%BC%95%E6%93%8E%E6%9C%80%E4%BD%B3%E5%8C%96)
16. [1号店11.11：分布式搜索引擎的架构实践](http://www.infoq.com/cn/articles/yhd-11-11-distributed-search-engine-architecture)
