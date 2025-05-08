## 1.Spring相关资源地址

​	官网地址：https://spring.io/projects/spring­framework#overview 

spring5中文手册：https://github.com/DocsHome/spring-

docs/blob/master/SUMMARY.md

压缩包下载地址：https://repo.spring.io/list/libs-snapshot-

local/org/springframework/spring/

源码地址：https://github.com/spring­projects/spring­framework

## 2.什么是spring

Spring 是一个轻量级的开源框架。

Spring能很好解决企业级应用开发的业务逻辑和其他各层之间的耦合度问题。

Spring是一个**IOC**和**APO**的容器框架

​		**IOC** ：为控制反转。

​		**Aop** ：为面向切面编程。

​		容器 ：包含并管理应用对象的生命周期。

Spring可以做很多事情，它为企业级开发提供给了丰富的功能，但是这些功能

的底层都依赖于它的两个核心特性，也就是**依赖注入（dependency**

**injection，DI）和面向切面编程（**

**aspect-oriented programming，**

**AOP）**。

### 	spring的模块划分图

![image-20230219194109156](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20230219194109156.png)

模块解释：

Test:Spring的单元测试模块

Core Container:核心容器模块

AOP+Aspects:面向切面编程模块

Instrumentation:提供了class instrumentation支持和类加载器的实现来在特定的应用服务器上使用,几乎

不用

Messaging:包括一系列的用来映射消息到方法的注解,几乎不用

Data Access/Integration:数据的获取/整合模块，包括了JDBC,ORM,OXM,JMS和事务模块

Web:提供面向web整合特性