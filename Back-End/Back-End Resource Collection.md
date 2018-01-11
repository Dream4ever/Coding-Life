# 后端相关资源汇总

## 语言

### C#

#### 编码规范

[C# Coding Conventions (C# Programming Guide)](https://msdn.microsoft.com/en-us/library/ff926074.aspx)：MSDN官方的C#编程规范

[Secure Coding Guidelines](https://msdn.microsoft.com/en-us/library/8a3x2b7f.aspx)：MSDN上的安全编码规范

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

## 框架

### Node.JS

#### 编码规范

[Node.js Best Practices](https://github.com/i0natan/nodebestpractices)

#### 库 & 框架

[BigPipe](https://github.com/bigpipe/bigpipe)：以分块的方式（`Pagelets`）向前端传送页面，实现渐进式的加载

### MVC

[Model-View-Controller (MVC) Explained Through Ordering Drinks At The Bar](https://medium.freecodecamp.org/model-view-controller-mvc-explained-through-ordering-drinks-at-the-bar-efcba6255053)

[ASP_NET_MVC3_请求处理流程(1) MVC请求入口](http://blog.csdn.net/a497785609/article/details/50097451)

### ASP.NET

#### 业务实现

##### Controller 中获取 Route 中的参数

Google: `asp.net mvc controller get data from route`

[Get Route Parameter Value in Controller](https://forums.asp.net/t/1386372.aspx?Get+Route+Parameter+Value+in+Controller)：在 Controller 中，用 `string Id = (string)this.RouteData.Values["id"];` 这样的语句即可，不过在 Route 中，需要声明 `id` 这个变量：

```cs
routes.MapRoute(
    name: "Test",
    url: "Test/tspt/{bookName}/{id}.html",
    defaults: new { controller = "Test", action = "Index", id = UrlParameter.Optional }
);
```

#### 开发规范

[Best Practices For ASP.NET MVC Application](http://www.c-sharpcorner.com/article/best-practices-for-asp-net-mvc-application/)：ASP.NET MVC 应用最佳实践

[ASP.NET MVC Solution Architecture – Best Practices](https://chsakell.com/2015/02/15/asp-net-mvc-solution-architecture-best-practices/)：第一次大致看了一遍，应该是自底向上把每一层该如何设计都大致讲了一下，配套的源码就在 GitHub 上：[mvcarchitecture](https://github.com/chsakell/mvcarchitecture)。

[ASP.NET MVC开发：Web项目开发必备知识点](http://www.cnblogs.com/lixiaobin/p/MvcWebLearn.html)

#### 知识学习

[the-best-way-to-learn-aspnet--net-22404](https://code.tutsplus.com/tutorials/the-best-way-to-learn-aspnet--net-22404)，讲述ASP.NET的学习路线，推荐了几本书籍和大体的学习方法。

#### WebAPI

2018年1月8日新增

[前后端分离的思考与实践（一）](http://taobaofed.org/blog/2014/04/05/practice-of-separation-of-front-end-from-back-end/)

[Getting Started with ASP.NET Web API 2 (C#)](https://docs.microsoft.com/en-us/aspnet/web-api/overview/getting-started-with-aspnet-web-api/tutorial-your-first-web-api)

Google: `前端vue 后端asp.net`

[asp.net mvc 项目中怎么用react redux,vue 等前端框架？](https://www.zhihu.com/question/57766078)

[ASP.NET Core + Vue.js 开发记录系列文章](http://www.wangziwen.vip/2017/11/04/aspnet-core-vuejs-kf01/)

[Is Node.js declining already?](https://www.quora.com/Is-Node-js-declining-already)

---

[C#开发REST WEB API有哪些方法？](https://segmentfault.com/q/1010000011128866)

[ASP.NET Web API 2 - MSDN](https://msdn.microsoft.com/en-us/library/dn448365%28v=vs.118%29.aspx?f=255&MSPPError=-2147217396)

[ASP.NET MVC Web API Post FromBody（Web API 如何正确 Post）](http://www.cnblogs.com/xishuai/p/aspnet_mvc_web_api_httpclient_json_frombody_post.html)

[WebApi中使用 Asp.Net Identity 进行身份认证](http://ymhou.github.io/2016/07/02/WebApi-use-Asp-Net-Identity/)

[ASP.NET Web API 入门实战系列](http://ymhou.github.io/2016/09/10/aspnet-webapi-1/)：从基本的EF数据库的创建，到API的自动生成，以及最后的单页应用示例，基础的部分都简单介绍了一下，适合入门。

#### 微信SDK

[微信公众平台SDK Senparc.Weixin for C#](https://github.com/JeffreySu/WeiXinMPSDK)

#### 性能优化

[提高 ASP.NET Web 应用性能的 24 种方法和技巧](https://segmentfault.com/a/1190000004352989)：讲的都是具体的技术实现方面的细节。

#### 上传功能
 
[How to Implement a Web API controller to accept chunked uploads using JQuery File Upload?](http://stackoverflow.com/questions/26546296)，讲解如何用jQuery File Upload控件实现分片上传。

[File Upload Without Page Refresh in ASP.NET MVC](http://www.codeproject.com/Articles/1108516/File-Upload-Without-Page-Refresh-in-ASP-NET-MVC)

[随便说说：在ASP.NET应用程序中上传文件](http://blog.zhaojie.me/2008/02/aspnet-upload.html)

搜索关键字：Search "asp.net upload" in Code Project

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

[Configure Web Server Security (IIS 7)](https://technet.microsoft.com/en-us/library/cc731278%28v=ws.10%29.aspx?f=255&MSPPError=-2147217396)

[Apache Security Tips](https://httpd.apache.org/docs/2.4/misc/security_tips.html)：注意Apache版本
