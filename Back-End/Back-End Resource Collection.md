# 后端相关资源汇总

## 运行时

### Node.JS

#### 知识学习

[【全文】狼叔：如何正确的学习Node.js](https://cnodejs.org/topic/5ab3166be7b166bb7b9eccf7)：知乎 Live 文字稿

[迷茫时学习Node.js最好的方法](https://cnodejs.org/topic/59c75a3dd7cbefc511964688)：狼叔指点 Node.js 的学习方法，适合于初级阶段

[高可用架构专用《全栈工程师之路-Node.js》](https://github.com/i5ting/nodejs-fullstack)

#### 编码规范

[Node.js Best Practices](https://github.com/i0natan/nodebestpractices)

#### 性能调优

[唯快不破，让nodejs再快一点](https://github.com/alibaba/beidou/blob/master/packages/beidou-docs/articles/node-performance-optimization.md)：应用阿里开发的 alinode，对 Node.js 代码进行分析并调优。

#### 库 & 框架

无

## 语言

### C Sharp

#### 编码规范

[C# Coding Conventions (C# Programming Guide)](https://msdn.microsoft.com/en-us/library/ff926074.aspx)：MSDN官方的C#编程规范

[Secure Coding Guidelines](https://msdn.microsoft.com/en-us/library/8a3x2b7f.aspx)：MSDN上的安全编码规范

### MVC

[ASP.NET Routing | MSDN](https://msdn.microsoft.com/en-us/library/cc668201.aspx)：非常适合入门学习 Route 部分。精炼地介绍了 Route 中的各个知识点，并有实际代码辅助理解，真是官方的良心文档！

[Controllers and Action Methods in ASP.NET MVC Applications](https://msdn.microsoft.com/en-us/library/dd410269(v=vs.100).aspx)：很简单地介绍了 Controller 和其中的 Action Methods，真的是很简单……

[Model-View-Controller (MVC) Explained Through Ordering Drinks At The Bar](https://medium.freecodecamp.org/model-view-controller-mvc-explained-through-ordering-drinks-at-the-bar-efcba6255053)

### ASP.NET

#### 业务实现

##### Controller 中获取 Route 中的参数

- Google: `asp.net mvc controller get data from route`

- [Get Route Parameter Value in Controller](https://forums.asp.net/t/1386372.aspx?Get+Route+Parameter+Value+in+Controller)：在 Controller 中，用 `string Id = (string)this.RouteData.Values["id"];` 这样的语句即可，不过在 Route 中，需要声明 `id` 这个变量：

```cs
routes.MapRoute(
    name: "Test",
    url: "Test/tspt/{bookName}/{id}.html",
    defaults: new { controller = "Test", action = "Index", id = UrlParameter.Optional }
);
```

##### 从 Controller 向 View 传数据

- Google: `asp.net mvc pass parameter from controller to view`

- [Various Ways to Pass Data From Controller to View in MVC](http://www.c-sharpcorner.com/UploadFile/abhikumarvatsa/various-ways-to-pass-data-from-controller-to-view-in-mvc/)：在 Controller 中，为 `ViewBag` 这个实例添加属性并赋值，然后在 View 中使用属性即可。

```cs
// TestController.cs
string Id = (string)this.RouteData.Values["id"];
ViewBag.Id = Id;

// Index.cshtml
@{
    var src = "/tspt/xztxyy3b/audio/" + ViewBag.Id + ".mp3";
}
...
<source src=@src type="audio/mp3">
```

#### 开发规范

[Best Practices For ASP.NET MVC Application](http://www.c-sharpcorner.com/article/best-practices-for-asp-net-mvc-application/)：ASP.NET MVC 应用最佳实践

[ASP.NET MVC Solution Architecture – Best Practices](https://chsakell.com/2015/02/15/asp-net-mvc-solution-architecture-best-practices/)：第一次大致看了一遍，应该是自底向上把每一层该如何设计都大致讲了一下，配套的源码就在 GitHub 上：[mvcarchitecture](https://github.com/chsakell/mvcarchitecture)。

[ASP.NET MVC开发：Web项目开发必备知识点](http://www.cnblogs.com/lixiaobin/p/MvcWebLearn.html)

#### 知识学习

[the-best-way-to-learn-aspnet--net-22404](https://code.tutsplus.com/tutorials/the-best-way-to-learn-aspnet--net-22404)，讲述ASP.NET的学习路线，推荐了几本书籍和大体的学习方法。

#### 性能优化

[提高 ASP.NET Web 应用性能的 24 种方法和技巧](https://segmentfault.com/a/1190000004352989)：讲的都是具体的技术实现方面的细节。

#### 上传功能

[How to Implement a Web API controller to accept chunked uploads using JQuery File Upload?](http://stackoverflow.com/questions/26546296)，讲解如何用jQuery File Upload控件实现分片上传。

[File Upload Without Page Refresh in ASP.NET MVC](http://www.codeproject.com/Articles/1108516/File-Upload-Without-Page-Refresh-in-ASP-NET-MVC)

[随便说说：在ASP.NET应用程序中上传文件](http://blog.zhaojie.me/2008/02/aspnet-upload.html)

搜索关键字：Search "asp.net upload" in Code Project

## API

[7 Rules for REST API URI Design](http://blog.restcase.com/7-rules-for-rest-api-uri-design/)

[【译】RESTful API 设计最佳实践](https://segmentfault.com/a/1190000011516151)

[【目标不加班】善用API统一描述语言提升RestAPI开发效率](https://segmentfault.com/a/1190000010910896)

[我所理解的接口设计](https://segmentfault.com/a/1190000013703264)：正文和回复都干货满满，都是实际的业务经验。

[RESTful – 移动互联网时代的高效API架构风格](http://www.makmong.com/1009.html)：后端.NET配套方案：Asp.Net WebApi，或者[Nancy](http://nancyfx.org)

### PHP

#### 编码规范

[PHP Standards Recommendations - PHP-FIG](http://www.php-fig.org/psr/)：目前最普遍采用的PHP编码规范

#### 代码安全

[PHP安全编码 - 枪与玫瑰](https://www.mudoom.com/php%E5%AE%89%E5%85%A8%E7%BC%96%E7%A0%81/)

[SQL注入如何防范?](https://segmentfault.com/q/1010000005688399)

[PHP 代码安全检测](http://blog.csdn.net/mervyn1205/article/details/39989693)

[Handle $_GET safely PHP](http://stackoverflow.com/questions/9759188/handle-get-safely-php)

[PHP safe $_GET or not](http://stackoverflow.com/questions/3388983/php-safe-get-or-not)

[Calling PHP functions within HEREDOC strings](http://stackoverflow.com/questions/104516/calling-php-functions-within-heredoc-strings)

[Data Encoding: A Guide to UTF-8 for PHP and MySQL](https://www.toptal.com/php/a-utf-8-primer-for-php-and-mysql)

## IDE

### Visual Studio

#### 插件

[Visual Studio Marketplace](https://marketplace.visualstudio.com/)：Visual Studio官方的插件网站，收录了很多好用的插件。

[Visual Studio 有哪些好用的插件？](https://www.zhihu.com/question/20617534)

[API文档自动生成工具：DocFX](http://dotnet.github.io/docfx/)

## 数据库

### 安装参考

[How To Install SQL 2008 R2 on Windows Server 2008 R2 SP1 For Use With SCVMM 2008 R2 SP1](https://blogs.technet.microsoft.com/danstolts/2011/04/how-to-install-sql-2008-r2-on-windows-server-2008-r2-sp1-for-use-with-scvmm-2008-r2-sp1/)

### 安全

[Gitlab从删库到恢复 - 数据库备份\恢复\容灾\HA的靠谱姿势](https://yq.aliyun.com/articles/69179)

[The Hitchhiker's Guide to SQL Injection prevention](https://phpdelusions.net/sql_injection)

[SQL注入如何防范?](https://segmentfault.com/q/1010000005688399)

[Basic SQL Server security best practices](http://searchsqlserver.techtarget.com/feature/Basic-SQL-Server-security-best-practices)

[Microsoft SQL Server security best practices checklist](http://searchsqlserver.techtarget.com/tip/Microsoft-SQL-Server-security-best-practices-checklist)

[MySQL安全策略](http://imysql.com/2016/03/15/sth-about-mysql-data-security.shtml)

### 规范

[SQL Server Table and Column Naming Conventions](http://www.codeproject.com/Articles/1065295/SQL-Server-Table-and-Column-Naming-Conventions)

[SQL Server 数据库设计规范](http://www.cnblogs.com/chenmh/p/3944116.html)

[浅析Sql Server参数化查询](http://www.cnblogs.com/lzrabbit/archive/2012/04/21/2460978.html)

[安居客 MySQL 使用规范](https://github.com/anjuke/coding-style/blob/master/mysql/mysql-guideline.md)

## 服务器

[Windows Server 性能监控最佳实践](https://www.datadoghq.com/blog/monitoring-windows-server-2012/): 系列一共三篇文章，第一篇讲基础知识，第二篇讲如何用 Windows Server 自带的功能做性能监控，第三篇讲如何用软件做性能监控，值得一读。

相关关键字：`windows server performance monitoring best practices`

[Web开发者手边的一本CentOS小书](https://array-huang.gitbooks.io/centos-book/content/)

[入门用户的网站服务器安全技巧](https://segmentfault.com/a/1190000004178690)

[服务器安全基础指南](https://segmentfault.com/a/1190000005753282)

[Configure Web Server Security (IIS 7)](https://technet.microsoft.com/en-us/library/cc731278%28v=ws.10%29.aspx?f=255&MSPPError=-2147217396)

[Apache Security Tips](https://httpd.apache.org/docs/2.4/misc/security_tips.html)：注意Apache版本

---

## ASP.NET 系统学习

### 学习资源

★★★★★ [ASP.NET MVC Tutorials](http://www.tutorialsteacher.com/mvc/asp.net-mvc-tutorials)：教程图文并茂，每一小节都很短，并且最后往往还会有本节知识点的总结回顾，有时还会罗列出建议阅读的资料，真！良！心！

建议按顺序学习，2017年5月16日，目前的价格是每门课10美元。

1. [C# Basics for Beginners: Learn C# Fundamentals by Coding](https://www.udemy.com/csharp-tutorial-for-beginners/) 
1. [C# Intermediate: Classes, Interfaces and OOP](https://www.udemy.com/csharp-intermediate-classes-interfaces-and-oop/) 
1. [C# Advanced Topics: Take Your C# Skills to the Next Level](https://www.udemy.com/csharp-advanced/) 
1. [Entity Framework in Depth: The Complete Guide](https://www.udemy.com/entity-framework-tutorial/) 
1. [The Complete ASP.NET MVC 5 Course](https://www.udemy.com/the-complete-aspnet-mvc-5-course/) 
1. 06_Become a Full-stack .NET Developer
1. 07_Become a Full-stack .NET Developer - Advanced Topics
1. 08_Become a Full-stack .NET Developer - Architecture and Testing

### 最佳实践

- Google： `asp.net mvc best practise`

### 话题探讨

- Google关键字： `asp net mvc code first vs database first`

### **学习路线**

#### 重新规划

- [ASP.NET MVC | Microsoft Docs](https://docs.microsoft.com/en-us/aspnet/mvc/)
- [ASP.NET MVC - 教程 | W3School](http://www.w3school.com.cn/aspnet/mvc_intro.asp)
- Google: `asp.net mvc 教程`
- Google: `asp.net mvc 入门`

#### 过往资料

- [What is the best (and fastest) way to learn ASP.NET MVC?](https://www.danylkoweb.com/Blog/what-is-the-best-and-fastest-way-to-learn-aspnet-mvc-8V)
- [What are the best resources to learn asp.net MVC?](https://www.quora.com/What-are-the-best-resources-to-learn-asp-net-MVC)
