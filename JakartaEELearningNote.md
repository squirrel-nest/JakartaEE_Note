# Jakarta EE 8 Reference
## 前瞻性 - 在开始Java EE 的学习旅程之前，先了解了解 前瞻性的问题，把握好学习的方向，2020.4.5 -之后这些也许又落伍了 - 理解：周虽旧邦，其命维新 的 发展规律
   * [https://zhuanlan.zhihu.com/p/78720067](云原生时代JAVA语言的求生之路) - 参考其中的 reference<br>
   * [Java生态系统总结(QCon2019)](http://monkeybean.cn/2019/05/12/qcon2019/)<br>
   * [Kubernetes 是什么？](https://kubernetes.io/zh/docs/concepts/overview/what-is-kubernetes/)<br>
   * [EE4J Projects - Technical Direction](https://docs.google.com/document/d/12vO9Ztcxyd6oxDnKFi73p7JsYaPgifpepggFxzW_uyE/edit#)<br>
   * [GraalVM - High-performance polyglot VM: What does GraalVM do?](https://www.graalvm.org/)<br>
   * [Spring Cloud 使用 Kubernetes 作为配置中心 - 使用加密配置](https://blog.csdn.net/u013360850/article/details/100635538)<br>
## SDK Download
   * [Java™ EE 8 SDK Downloads](https://www.oracle.com/java/technologies/javaee-8-sdk-downloads.html)<br>


## Jakarta EE 8 的学习路径

### Jakarta EE Persistence --> [JakartaEEPersistenceLearningNote.md](https://github.com/squirrel-nest/JavaEELearningNote/blob/master/JakartaEEPersistenceLearningNote.md)


## Tutorials - Google Search: jakarta ee tutorial | jakarta ee 8 tutorial
   * [eclipse-ee4j/jakartaee-tutorial](https://github.com/eclipse-ee4j/jakartaee-tutorial) - Migrated from [javaee/tutorial](https://github.com/javaee/tutorial) --> [The Jakarta EE 8 Tutorial - DRAFT](https://eclipse-ee4j.github.io/jakartaee-tutorial/toc.html)<br>
      + >This repository contains the source files that are used to build the Jakarta Enterprise Edition (Jakarta EE) Tutorial. The source files are authored in AsciiDoc. AsciiDoc is similar to markdown but is particularly suited for user documentation. This project also uses JBake. JBake is a static site generator that is inspired from Jekyll and written in Java. JBake uses templates for the structure of the page and the body of the page is generated from AsciiDoc content.
      + >
      + >Note that the Jakarta EE Tutorial code examples are located in a separate repository eclipse-ee4j/jakartaee-tutorial-examples.
   * [Jakarta EE Platform - spec-8](https://jakarta.ee/specifications/platform/8/platform-spec-8.pdf) - PDF 文档 - 文档的GitHub资源：[Jakarta EE Platform Specification](https://github.com/eclipse-ee4j/jakartaee-platform/tree/master/specification) - eclipse-ee4j/jakartaee-platform<br>
      + [JAXB and JAX-WS no longer part of Java EE platform](https://javaee.github.io/glassfish/doc/5.0/release-notes.pdf#G3.1520176) - **深入了解一下**<br>
   * [Getting started with Jakarta EE](http://www.mastertheboss.com/javaee/jakarta-ee/getting-started-with-jakarta-ee)<br>
   * [rieckpil/blog-tutorials](https://github.com/rieckpil/blog-tutorials) - 备注：这个例子比较新，参考<br>
      + [Bootstrap your first Jakarta EE 8 application](https://rieckpil.de/howto-bootstrap-your-first-jakarta-ee-8-application/) - 创建Maven 与 Gradle 共生的 例子，以这个教程为 模板<br>
      + [Jakarta EE 8 CRUD API Tutorial using Java 11](https://rieckpil.de/jakarta-ee-crud-api-tutorial/)<br>
   * [​Java tutorials for both Java EE & Jakarta EE and the Spring ecosystem](https://rieckpil.de/#/blog) - Example 下一条<br>
      + [Java EE 8/Jakarta EE 8 Sandbox](https://github.com/hantsy/ee8-sandbox)<br>
## 一些知识背景介绍等
   * [Java EE vs J2EE vs Jakarta EE](https://www.baeldung.com/java-enterprise-evolution)<br>
   * [Jakarta EE 8 and Beyond](https://dzone.com/articles/jakarta-ee-8-and-beyond)<br>
   * [Jakarta EE 8: Past, Present, and Future](https://jaxenter.com/jakarta-ee-8-past-present-future-161990.html)<br>
   * [Jakarta EE 8: The new era of Java EE explained](https://developers.redhat.com/blog/2019/09/12/jakarta-ee-8-the-new-era-of-java-ee-explained/)<br>

## Examples - Google Search: github java ee projects opensource example site:github.com | jakarta ee example | github jakarta ee projects opensource example site:github.com
   * [Jakarta EE Examples](https://projects.eclipse.org/proposals/jakarta-ee-examples) - 这个是官网的Examples 的即介绍，认真先看。优先看。。。<br>
   * [daggerok/java-ee-examples](https://github.com/daggerok/java-ee-examples) - 用到了Kotlin语言，参考看看<br>
   * [manorrock/jakartaee-examples](https://github.com/manorrock/jakartaee-examples) - 非常经典，已贡献给Eclipse Foundation<br>
      + >This repository has been donated to the Eclipse Foundation, click [here](https://github.com/eclipse-ee4j/jakartaee-examples) ->  [eclipse-ee4j/jakartaee-examples] to go to its new home.
        ```
           This repository has been deprecated and will be removed August 1st, 2020.
        ```

   * [Examples for Jakarta EE](https://projects.eclipse.org/projects/ee4j.jakartaee-examples/developer)<br>
      + [eclipse-ee4j/jakartaee-examples](https://github.com/eclipse-ee4j/jakartaee-examples) - 是上面一个新的Github源位置<br>
   * [eclipse-ee4j/jakartaee-tutorial-examples](https://github.com/eclipse-ee4j/jakartaee-tutorial-examples) -- migrated from [javaee/tutorial-examples](https://github.com/javaee/tutorial-examples) - Java EE tutorial examples<br>
   * [payara/Payara-Examples](https://github.com/payara/Payara-Examples) - JakartaEE 在 Payara Web 服务器 上的部署于应用 <br>
   * [Example Health JEE Application on Openshift](https://github.com/IBM/example-health-jee-openshift) - IBM/example-health-jee-openshift : IBM 的 Open Liberty 上的部署与应用<br>
      + [使用 Java EE、Open Liberty 和 Node.js 在一个虚构的医疗保健应用中部署基于 Kubernetes 的微服务](https://developer.ibm.com/cn/patterns/jee-app-modernization-with-openshift/)<br>
         - >本 Code Pattern 展示了如何通过将 Java EE 应用程序转换为基于 Kubernetes 的微服务来实现应用程序现代化。它演示了为一个虚构的医疗保健公司的面向患者的应用程序创建容器镜像，并将其部署到 Red Hat OpenShift on IBM Cloud™ 集群上的步骤。
         - >
         - >此示例代码是一系列 Code Pattern 的一部分，这些 Code Pattern 专注于虚构的医疗保健公司，并使用 Red Hat OpenShift on IBM Cloud™ 企业版 Kubernetes 环境演示应用程序现代化。您将学习如何使用来自 Java EE 应用程序的 REST API 在 MySQL 数据库上填充和访问大量数据。此外，您还可以通过部署 Node.js 和 PHP Web 应用程序来使用 OpenShift 的 Source-to-Image 工具包，这些应用程序从 Java EE 应用程序对 API 进行 RESTful 调用，并显示来自 MySQL 数据库的数据。
   * []()<br>
   * []()<br>
   * []()<br>
   * []()<br>
   * []()<br>
   * [bmuschko/whats-new-in-java-12](https://github.com/bmuschko/whats-new-in-java-12)<br>
   * [IanDarwin/javasrc](https://github.com/IanDarwin/javasrc) - Java 的很多知识混合，参考学习。。。<br>
   * [SmartDeviceLink (SDL)](https://github.com/smartdevicelink/sdl_java_suite)<br>
      + >SmartDeviceLink (SDL) is a standard set of protocols and messages that connect applications on a smartphone to a vehicle head unit. This messaging enables a consumer to interact with their application using common in-vehicle interfaces such as a touch screen display, embedded voice recognition, steering wheel controls and various vehicle knobs and buttons. There are three main components that make up the SDL ecosystem.

## Advance Examples - 值得推荐，开源项目
   * [phillip-kruger/jello](https://github.com/phillip-kruger/jello)<br>
      - >This is an example application to demonstrate some of the APIs available under the Jakarta EE Umbrella.
      - High Level Overview
      - ![High Level Overview](https://raw.githubusercontent.com/phillip-kruger/jello/master/high_level.png)<br>
   * [eclipse-ee4j/jakartaee-tck](https://github.com/eclipse-ee4j/jakartaee-tck)<br>
   * [wesleyegberto/javaee8-jsf-chat](https://github.com/wesleyegberto/javaee8-jsf-chat) - 学习WebSocket的时候，可以参考，这个项目是2019年9月份更新为Jakarta EE 8<br>
   * [imixs/imixs-workflow](https://github.com/imixs/imixs-workflow) - 这个Workflow，效果蛮符合要求<br>
      - >Imixs-Workflow is an open source workflow engine to build human-centric workflow applications on a flexible and robust framework. Using the Business Process Modelling Notation - BPMN 2.0, business logic can be modeled fast, easy and in a flexible way. Imixs-Workflow is based on the Jarkarta EE and the Eclipse Microprofile standards and fits into any modern microservice architecture thanks to its openness. Imixs-Workflow runs on all modern application servers like Wildfly, Payara, Open Liberty or Apache TomEE.
      - Imixs-BPMN
      - ![Imixs-BPMN](https://github.com/imixs/imixs-workflow/raw/master/screen_001.png)<br>
   * [eclipse-ee4j/jpa-api](https://github.com/eclipse-ee4j/jpa-api) - Jakarta Persistence project<br>
      - >Jakarta Persistence defines a standard for management of persistence and object/relational mapping in Java(R) environments.

   * [wildfly-archetypes/wildfly-jakartaee-ear-archetype/](https://github.com/wildfly/wildfly-archetypes/tree/master/wildfly-jakartaee-ear-archetype)<br>
      + Introduction
         - >This archetype creates a blank EAR project with EJB and Web module. It is prepared for running Arquillian unit tests. More details can be found in the file "src/main/resources/archetype-resources/README.txt", which is end-user doc and added to the resulting project.
   * [jrbalsas/dawClubJSF](https://github.com/jrbalsas/dawClubJSF)<br>
      + >Sample Maven Netbeans project with JSF CRUD Web App
   * [thjanssen/HibernateTips](https://github.com/thjanssen/HibernateTips)<br>
   * [jakartaee/jakarta.ee](https://github.com/jakartaee/jakarta.ee)<br>
   * [lenve/JavaEETest](https://github.com/lenve/JavaEETest) - 很多SpringBoot项目，可以参考参考<br>

## JavaEE Examples - 8 version   
   * [javaee-samples/javaee8-samples](https://github.com/javaee-samples/javaee8-samples)<br>
   * [lpelczar/JavaEE-hibernate-web-app](https://github.com/lpelczar/JavaEE-hibernate-web-app)<br>
   * [javamelody/javamelody](https://github.com/javamelody/javamelody) - JavaMelody<br>
      + >The goal of JavaMelody is to monitor Java or Java EE applications in QA and production environments.
   * [c0de8ug/javaee-tutorial](https://github.com/c0de8ug/javaee-tutorial)<br>
      + >这是个简单的教务系统网站,并且结合了图书订购功能,希望这个小DEMO能对大家学习有帮助
## Examples - Old 7 version   
   * [Azure-Samples/Java-application-petstore-ee7](https://github.com/Azure-Samples/Java-application-petstore-ee7) - 非优先。。。<br>
   * [dockersamples/javaee-demo](https://github.com/dockersamples/javaee-demo) - Docker 的例子<br>
      + >This example demonstrates the path to modernizing a Java EE application to a containerized infrastructure. We'll migrate the Java EE 7 Hands-on Lab to Docker. Furthermore, we'll update the presentation layer written in Java Server Faces to a React application.
   * [Java EE 7 Example for JMS and WebSockets integration](https://github.com/brunoborges/javaee7-jms-websocket-example)<br>
      + >This application demonstrates a full-duplex scenario using WebSockets and JMS, with a fully functional server-side asynchronous push, using CDI events and EJB.
        >
        >Details and step-by-step were blogged [here]: https://blogs.oracle.com/brunoborges/entry/integrating_websockets_and_jms_with
   * WebSocket Java EE 7 - AngularJS - WildFly 10 Docker: [mgreau/javaee7-websocket](https://github.com/mgreau/javaee7-websocket)<br>
      + ![Multiple matches in live (US OPEN)](https://github.com/mgreau/javaee7-websocket/raw/master/doc/img/websocket_wildfly_angularjs_tennis.png)<br>
      + >Install on your local WildFly 10 Application Server
   * [javaee-samples/javaee7-docker-maven](https://github.com/javaee-samples/javaee7-docker-maven) - Run Java EE 7 Application as Docker Container using Maven<br>
      + >This sample application shows how to package a Java EE 7 application as Docker image and run it within a container using docker-maven-plugin.
         - 
   * [algaworks/curso-javaee-primefaces](https://github.com/algaworks/curso-javaee-primefaces)<br>
      + 
## Awesome JavaEE projects
   * [ScarlettRay/JavaEE-projects](https://github.com/ScarlettRay/JavaEE-projects)<br>
      + >这个仓库收藏了一些自己在学习和工作过程中接触到的Javaee项目，为后人的项目开发提供一些思路或者解决方案吧。也希望各位看官可以将你们觉得不错的项目提交上来，格式不限，网站链接、网盘、源码都可以，PR,issues,或者直接联系我。
   * [howsun/howsun-javaee-framework](https://github.com/howsun/howsun-javaee-framework)<br>
      + >这是一款特别适用于中小企业应用的JavaEE快速开发框架。它是居于Spring容器之上，封装了DAO（含Hibernate和MongoDB）操作、多模块统一管理、统一配置管理、统一日志管理等优雅的工程管理开发模型，并提供大量工具包、Json操作、分页辅助工具。
   * [czwbig/Tmall_JavaEE](https://github.com/czwbig/Tmall_JavaEE)<br>
      + >技术栈 Servlet + Jsp + Tomcat , 是Java Web入门非常好的练手项目
        >
        >本项目为Java EE入门练手项目，没有使用 SSH , SSM 框架，而是使用 JavaEE 整套技术来作为解决方案，实现模仿天猫网站的各种业务场景。 之所以不使用框架，就是为了借助这个项目夯实 JavaEE 基础，并且在项目中借助反射等技术。--> [模仿天猫前台](http://how2j.cn/tmall?p=55563)<br>
   * [AdamBien/javaee8-essentials-archetype](https://github.com/AdamBien/javaee8-essentials-archetype)<br>
      + >Minimalistic Java EE 8 / Jakarta EE + MicroProfile Quickstarter
      + >A quickstart maven archetype for creating greenfield Java EE 8 / Jakarta EE project with MicroProfile 2+ APIs.
        >
        >Fire up your CLI and type: mvn archetype:generate -Dfilter=com.airhacks:javaee8-essentials-archetype to create a fully fledged Java EE 8 "kB" project. Use the most recent version.
   * [arun-gupta/microservices](https://github.com/arun-gupta/microservices) - 微服务 模式<br>
      + >Refactor monolith to microservices
   * [JaceyRx/Examination_System](https://github.com/JaceyRx/Examination_System) 这个项目是一个简单的教务查询系统，该练手小项目希望能帮助到大家，熟悉SSM的整合开发<br>
      + >这个项目是一个简单的教务查询系统，该练手小项目希望能帮助到大家，熟悉SSM的整合开发
   * [Vino007/javaEEScaffold](https://github.com/Vino007/javaEEScaffold)<br>
      + >JavaEEScaffold-----java web 脚手架搭建(用户角色权限管理系统) ##项目地址 JavaEEScaffold 用户名：admin 密码：1111 数据库文件：javaEEScaffold.sql ##项目介绍
   * [GVP若依 / RuoYi](https://gitee.com/y_project/RuoYi)<br>
      + >基于SpringBoot的权限管理系统 易读易懂、界面简洁美观。 核心技术采用Spring、MyBatis、Shiro没有任何其它重度依赖。直接运行即可用
http://www.ruoyi.vip
      
   * [WebGoat/WebGoat-Legacy](https://github.com/WebGoat/WebGoat-Legacy)<br>
      + >This program is a demonstration of common server-side application flaws. The exercises are intended to be used by people to learn about application penetration testing techniques.
## githuber 相关
   * [Thorben Janssen](https://github.com/thjanssen) - 关于Jakarta EE 的 数据层（Persistence 和 Hibernate）例子<br>
   * [RuoYi: 使用若依快速构建web应用程序](http://doc.ruoyi.vip/)<br>
   
