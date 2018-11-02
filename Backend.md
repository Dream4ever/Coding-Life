# 后端相关资源汇总

## 技术选型

[Choosing a (Language) Stack](https://engineering.wework.com/choosing-a-language-stack-cac3726928f6)

> 一家公司的技术团队需要为后端业务选出新的语言：Go、Kotlin，还是 Ruby？文章首先描述了需要进行定性对比和定量对比的指标，然后讲了需要用三种语言开发并测试的一项业务。在此基础之上，对用三种语言开发出来的业务分别进行了负载测试，Go 以微小的优势胜出。接着又对负载测试的结果进行分析，并说明了技术团队最终选择 Go 语言的原因。另外，还分别介绍了用这三种语言开发业务时的思路，需要注意的地方，每种语言的长处和不足。对于希望在技术的道路上更进一步的同学，不管是前端，还是后端，或者别的什么岗位，都可以看看这篇文章。不只是可以看技术，也可以学习这次语言优选背后的思路，真的是学无止境。

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

## API

[7 Rules for REST API URI Design](http://blog.restcase.com/7-rules-for-rest-api-uri-design/)

[【译】RESTful API 设计最佳实践](https://segmentfault.com/a/1190000011516151)

[【目标不加班】善用API统一描述语言提升RestAPI开发效率](https://segmentfault.com/a/1190000010910896)

[我所理解的接口设计](https://segmentfault.com/a/1190000013703264)：正文和回复都干货满满，都是实际的业务经验。

[RESTful – 移动互联网时代的高效API架构风格](http://www.makmong.com/1009.html)：后端.NET配套方案：Asp.Net WebApi，或者[Nancy](http://nancyfx.org)

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

[浅谈数据库用户表结构设计](http://wpceo.com/user-database-table-design/)

## 服务器

[Windows Server 性能监控最佳实践](https://www.datadoghq.com/blog/monitoring-windows-server-2012/): 系列一共三篇文章，第一篇讲基础知识，第二篇讲如何用 Windows Server 自带的功能做性能监控，第三篇讲如何用软件做性能监控，值得一读。

相关关键字：`windows server performance monitoring best practices`

如何查看 IIS 并发？利用性能计数器即可

[基于ELK实现Windows服务器系统日志监控](https://bbs.huaweicloud.com/blogs/e9dcf82bc39611e7b8317ca23e93a891)

[Web开发者手边的一本CentOS小书](https://array-huang.gitbooks.io/centos-book/content/)

[入门用户的网站服务器安全技巧](https://segmentfault.com/a/1190000004178690)

[服务器安全基础指南](https://segmentfault.com/a/1190000005753282)

[Configure Web Server Security (IIS 7)](https://technet.microsoft.com/en-us/library/cc731278%28v=ws.10%29.aspx?f=255&MSPPError=-2147217396)

[Apache Security Tips](https://httpd.apache.org/docs/2.4/misc/security_tips.html)：注意Apache版本
