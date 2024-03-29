# 官网的资源
  * Jakarta EE Tutorial
    - <details open>
          <summary>
              说明
          </summary>
          The <a href="https://eclipse-ee4j.github.io/jakartaee-tutorial">Jakarta EE Tutorial</a> is a comprehensive reference for developing applications with Jakarta EE.
      </details>
  * First Cup
    - <details open>
          <summary>
              说明
          </summary>
          The <a href="https://eclipse-ee4j.github.io/jakartaee-firstcup/">First Cup</a> is part of the Tutorial and is a gentle hands-on introduction to Jakarta EE.
      </details>
  * First Cup Examples
    - <details open>
          <summary>
              说明
          </summary>
          You can further explore the <a href="https://github.com/eclipse-ee4j/jakartaee-firstcup-examples">First Cup Examples</a> to get a feel for how Jakarta EE applications look like.
      </details>
  * Jakarta EE Tutorial Examples
    - <details open>
          <summary>
              说明
          </summary>
          The <a href="https://github.com/eclipse-ee4j/jakartaee-tutorial-examples">Jakarta EE Tutorial Examples</a> is a very comprehensive resource showing you how to use many Jakarta EE APIs and features.
      </details>
  * Cargo Tracker
    - <details open>
          <summary>
              说明
          </summary>
          The <a href="https://eclipse-ee4j.github.io/cargotracker/">Cargo Tracker</a> project demonstrates first-hand how you can develop applications with Jakarta EE using widely adopted architectural best practices like Domain-Driven Design (DDD).
      </details>
## Wildfly 的 官网例子。。。 列表
   * Downloading the quickstarts -- [Downloading the quickstarts -> JBoss Developer Framework](https://github.com/wildfly/quickstart)
   * 【这个例子，太久远了，可不用看？】Getting Started Developing Applications Guide --》[Getting Started Developing Applications Guide](https://docs.wildfly.org/26/Getting_Started_Developing_Applications_Guide.html) --》[Kitchensink Quickstart](https://github.com/wildfly/quickstart/blob/10.x/guide/KitchensinkQuickstart.asciidoc)
     + 源码：[CDI + JSF + EJB + JTA + Bean Validation + JAX-RS + Arquillian: Kitchensink quickstart](https://github.com/wildfly/quickstart/blob/10.x/guide/KitchensinkQuickstart.asciidoc)
  * Bootable JAR Guide --》需要知道的方法，方便开发。--〉[Bootable JAR Guide](https://docs.wildfly.org/26/Bootable_Guide.html)
    - https://github.com/wildfly-extras/wildfly-jar-maven-plugin

# Sample for Tutorial
## 按顺序学习的教程与配套的例子
  * [Kickstart a Jakarta EE 10 Application](https://hantsy.medium.com/kickstart-a-jakarta-ee-10-application-d579577af634)
  * [Jakarta EE 9 Hello World example application](http://www.mastertheboss.com/java-ee/jakarta-ee/jakarta-ee-9-hello-world-example-application/)
    - <details open>
          <summary>
              说明
          </summary>
          Hello World 的 例子<br />
          配套的例子： 👉 <a href="https://github.com/fmarchioni/mastertheboss/tree/master/jakartaee/jakartaee-9">mastertheboss/jakartaee/jakartaee-9/</a>
  * [Getting started with Jakarta EE](http://www.mastertheboss.com/java-ee/jakarta-ee/getting-started-with-jakarta-ee/)
    - <details open>
          <summary>
              说明
          </summary>
          基本的实现<br />
          配套的例子： 👉 <a href="https://github.com/fmarchioni/mastertheboss/tree/master/jakartaee">mastertheboss/jakartaee/</a>
      </details>
  * [Getting started with Jakarta RESTful Services](http://www.mastertheboss.com/jboss-frameworks/resteasy/getting-started-with-jakarta-restful-services/)
    - <details open>
          <summary>
              说明
          </summary>
          实现 Jakarta RESTful Services<br />
          例子： 👉 <a href="https://github.com/fmarchioni/mastertheboss/tree/master/jakartaee">mastertheboss/jakartaee/</a>
      </details>
## 官网的例子 - 暂时 放这
   * [Examples for Jakarta EE](https://projects.eclipse.org/projects/ee4j.jakartaee-examples/developer)<br>
      + [eclipse-ee4j/jakartaee-examples](https://github.com/eclipse-ee4j/jakartaee-examples) - 是上面一个新的Github源位置<br>
   * [eclipse-ee4j/jakartaee-tutorial-examples](https://github.com/eclipse-ee4j/jakartaee-tutorial-examples) -- migrated from [javaee/tutorial-examples](https://github.com/javaee/tutorial-examples) - Java EE tutorial examples<br>
## Examples - Google Search: github java ee projects opensource example site:github.com | jakarta ee example | github jakarta ee projects opensource example site:github.com
   * [Jakarta EE Examples](https://projects.eclipse.org/proposals/jakarta-ee-examples) - 这个是官网的Examples 的即介绍，认真先看。优先看。。。<br>
   * [daggerok/java-ee-examples](https://github.com/daggerok/java-ee-examples) - 用到了Kotlin语言，参考看看<br>
   * [manorrock/jakartaee-examples](https://github.com/manorrock/jakartaee-examples) - 非常经典，已贡献给Eclipse Foundation<br>
      + >This repository has been donated to the Eclipse Foundation, click [here](https://github.com/eclipse-ee4j/jakartaee-examples) ->  [eclipse-ee4j/jakartaee-examples] to go to its new home.
        ```
           This repository has been deprecated and will be removed August 1st, 2020.
        ```
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
   * 有些值得参考 - [daggerok/java-ee-examples](https://github.com/daggerok/java-ee-examples)<br>
      + 一些教程
         - [JavaEE examples java-ee-examples (0.0.1)](https://daggerok.github.io/java-ee-examples/)<br>
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

## WildFly Examples
   * 参考
      + WildFly Maven Plugin - [Adding Resources Examples](https://docs.jboss.org/wildfly/plugins/maven/latest/examples/add-resource-example.html)<br>
