# 应用服务器
### 简介

应用服务器的主要作用是与数据库建立连接，暴露一个RESTful API服务给Web前端使用。

应用服务器采用Java实现，使用的框架有

|框架/依赖|
|----|
| Spring Boot         |
| Spring Framework    |
| Spring Security     |
| Spring Data MongoDB |
| Spring Data REST    |
| Spring REST Docs    |
| Lombok              |

由于现在最流行的后端框架就是Java的**SpringBoot**，所以本系统采取了该框架，而本系统通常来说不需要长时间的大量IO的操作，所以没有考虑Spring Webflux，转而使用了传统的Spring MVC框架。
本文将结合系统采用的Spring各框架，介绍该应用服务器的基本框架。

如图为Spring MVC的架构图。Front controller即为DispatcherServlet

![mvc](/imgs/mvc.png)

如图为Spring Security的过滤链架构图

![filterchain](/imgs/multi-securityfilterchain.png)

