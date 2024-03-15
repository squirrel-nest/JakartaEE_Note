# ✨ Jakarta EE Project

<details open>
    <summary>
        <i><b>✨ Jakarta EE 的 开发</b></i>
    </summary>
    <ul type="disc">
        <li>
            <details open>
                <summary>
                    <i><b>✨ 项目 的 脉络</b></i>
                </summary>
                <ul type="disc">
                    <li>
                        -
                    </li>
                </ul>
            </details>
        </li>
        <li>
            <details open>
                <summary>
                    <i><b>✨ 项目文件夹 路径</b></i>
                </summary>
                <ul type="disc">
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ GitHub Repository - <a href="https://github.com/squirrel-nest/JakartaEE_Code">squirrel-nest/JakartaEE_Code</a></b></i>
                            </summary>
                            <ul type="disc">
                                <li>
                                    <a href="https://github.com/squirrel-nest/JakartaEE_Code/tree/master/lzdata-ee-9-gdev">squirrel-nest/JakartaEE_Code/lzdata-ee-9-gdev/</a>
                                </li>
                            </ul>
                        </details>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 本地目录 - MacOS System</b></i>
                            </summary>
                            <ul type="disc">
                                <li>
                                    /Users/Codes/JakartaEEProjects/01_LearningCode/lzdata-ee-9-gdev
                                </li>
                            </ul>
                        </details>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 本地目录 - Windows System</b></i>
                            </summary>
                            <ul type="disc">
                                <li>
                                    E:\JavaEEDev\JavaEELearningCode\lzdata-ee-9-gdev
                                </li>
                            </ul>
                        </details>
                    </li>
                </ul>
            </details>
        </li>
        <li>
            <details open>
                <summary>
                    <i><b>✨ 版本 管理 与 更新</b></i>
                </summary>
                <ul type="disc">
                    <li>方法 - 沿革</li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ Gradle 模式</b></i>
                            </summary>
                            <ol type="disc">
                                <li>
                                    <details open>
                                        <summary>
                                            <i><b>✨ 文件 的 结构 - versions_variable.gradle 文件 管理阶段</b></i>
                                        </summary>
                                        <ul type="disc">
                                            <li>
                                                <details open>
                                                    <summary>
                                                        <i><b>✨ lzdata-ee9-servletweb</b></i>
                                                    </summary>
                                                    <ul type="disc">
                                                        <li>build.gradle
                                                            <pre><code>apply from: '../core_dependencies_servlet_web_9.gradle'
apply from: '../test_dependencies_common.gradle'</code></pre>
                                                        </li>
                                                        <li>--> core_dependencies_servlet_web_9.gradle
                                                            <pre><code>dependencies {
<br>
    // implementation project(path: ':lzdata-ee-utils')
    implementation project(path: ':lzdata-ee9-servlet-base')
    ...
    implementation deps.mysql.mysql_connector_java
<br>
}</code></pre>
                                                        </li>
                                                        <li>
                                                            ==> <a href="#lzdata-ee9-servlet-base">lzdata-ee9-servlet-base</a>
                                                        </li>
                                                    </ul>
                                                </details>
                                            </li>
                                            <li>
                                                <details open>
                                                    <summary>
                                                        <i><b>✨ lzdata-ee9-servlet-base</b></i>
                                                    </summary>
                                                    <a id="lzdata-ee9-servlet-base"></a>
                                                    <ul type="disc">
                                                        <li>build.gradle
                                                            <pre><code>apply from: '../core_dependencies_servlet_base_9.gradle'
apply from: '../test_dependencies_common.gradle'</code></pre>
                                                        </li>
                                                        <li>--> core_dependencies_servlet_base_9.gradle
                                                            <pre><code>dependencies {
<br>
    implementation project(path: ':lzdata-ee9-jaxws-base')
    implementation project(path: ':lzdata-ee9-jpa-model')
...
    implementation deps.jakarta.platform.jakartaee_api_9
...
    implementation deps.org_glassfish.jakarta_el
...
    implementation deps.mysql.mysql_connector_java</code></pre>
                                                        </li>
                                                        <li>
                                                            ==> <a href="#lzdata-ee9-jaxws-base">lzdata-ee9-jaxws-base</a> 👈 是 Project<br>
                                                            ==> <a href="#lzdata-ee9-jpa-model">lzdata-ee9-jpa-model</a> 👈 是 Project
                                                        </li>
                                                    </ul>
                                                </details>
                                            </li>
                                            <li>
                                                <details open>
                                                    <summary>
                                                        <i><b>✨ lzdata-ee9-jaxws-base</b></i>
                                                    </summary>
                                                    <a id="lzdata-ee9-jaxws-base"></a>
                                                    <ul type="disc">
                                                        <li>build.gradle
                                                            <pre><code>apply from: '../core_dependencies_jaxws_base_9.gradle'
apply from: '../test_dependencies_common.gradle'
apply from: '../test_dependencies_jaxws_base_9.gradle'</code></pre>
                                                        </li>
                                                        <li>--> core_dependencies_jaxws_base_9.gradle
                                                            <pre><code>dependencies {
<br>
    implementation project(path: ':lzdata-ee9-jpa-model')
...
    implementation deps.jakarta.platform.jakartaee_api_9
    implementation deps.com_sun.xml.ws.jaxws_rt
    implementation deps.com_sun.xml.ws.jaxws_ri
<br>
    implementation deps.org_glassfish.jakarta_el
...
...
    implementation deps.mysql.mysql_connector_java
<br>
    implementation deps.commons_io.commons_io
<br>
    testImplementation deps.jboss.resteasy.client
    // implementation 'org.jboss.resteasy:resteasy-multipart-provider:4.5.8.Final'
    compileOnly deps.jboss.resteasy.multipart_provider
    compileOnly deps.jboss.resteasy.jaxrs
}</code></pre>
                                                        </li>
                                                    </ul>
                                                </details>
                                            </li>
                                        </ul>
                                    </details>
                                </li>
                            </ol>
                        </details>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ Maven 模式</b></i>
                            </summary>
                            <ul type="disc">
                                <li>
                                    -
                                </li>
                            </ul>
                        </details>
                    </li>
                </ul>
            </details>
        </li>
    </ul>
</details>

----


## 项目说明
   * 框架搭建 以 Jakarta EE 9 作为开发的主线, javax 包名 已经全部更改为 jakarta, 共用的模块用 _share_ 或 _common_ 
   * 总项目文件夹：E:\JavaEEDev\JavaEELearningCode\lzdata-ee-9-gdev
   * Jakarta EE 8 为旧的版本, 可以废弃了
## lzdata-ee-9-gdev 项目
### 项目路径
  * 数据库 - 相关设计模型文件等
  * 代码
## 项目 的 编译
  * 编译方法
    + 参见 --> [](url)
    + 终端命令的方法 - 优先选择
    + 开发工具直接编译
  * 编译后 war文件目录
     + Gradle
        - war文件目录：在每个Module目录下的 build/libs 目录 中
     + Maven
        - war文件目录：每个Module目录下的 target 目录 中

## 项目的 部署
### 启动顺序
  * 数据库
    + <details open>
         <summary>
             MySQL
         </summary>
         <ul type="square">
             <li>MySQL 安装 与 设置 入口【目前】：<a href="https://github.com/squirrel-nest/MacOS_Note/blob/master/MacOS_Install%26Setting_Database.md#mysql">squirrel-nest/MacOS_Note/MacOS_Install&Setting_Database.md</a>
             </li>
         </ul>
         <ul type="square">
             <li>MySQL Server Home 位置: 
                 <ul type="disc">
                   <li>MacOS
                       <ul type="circle">
                           <li>/usr/local/mysql</li>
                       </ul>
                   </li>
                   <li>Windows
                       <ul type="circle">
                           <li>E:\Softwares\MySQL\mysql-8.0.29</li>
                       </ul>
                   </li>
                 </ul>
             </li>
             <li>MySQL 启动 命令
                 <ul type="disc">
                   <li>启动 - 方法 1
                       <ul type="circle">
                           <li>cd /usr/local/mysql && bin/mysqld_safe --user=mysql &</li>
                       </ul>
                   </li>
                   <li>登陆 账号 & 密码
                       <ul type="circle">
                           <li>r**t</li>
                           <li>r**t**3</li>
                       </ul>
                   </li>
                 </ul>
             </li>
             <li>MySQL 停止 命令
                 <ul type="disc">
                   <li>停止 - 方法 1
                       <ul type="circle">
                           <li>cd /usr/local/mysql && bin/mysqladmin -u root -p shutdown &</li>
                       </ul>
                   </li>
                 </ul>
             </li>
         </ul>
      </details>

  * WebServer
    + <details open>
         <summary>
             Wildfly
         </summary>
         <ul type="square">
             <li>Wildfly 安装 与 设置 入口【目前】：<a href="https://github.com/squirrel-nest/MacOS_Note/blob/master/MacOS_Install&Setting_WebServer.md">squirrel-nest/MacOS_Note/MacOS_Install&Setting_WebServer.md</a>
             </li>
         </ul>
         <ul type="square">
             <li>Wildfly Home 位置: 
                 <ul type="disc">
                   <li>MacOS
                       <ul type="circle">
                           <li>原始路径：/Users/Softwares/Wildfly/wildfly-preview-26.1.1.Final</li>
                           <li>备注：是否要建立一个软连接到 /usr/local/wildfly</li>
                           <li>Symbolic link 命令：cd /usr/local && ln -s /Users/Softwares/Wildfly/wildfly-preview-26.1.1.Final /usr/local/wildfly</li>
                       </ul>
                   </li>
                   <li>Windows
                       <ul type="circle">
                           <li>E:\Softwares\Wildfly\wildfly-preview-26.1.1.Final</li>
                       </ul>
                   </li>
                 </ul>
             </li>
             <li>WildFly 启动 命令
                 <ul type="disc">
                   <li>启动 - 方法 1<br />
                       备注：命令后面 & 符号 可选
                       <ul type="circle">
                           <li>cd /Users/Softwares/Wildfly/wildfly-preview-26.1.1.Final && bin/standalone.sh &</li>
                       </ul>
                   </li>
                 </ul>
             </li>
             <li>MySQL 停止 命令
                 <ul type="disc">
                   <li>停止 - 方法 1
                       <ul type="circle">
                           <li>Control + C 即可</li>
                       </ul>
                   </li>
                 </ul>
             </li>
         </ul>
      </details>

### 部署的方式
  * Wildfly
    + <details open>
         <summary>
             Wildfly 部署的方式
         </summary>
         <ul type="square">
             <li>内容后续补充：参见 <a href="https://github.com/squirrel-nest/MacOS_Note/blob/master/MacOS_Install&Setting_WebServer.md">squirrel-nest/MacOS_Note/MacOS_Install&Setting_WebServer.md</a>  中的相关内容
             </li>
         </ul>
      </details>
### 部署的 Web Service 列表
  * 参见 <a href="https://github.com/squirrel-nest/JakartaEE_Note/blob/master/WebServiceList.md">Web Service 列表</a>


## Web Services 例子 --> 参考 Tutorial 中的 例子 和 教程 Part VI: Web Services
### Jakarta XML Web Services Sample - "Big" Web Services
  * Introduction
    + <details open>
         <summary>
             Jakarta XML Web Services 的 一些 介绍
         </summary>
         <ul type="square">
             <li>Big web services use XML messages that follow the Simple Object Access Protocol (SOAP) standard, an XML language defining a message architecture and message formats.</li>
             <li>Jakarta XML Web Services formerly call Java API for XML Web Services (JAX-WS)</li>
             <li>Jakarta XML Web Services is now included in the Jakarta EE platform as an optional technology under the jakarta namespace.</li>
         </ul>
      </details>
  * Jakarta XML Web Services Sample 模块 的 架构 以及 模块间的关系
    + <details open>
         <summary>
             说明
         </summary>
         <ul type="square">
             <li>
                 mermaid
             </li>
         </ul>
      </details>
    + 说明
      1. 模块的架构
         - lzdata-ee9-jaxwsweb【前端】 --> lzdata-ee9-jaxws-base【中间层】 --> lzdata-ee9-jpa-model【数据接入层模块】，lzdata-ee9-jpa-model 属于共用模块 其他模块 也可以 调用。。。lzdata-ee9-jpa-model模块参见 数据接入层中，Jakarta Pesistence 模块 的说明。。。
         - 无法使用分模块的功能，合并到 lzdata-ee9-fusionweb 模块中。。。见 lzdata-ee9-fusionweb 模块的例子说明
      + 例子
         - JAX-WS 的简单例子 - Jakarta EE tutorial
           * Hello Service Eaxmple
             + WSDL
               - http://localhost:8088/lzjaxwsweb9/Hello?wsdl
             + SOAP 说明
               - rpc style
               - soap 1.2
             + 后端架构 - Package：com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap12.hello
               - Interface class:
                  * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap12.hello.HelloInf
               - Implementation class:
                  * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap12.hello.Hello
               -  javax.xml.ws.Endpoint:
                  * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap12.hello.HelloPublisher
               - **WebServiceClient** (不是 WebService) class:
                  * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap12.hello.HelloService
             + 逻辑层实现 - Servlet
               - Servlet
                 * com.lzsoft.lzdata.weblogic.servlet.tutorial.helloservice.HelloServlet
               - Service
                 * 保留
             + 前端实现 - Front End - 界面
               - Web 实现
                 * 方法1：html界面
                   + [http://localhost:8088/lzjaxwsweb9/jaxws-hello-service.html](http://localhost:8088/lzjaxwsweb9/jaxws-hello-service.html) --><br>
                     - --> [http://localhost:8088/lzjaxwsweb9/HelloServlet](http://localhost:8088/lzjaxwsweb9/HelloServlet)<br>
               - Client 实现
           * HelloWorld Service Eaxmple - Soap 1.2 Including RPC Style & Doc Style
             + Web Page
               - --> [http://localhost:8088/lzjaxwsweb9/HelloWorldServlet - Include Rpc and Doc](http://localhost:8088/lzjaxwsweb9/HelloWorldServlet)<br>
             + WSDL
               - rpc style
                 * http://localhost:8088/lzjaxwsweb9/HelloWorldRpcService?wsdl
               - doc style
                 * http://localhost:8088/lzjaxwsweb9/HelloWorldDocService?wsdl
               + SOAP 说明
                 - soap 1.2
               + 后端架构
                  - Rpc Style
                    - Package
                      * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap.rpcstyle
                    - Interface class:
                      * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap.rpcstyle.HelloWorldRpc
                    - Implementation class:
                      * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap.rpcstyle.HelloWorldRpcImpl
                    -  javax.xml.ws.Endpoint:
                       * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap.rpcstyle.HelloWorldRpcPublisher
                    - **WebServiceClient** (不是 WebService) class:
                       * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap.rpcstyle.HelloWorldRpcImplService

                  - Doc Style
                    - Package
                       * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap.docstyle
                    - Interface class:
                       * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap.docstyle.HelloWorldDoc
                    - Implementation class:
                       * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap.docstyle.HelloWorldDocImpl
                    -  javax.xml.ws.Endpoint:
                       * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap.docstyle.HelloWorldDocPublisher
                    - **WebServiceClient** (不是 WebService) class:
                       * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap.docstyle.HelloWorldDocImplService
               + 逻辑层实现 - Servlet
                  - Servlet
                     * com.lzsoft.lzdata.weblogic.servlet.tutorial.helloservice.MainHelloWorldServlet
                  - Service
                     * 
               + 前端实现 - Front End - 界面
                  - Web 实现
                     * 方法1：html界面
                        + 待完成 - [http://localhost:8088/lzjaxwsweb9/jaxws-hello-service.html](http://localhost:8088/lzjaxwsweb9/jaxws-hello-service.html) --><br>
                           - --> [http://localhost:8088/lzjaxwsweb9/HelloWorldServlet - Include Rpc and Doc](http://localhost:8088/lzjaxwsweb9/HelloWorldServlet)<br>
                  - Client 实现
                     * com.lzsoft.lzdata.javaeeclient.jaxwstest.tutorial.helloservice.soap.HelloWorldClient
                        + 说明
                           - javax.xml.ws.Service; 需要更改为：jakarta.xml.ws.Service;，否则会报错。。。

            * HelloWorldServletTest Service Eaxmple - **与上同，可以不用看。。。**
               + Web Page
                  - --> [http://localhost:8088/lzjaxwsweb9/MServletTest](http://localhost:8088/lzjaxwsweb9/MServletTest)<br>

               + 逻辑层实现 - Servlet
                  - Servlet
                     * com.lzsoft.lzdata.weblogic.servlet.tutorial.helloservice.HelloWorldServletTest


            * AddNumbers Service Eaxmple - Soap 1.2 Doc Style
               + Web Page
                  - --> []()<br>
               + WSDL -- 两种方式：1. Web Server。 2. Endpoint: AddNumbersPublisher
                  - document style - default: 默认为document style
                     * http://localhost:8088/lzjaxwsweb9/AddNumbersImpl?wsdl
               + SOAP 说明
                  - soap 1.2
               + 后端架构
                 - Package
                    * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap12.addnumbers
                 - Interface class:
                    * 无，后续补加  --> com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap12.addnumbers.AddNumbers 已补。2021-01-16
                 - Implementation class:
                    * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap12.addnumbers.AddNumbersImpl
                 -  javax.xml.ws.Endpoint:
                    * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap12.addnumbers.AddNumbersPublisher
                 - **WebServiceClient** (不是 WebService) class:
                    * com.lzsoft.lzdata.webservice.jaxws.tutorial.helloservice.soap12.addnumbers.AddNumbersImplService
               + 逻辑层实现 - Servlet
                  - Servlet
                     * 无
                  - Service
                     * 
               + 前端实现 - Front End - 界面
                  - Web 实现
                     * 方法1：html界面
                        + 待完成 - []() --><br>
                           - --> []()<br>
                  - Client 实现
                     * com.lzsoft.lzdata.javaeeclient.jaxwstest.tutorial.helloservice.soap12.addnumbers.AddNumbersClient
                        + 报错，待查
                     * com.lzsoft.lzdata.javaeeclient.jaxwstest.tutorial.helloservice.soap12.addnumbers.AddNumbersRefFromHelloWorld
                        + 借鉴 HelloWorldClient，通过，但其中的 AddNumbersException 报错，未解决


            * CalculatorMy Service Eaxmple - Soap 1.2 Doc Style
               + Reference
                  - --->
               + Web Page
                  - --> [http://localhost:8088/lzjaxwsweb9/HelloWorldServlet - Include Rpc and Doc](http://localhost:8088/lzjaxwsweb9/HelloWorldServlet)<br>
               + WSDL
                  - document style - default: 默认为document style
                     * http://localhost:8088/lzjaxwsweb9/CalculatorMyImpl?wsdl
               + SOAP 说明
                  - soap 1.2
               + 后端架构
                 - Package
                    * org.me.calculator
                 - Interface class:
                    * org.me.calculator.CalculatorMy
                 - Implementation class: -- @WebService
                    * org.me.calculator.CalculatorMyImpl
                    * org.me.calculator.ServerInfo -- Not a Implementation class
                 -  javax.xml.ws.Endpoint:
                    * 无
                 - **WebServiceClient** (不是 WebService) class:
                    * org.me.calculator.CalculatorMyImplService
               + 逻辑层实现 - Servlet
                  - Servlet
                     * 无 -- 后续实现。 -- 目前实现方式是采用 JSP 页面中直接嵌入 Java 逻辑代码。。。
                  - Service
                     * 
               + 前端实现 - Front End - 界面
                  - Web 实现
                     * 方法1：html界面
                        + [http://localhost:8088/lzjaxwsweb9/calculator-my.jsp](http://localhost:8088/lzjaxwsweb9/calculator-my.jsp) --><br>
                           - --> []()<br>
                        + Path：
                           - lzdata-ee-9-gdev/lzdata-ee8-jaxwsweb/src/main/webapp/calculator-my.jsp
                           - lzdata-ee-9-gdev/lzdata-ee8-jaxwsweb/src/main/webapp/calculator-my-response.jsp
                        
                  - Client 实现



            * Task Service Eaxmple - Soap 1.2 RPC Style
               + WSDL
                  - rpc style
                     * http://localhost:8088/lzjaxwsweb9/TaskServiceImpl?wsdl 注：这个是部署到Wildfly上的。。。，Local看clinet中的说明
               + SOAP 说明
                  - soap 1.2
               + 后端架构
                  - Rpc Style
                    - Package
                       * com.lzsoft.lzdata.webservice.jaxws.taskservice
                    - Interface class:
                       * com.lzsoft.lzdata.webservice.jaxws.taskservice.TaskService
                    - Implementation class:
                       * com.lzsoft.lzdata.webservice.jaxws.taskservice.TaskServiceImpl
                    -  javax.xml.ws.Endpoint:
                       * com.lzsoft.lzdata.webservice.jaxws.taskservice.TodolistApplicationSOAPPublisher
                    - **WebServiceClient** (不是 WebService) class:
                       * 未完成
               + 逻辑层实现 - Servlet
                  - Servlet
                     * 暂无
                  - Service
                     * 
               + 前端实现 - Front End - 界面
                  - Web 实现
                     * 方法1：html界面
                        + 待完成 -  --><br>
                           - --> <br>
                  - Client 实现
                     * Package
                        + com.lzsoft.lzdata.webservice.jaxws.taskservice.TodolistApplicationSOAPPublisherClient
                     * 方法
                        + 本机模式
                           1. 执行: com.lzsoft.lzdata.webservice.jaxws.taskservice.TodolistApplicationSOAPPublisher
                           2. 再执行：com.lzsoft.lzdata.webservice.jaxws.taskservice.TodolistApplicationSOAPPublisherClient
                           3.查看结果。。。
                        + 服务器模式
                           1. 上传war文件到服务器端
                           2. 将 QName设置指向服务器端
                           3. 再执行：com.lzsoft.lzdata.webservice.jaxws.taskservice.TodolistApplicationSOAPPublisherClient




            * EmployeeService Service Eaxmple - Soap 1.2 RPC Style
            * LoginService Service Eaxmple - Soap 1.2 RPC Style
            * OrderService Service Eaxmple - Soap 1.2 RPC Style
               + Reference
                  - --->
               + Web Page
                  - --> []()<br>
               + WSDL
                  - rpc style - default: 默认为document style
                     * http://localhost:8088/lzjaxwsweb9/EmployeeServiceImpl?wsdl
                     * http://localhost:8088/lzjaxwsweb9/LoginServiceImpl?wsdl
                     * http://localhost:8088/lzjaxwsweb9/OrderServiceImpl?wsdl
               + SOAP 说明
                  - soap 1.2
               + 后端架构
                 - Package
                    * com.memorynotfound.ws
                 - Interface class:
                    * com.memorynotfound.ws.EmployeeService
                    * com.memorynotfound.ws.LoginService
                    * com.memorynotfound.ws.OrderService
                 - Implementation class: -- @WebService
                    * com.memorynotfound.ws.EmployeeServiceImpl
                    * com.memorynotfound.ws.LoginServiceImpl
                    * com.memorynotfound.ws.OrderServiceImpl
                 -  javax.xml.ws.Endpoint:
                    * com.memorynotfound.ws.WebServicePublisher
                 - **WebServiceClient** (不是 WebService) class:
                    * 无
               + 逻辑层实现 - Servlet
                  - Servlet
                     * 无 -- 后续实现。 -- 目前实现方式是采用 JSP 页面中直接嵌入 Java 逻辑代码。。。
                  - Service
                     * 
               + 前端实现 - Front End - 界面
                  - Web 实现
                     * 方法1：html界面
                        + [http://localhost:8088/lzjaxwsweb9/calculator-my.jsp](http://localhost:8088/lzjaxwsweb9/calculator-my.jsp) --><br>
                           - --> []()<br>
                        + Path：
                           - lzdata-ee-9-gdev/lzdata-ee8-jaxwsweb/src/main/webapp/calculator-my.jsp
                           - lzdata-ee-9-gdev/lzdata-ee8-jaxwsweb/src/main/webapp/calculator-my-response.jsp
                        
                  - Client 实现
                     * Package
                        + com.memorynotfound.client.GreetingClient
                     * 方法
                        + 本机模式
                           1. 执行: com.memorynotfound.ws.WebServicePublisher
                           2. 再执行：com.memorynotfound.client.GreetingClient
                           3.查看结果。。。
                        + 服务器模式
                           1. 将 com.memorynotfound.client.GreetingClient 中， QName设置指向服务器端
                           2. 上传war文件到服务器端
                           3. 再执行：com.memorynotfound.client.GreetingClient  -- Passed





            * GeoIPServiceSoap Service Eaxmple - Soap 1.2 Doc Style
               + Reference
                  - --->
               + Web Page
                  - --> []()<br>
               + WSDL
                  - doc style - default: 默认为document style
                     * http://localhost:8088/lzjaxwsweb9/GeoIPServiceSoapImpl?wsdl
               + SOAP 说明
                  - soap 1.2
               + 后端架构
                 - Package
                    * net.webservicex
                 - Interface class:
                    * net.webservicex.GeoIPServiceSoap
                 - Implementation class: -- @WebService
                    * net.webservicex.GeoIPServiceSoapImpl
                 -  javax.xml.ws.Endpoint:
                    * 无
                 - **WebServiceClient** (不是 WebService) class:
                    * net.webservicex.GeoIPService
               + 逻辑层实现 - Servlet
                  - Servlet
                     * 无 -- 后续实现。 -- 目前实现方式是采用 JSP 页面中直接嵌入 Java 逻辑代码。。。
                  - Service
                     * 
               + 前端实现 - Front End - 界面
                  - Web 实现
                     * 方法1：html界面
                        + [http://localhost:8088/lzjaxwsweb9/calculator-my.jsp](http://localhost:8088/lzjaxwsweb9/calculator-my.jsp) --><br>
                           - --> []()<br>
                        + Path：
                           - lzdata-ee-9-gdev/lzdata-ee9-jaxwsweb/src/main/webapp/calculator-my.jsp
                           - lzdata-ee-9-gdev/lzdata-ee9-jaxwsweb/src/main/webapp/calculator-my-response.jsp
                        
                  - Client 实现
                     * Package
                        + com.soni.LocationFinderMain
                     * 方法
                        + 本机模式
                           1. 执行: 
                           2. 再执行：
                           3.查看结果。。。
                        + 服务器模式
                           1. 将 com.soni.LocationFinderMain 中， QName设置指向服务器端
                           2. 上传war文件到服务器端
                           3. 再执行：com.soni.LocationFinderMain  -- Fail Passed







            * HelloPersonService Service Eaxmple - Soap 1.2 Doc Style
               + Reference
                  - ---> E:\JavaEESamples\JAX-WS\PerDalsten-HelloService
               + Web Page
                  - --> [http://localhost:8088/lzjaxwsweb9/perdalsten-helloservice.jsp](http://localhost:8088/lzjaxwsweb9/perdalsten-helloservice.jsp)<br>
               + WSDL
                  - doc style - default: 默认为document style
                     * http://localhost:8088/lzjaxwsweb9/HelloPersonServiceWS?WSDL
               + SOAP 说明
                  - soap 1.2
               + 后端架构
                 - Package
                    * net.webservicex
                 - Interface class:
                    * com.lzsoft.lzdata.webservice.jaxws.personservice.dk.purplegreen.HelloPersonService
                 - Implementation class: -- @WebService
                    * com.lzsoft.lzdata.webservice.jaxws.personservice.dk.purplegreen.HelloPersonServiceWS
                 -  javax.xml.ws.Endpoint:
                    * 无
                 - **WebServiceClient** (不是 WebService) class:
                    * com.lzsoft.lzdata.webservice.jaxws.personservice.dk.purplegreen.HelloPersonServiceClient
               + 逻辑层实现 - Servlet
                  - Servlet
                     * com.lzsoft.lzdata.weblogic.servlet.dk.purplegreen.HelloPersonServlet
                  - Service
                     * 
               + 前端实现 - Front End - 界面
                  - Web 实现
                     * 方法1：html界面
                        + [http://localhost:8088/lzjaxwsweb9/calculator-my.jsp](http://localhost:8088/lzjaxwsweb9/calculator-my.jsp) --><br>
                           - --> []()<br>
                        + Path：
                           - lzdata-ee-9-gdev/lzdata-ee9-jaxwsweb/src/main/webapp/calculator-my.jsp
                           - lzdata-ee-9-gdev/lzdata-ee9-jaxwsweb/src/main/webapp/calculator-my-response.jsp
                        
                  - Client 实现
                     * Package
                        + com.soni.LocationFinderMain
                     * 方法
                        + 本机模式
                           1. 执行: 
                           2. 再执行：
                           3.查看结果。。。
                        + 服务器模式
                           1. 将 com.soni.LocationFinderMain 中， QName设置指向服务器端
                           2. 上传war文件到服务器端
                           3. 再执行：com.soni.LocationFinderMain  -- Fail Passed










## 分项目
   * lzdata-ee8-servletweb
      + 说明
         1. 模块的架构
            - 中间层Java文件放在模块 lzdata-ee9-servlet-base 中, 通过 lzdata-ee9-servlet-base 模块 调用 数据接入层模块 lzdata-ee9-jpa-model，lzdata-ee9-jpa-model 属于共用模块 其他模块 也可以 调用。。。lzdata-ee9-jpa-model模块参见 数据接入层中，Jakarta Pesistence 模块 的说明。。。
            - 无法使用分模块的功能，合并到 lzdata-ee8-fusionweb 模块中。。。
      + 例子
         - JSP 的例子 - 仅JSP页面的例子
            1. http://localhost:8088/lzservletweb9/index.jsp  --> jakartaee-9
               * 说明
                  + 例子来源：[mastertheboss - jakartaee-9](https://github.com/fmarchioni/mastertheboss.git) -- E:\JavaEESamples\JakartaEE9\mastertheboss\jakartaee\jakartaee-9
                  + 字符集编码 采用 网页级 设置
                  + 没有用 web.xml --> 如果要用可以设置web.xml <welcome-file>index.jsp</welcome-file>
            2. http://localhost:8088/lzservletweb9/helloworldnew.jsp -- JSP 中嵌入的 java 语言 的 实现方法
         - JSP 与 Servlet 结合的例子，实现前后端的分离 -- 网页中不用嵌入的Java了，使得 维护方便了。。。
            1. http://localhost:8088/lzservletweb9/ 默认为 index.html   --> Source：jakartaee-9
            2. http://localhost:8088/lzservletweb9/index.html
               * 1 ~ 2 的说明
                  + 编码设置通过
                     1. Servlet 中，添加 response.setContentType("text/html;charset=UTF-8");
                     2. 网页中设置 UTF-8 的编码
                  + 网页： index.html 、 index_org.html
                  + Servlet
                     1. org.jboss.as.quickstarts.helloworld.HelloService
                     2. org.jboss.as.quickstarts.helloworld.HelloWorldServlet
            3. http://localhost:8088/lzservletweb9/index_cookbook_user.jsp
               * 说明
                  + 同例子 1 类似
                  + 通过 Servlet 生成 页面，返回客服端（前端）
            4. http://localhost:8088/lzservletweb9/index_push.html or http://localhost:8088/lzservletweb9/servlets/servlet/ServerPush
               * 说明
                  + 编码 - 没有设置，因此是乱码：）
                  + 无法显示图片，增加：pb.path(request.getContextPath() -- 解决：pb.path(request.getContextPath() + "/images/javaee-logo.png") 
                  ```java
                     html.append("<img src='" + request.getContextPath() + "/images/javaee-logo.png'><br>");
                  ```
                  + 网页：http://localhost:8088/lzservletweb9/index_push.html -- 改为 index_push.jsp，解决 相对路径的问题。。。
                  + Servlet
                     1. com.lzsoft.lzdata.weblogic.servlet.ServerPush
            5. http://localhost:8088/lzservletweb9/index_cookbook_serverpush.html
               * 说明
                  + 需要了解 HTTP/2.0 ServerPush 机制。。。
                  + 可以通过 PushBuilder pb = request.newPushBuilder(); 的 Push 机制，实现将图片分片发送客户端，以提高客户端加载速度。。
            6. http://localhost:8088/lzeefusionweb9/index_cookbook_ch04_servlet.jsp --> [lzdata-ee9-fusionweb - index_cookbook_ch04_servlet.jsp](#header-index_cookbook_ch04_servlet)<br><a href="#header-index_cookbook_ch04_servlet">lzdata-ee9-fusionweb - index_cookbook_ch04_servlet.jsp</a>
               * 说明
                  + 初始化 参数的方法
                  + 异步数据处理，加载页面的方法 。。。
                     - 无法使用分模块的方式。。。所以放在 ***lzeefusionweb8*** 模块中。。。
         -  JSP 结合 Servlet 和 Persistence 进行数据库的操作例子
            * MySQL 数据库的例子
               1. JSP 页面
               ```jsp
                   http://localhost:8088/lzservletweb9/customer_list.jsp
               ```
               2. Servlet
                  1. Create(添加 或 创建) 部分
                     >com.lzsoft.lzdata.weblogic.servlet.customer.AddCustomerServlet
                  2. Retrieve(检索 或 查询) 部分
                     >com.lzsoft.lzdata.weblogic.servlet.customer.CustomerListServlet
                  3. Update(更新 或 更改) 部分
                     >com.lzsoft.lzdata.weblogic.servlet.customer.UpdateCustomerServlet
                  4. Delete(删除) 部分
                     >com.lzsoft.lzdata.weblogic.servlet.customer.DeleteCustomerServlet
               3. Data Model - lzdata-ee8-jpa-model
                  1. Model
                     >com.lzsoft.lzdata.persistence.hibernate.models.Customer
                  2. Dao
                     >com.lzsoft.lzdata.persistence.hibernate.dao.CustomerDAO
                     >com.lzsoft.lzdata.persistence.hibernate.dao.HibernateCustomerDAO
         - Jakarta Servlet 与 Jakarta Bean Validation 的例子
   * lzdata-ee8-jaxrsweb - REST Service (JAX-RS)
      + 说明
         1. 模块的架构
            - lzdata-ee8-jaxrsweb【前端】 --> lzdata-ee8-jaxrs-base【中间层】 --> lzdata-ee8-jpa-model【数据接入层模块】，lzdata-ee8-jpa-model 属于共用模块 其他模块 也可以 调用。。。lzdata-ee8-jpa-model模块参见 数据接入层中，Jakarta Pesistence 模块 的说明。。。
            - 无法使用分模块的功能，合并到 lzdata-ee8-fusionweb 模块中。。。见 lzdata-ee8-fusionweb 模块的例子说明
      + 例子
         - JAX-RS 的简单例子
            1. http://localhost:8088/lzjaxrsweb9/exampleapi/hello -- {"message":"Duke says 你好，Jakarta EE 9！(Hello to Jakarta EE 9!)!"}
               * 后端实现
                  + com.lzsoft.lzdata.webservice.jaxrs.example.HelloWorldEndpoint
            2. http://localhost:8088/lzjaxrsweb9/exampleapi/greeting/美女 -- {"message":"Say Hello to 美女 at 2020-12-13T22:33:47.362864"}
               * 后端实现
                  + com.lzsoft.lzdata.webservice.jaxrs.example.GreetingResource
         - JSP 结合 JAX-RS，实现Json格式及Java对象的转换
            1. http://localhost:8088/lzjaxrsweb9/index.jsp
               * 说明
                  + tojson的部分：输入信息，转换成Java对象，然后再转换为json，并输出网页。
                     - JSP form 通过 post 将信息以参数的形式传递到 URL：/exampleapi/jsonb/tojson --> http://localhost:8088/lzjaxrsweb9/exampleapi/jsonb/tojson
                     - Service 部分 处理 Java 对象 --> com.lzsoft.lzdata.webservice.jaxrs.person.itbuzzpress.JsonService
                  + tojava部分：输入json格式的对象，如：{ "name": "韶涵", "surname": "张", "address": "台湾台北忠孝东路1号", "city": "台北" }，转换成Java对象，然后输出网页端。
         - JSP 结合 JAX-RS 和 Persistence ，实现 数据库的 CRUD
            1. Customers - CRUD
               * JAX-RS Package Location
                  + com.lzsoft.lzdata.webservice.jaxrs.customer.itbuzzpress.DbCustomerJsonService
                  + Module：lzdata-ee-9-gdev: lzdata-ee8-jaxrs-base
               * Front End - 界面
                  + 方法1：html界面
                     - http://localhost:8088/lzjaxrsweb9/jaxrs-crud-customers.html
                  + 方式2：jsp界面
                     - http://localhost:8088/lzjaxrsweb9/jaxrs-crud-customers-dbtojson.jsp
                        * 说明
                           + 从界面输入数据，存入数据库
                           + 从数据库中取出，用json格式展示在网页。
               * API
                  + http://localhost:8088/lzjaxrsweb9/exampleapi/dbjsonb/dbcustomertojson
            2. http://localhost:8088/lzjaxrsweb9/index_dbstudenttojson.jsp
               * 说明
                  + 从界面输入数据，存入数据库
                  + 从数据库中取出，用json格式展示在网页。
                     - http://localhost:8088/lzjaxrsweb9/exampleapi/dbjsonb/dbstudenttojson
                  + JAX-RS 数据处理部分：lzdata-ee8-jaxrs-base -->  com.lzsoft.lzdata.webservice.jaxrs.customer.itbuzzpress.DbCustomerJsonService

            3. http://localhost:8088/lzeefusionweb9/index.html - origin<br>  将pesistence与resource分模块放就无法实现，甚至：用 jakarta.persistence.NamedQuery, Model也无法实现分模块，但用 List\<Book\> 可以实现 Model 分模块。 参看 [lzdata-ee9fusionweb - index_fruits.html](#header-fruits)<br>
               http://localhost:8088/lzeefusionweb9/index_fruits.html - Path 的 设置方法，未实现
              
               * 说明
                  + 用 jakarta.persistence.NamedQuery 无法实现 分模块
                  + 参考：[]()<br>
                  + html 界面 -- 脚本：angular js --没有实现，angular js 对 path 的 动态path不知如何实现 待了解
                     - http://localhost:8088/lzeefusionweb9/index_fruits.html
                     - http://localhost:8088/lzeefusionweb9/index.html - origin
                  + io.openliberty.example.FruitResource
                  + CRUD部分
                     - Create
                     + Read - 从 mysql 获取数据
                        1. http://localhost:8088/lzeefusionweb8/api/fruits
                        2. http://localhost:8088/lzeefusionweb8/api/fruits/3
                     + Update
                     + Delete
            4. http://localhost:8088/lzjaxrsweb8/exampleapi/persons - 将pesistence与resource分模块放就无法实现 分模块报错, ，甚至：用 jakarta.persistence.NamedQuery, Model也无法实现分模块，但用 List\<Book\> 可以实现 Model 分模块。改为合并模式 --> 参见：[lzeefusionweb8 - PersonResource](#header-person_resource)<br>
              
               * 说明
                  + 参考：[]()<br>
                  + html 界面
                     - 无
                  + com.lzsoft.lzdata.webservice.jaxrs.person.de.rieckpil.blog.PersonResource
                  + CRUD部分
                     - Create
                     + Read - 从 mysql 获取数据
                        1. http://localhost:8088/lzjaxrsweb9/exampleapi/persons  分模块报错, ，甚至：用 jakarta.persistence.NamedQuery, Model也无法实现分模块，但用 List\<Book\> 可以实现 Model 分模块。改为合并模式 --> 参见：[lzeefusionweb8 - PersonResource](#header-person_resource)<br>
                        2. http://localhost:8088/lzeefusionweb9/exampleapi/persons/3
                     + Update
                     + Delete

            5. com.lzsoft.lzdata.webservice.jaxrs.book.BookResource - book crud and async
               * 说明
                  + 参考：[JAX-RS - Getting Started with MicroProfile](https://www.youtube.com/watch?v=-TmKXm0k7UI&feature=youtu.be)<br>
                  + JSP 界面
                     - 无
                  + CRUD部分
                     - Create
                     + Read（Query) - 从 mysql 获取数据
                        1. http://localhost:8088/lzjaxrsweb9/exampleapi/books
                        2. http://localhost:8088/lzjaxrsweb9/exampleapi/books/async - 异步方式，Jax-rs中，将pesistence与resource分模块放就无法实现。。。报错，，甚至：用 jakarta.persistence.NamedQuery, Model也无法实现分模块，但用 List\<Book\> 可以实现 Model 分模块。。是否是变量声明的范围问题 public。。。，应该是 服务器端 本身的问题 -- 待查 - 参见 [lzeefusionweb8 - books/async](#header-books_async)<br>
                        ```
                            RESTEASY003320: Failed processing arguments of public void
                            com.lzsoft.lzdata.webservice.jaxrs.book.BookResource.getBooksAsync(jakarta.ws.rs.container.AsyncResponse)
                        ```
                        3. http://localhost:8088/lzjaxrsweb9/exampleapi/books/6
                     + Update
                     + Delete
                  + 可以将 @PostConstruct 的 init 部分改成 从 数据库中 获取数据

         - JAX-RS: jsonb 与 jsonp 的 使用
            * 说明
               + 例子的来源为
                  - [eclipse-ee4j/glassfish-samples](https://github.com/eclipse-ee4j/glassfish-samples)<br> 不是 [eclipse-ee4j/jakartaee-examples](https://github.com/eclipse-ee4j/jakartaee-examples)<br>
                     
            * 例子
               1. jsonp 的 例子：
                  - 来源
                     * [https://github.com/eclipse-ee4j/glassfish-samples/tree/master/ws/javaee8/jsonp/jaxrs](https://github.com/eclipse-ee4j/glassfish-samples/tree/master/ws/javaee8/jsonp/jaxrs)<br>
                  - 说明
                     * json array 的例子
                        + http://localhost:8088/lzjaxrsweb9/exampleapi/array
                           - org.glassfish.samples.jsonp.jaxrs.ArrayResource
                     * 从数据库获取数据，然后输出array的方法 - 根据 array 的 例子 实现
                        + http://localhost:8088/lzjaxrsweb9/exampleapi/myarray
                           - org.glassfish.samples.jsonp.jaxrs.ArrayResourceMy
                           -  ArrayResourceMy 设置 JsonbConfig config 中用到了 org.glassfish.samples.jsonp.jaxrs.CustomerAdapter
                     * json object 的例子
                        + http://localhost:8088/lzjaxrsweb9/exampleapi/object
                           - org.glassfish.samples.jsonp.jaxrs.ObjectResource
                     * 从数据库获取数据，然后输出object的方法 - 根据 jbject 的 例子 实现，说明：需要加入 id 号，才能得到单个 object 记录。。。
                        + http://localhost:8088/lzjaxrsweb9/exampleapi/myobject/1
                           - org.glassfish.samples.jsonp.jaxrs.ObjectResourceMy
                     * jakarta.json.stream.JsonGenerator 的例子
                        + http://localhost:8088/lzjaxrsweb9/exampleapi/generator
                           - org.glassfish.samples.jsonp.jaxrs.GeneratorResource
                     * jakarta.json.stream.JsonParser 的例子
                        + http://localhost:8088/lzjaxrsweb9/exampleapi/parser
                           - org.glassfish.samples.jsonp.jaxrs.ParserResource
                        + 问题
                           - 由于Twitter更改了api接口1.1 --> 2.0 需要进行用户认证，目前尚未搞碇，Twitter Api 安全认证方式，需要学习。。。
                     * jakarta.json.JsonStructure 的例子
                        + http://localhost:8088/lzjaxrsweb9/exampleapi/structure
                           - org.glassfish.samples.jsonp.jaxrs.StructureResource
               2. jsonb 的 例子：
                  - 来源
                     * [https://github.com/eclipse-ee4j/glassfish-samples/tree/master/ws/javaee8/jsonb/jaxrs](https://github.com/eclipse-ee4j/glassfish-samples/tree/master/ws/javaee8/jsonb/jaxrs)<br>
                  - 说明
                     * serialization 的例子
                        + http://localhost:8088/lzjaxrsweb9/exampleapi/serialization
                           - org.glassfish.samples.jsonb.jaxrs.JsonbSerializationDemo
                     * deserialization 的例子
                        + http://localhost:8088/lzjaxrsweb9/exampleapi/deserialization
                           - org.glassfish.samples.jsonb.jaxrs.JsonbDeserializationDemo
                        + http://localhost:8088/lzjaxrsweb9/exampleapi/generic
                           - org.glassfish.samples.jsonb.jaxrs.JsonbDeserializationGenericDemo
         - JAX-RS，实现 引用 网络上 Json Api 的数据的方法
            * 说明
            * 例子
               1. http://localhost:8088/lzjaxrsweb9/exampleapi/quotes - ApplicationPath需要设置。。。否则，不行。
                  + 来源
                  + 说明
                     - com.lzsoft.lzdata.webservice.jaxrs.quote.de.rieckpil.blog.QuoteResource
                     - com.lzsoft.lzdata.webservice.jaxrs.quote.de.rieckpil.blog.UserAgentClientFilter
                     - com.lzsoft.lzdata.webservice.jaxrs.quote.de.rieckpil.blog.ClientLoggingResponseFilter
                     
              2. http://localhost:8088/lzjaxrsweb9/exampleapi/users  - Get Data from Web Api
                  + 来源
                  + 说明
                     - 更改成新的 wildfly服务器，无法部署，可以是服务器不支持旧的 inject 方法。。。
                     - com.lzsoft.lzdata.webservice.jaxrs.user.de.rieckpil.blog.UserResource
                     - com.lzsoft.lzdata.webservice.jaxrs.user.de.rieckpil.blog.
              3. http://localhost:8088/lzjaxrsweb9/exampleapi/myusers
                 + 说明
                    - 根据上述例子的原理，将UserProvider 合并到 Resource 就可以了，不用 inject 
                    - http://localhost:8088/lzjaxrsweb8/exampleapi/myusers
                    - 代码：com.lzsoft.lzdata.webservice.jaxrs.user.de.rieckpil.blog.UserResourceMy
              4. http://localhost:8088/lzjaxrsweb9/exampleapi/localcustomers
                 + 说明
                    - 同上代码，数据取自 自家服务器的数据：http://localhost:8088/lzjaxrsweb9/exampleapi/myarray
                    - 代码：com.lzsoft.lzdata.webservice.jaxrs.user.de.rieckpil.blog.LocalCustomerResource
         - JSP 结合 JAX-RS，实现 文件的 上传 与 下载
            * JSP 页面
               1. http://localhost:8088/lzjaxrsweb9/index_restfile_angular.jsp 上传下载文件
               2. http://localhost:8088/lzjaxrsweb9/index_restfile_purejsp.jsp
                  - com.lzsoft.lzdata.webservice.jaxrs.upanddownloadfile.mastertheboss
            * JAX-RS 后端实现
               + com.lzsoft.lzdata.webservice.jaxrs.upanddownloadfile.mastertheboss




      + 例子参考：[gmavridakis/SOAP-JAX-WS-RPC]
         + 
      + bbb
      + ddfdf
   * lzdata-ee8-fusionweb
      + Servlet 和 JSP 结合 实现前后端分离，以及异步数据处理的方式
         - <a id="header-index_cookbook_ch04_servlet"></a> http://localhost:8088/lzeefusionweb9/index_cookbook_ch04_servlet.jsp
      
      
      + JAX-RS
         - <a id="header-fruits"></a> http://localhost:8088/lzeefusionweb9/exampleapi/fruits
            * 说明
               + io.openliberty.example.FruitResource
         - <a id="header-books_async"></a> http://localhost:8088/lzeefusionweb9/exampleapi/books/async
            * 说明
               + com.lzsoft.lzdata.webservice.jaxrs.book.de.rieckpil.blog.BookResource
               + Book model 还是 放在 lzdata-ee8-jpa-model 模块中
         - <a id="header-person_resource"></a> http://localhost:8088/lzeefusionweb9/exampleapi/persons
            * 说明
               + com.lzsoft.lzdata.webservice.jaxrs.person.de.rieckpil.blog.PersonResource
               + Person model 还是 放在 lzdata-ee9-jpa-model 模块中      
      + 
## E:\JavaEEDev\JavaEELearningCode\lzdata-ee-8-jaxrs-new

### MySQL CRUD
   * BiDiction   OneToOne
      + 说明
         - 表 Employee 和 Address 为 OneToOne， 并且 共用 相同的 ID， 测试：HibernateJavaConfigMain.java
            1. com.lzsoft.lzdata.javaeebase.jpa.journaldev.HibernateJavaConfigMain
            2. com.lzsoft.lzdata.javaeebase.jpa.journaldev.HibernateAnnotationMain
               * 问题-报错，需要后续处理
               >Exception in thread "main" org.hibernate.MappingException: Unknown entity: com.lzsoft.lzdata.persistence.hibernate.model.employee.Employee
               >...
               >...
               >...
               >	at com.lzsoft.lzdata.javaeebase.jpa.journaldev.HibernateAnnotationMain.main(HibernateAnnotationMain.java:28)
               >
            3. com.lzsoft.lzdata.javaeebase.jpa.journaldev.HibernateLog4jExample
               * 问题-报错，需要后续处理
               >Exception in thread "main" org.hibernate.MappingException: Unknown entity: com.lzsoft.lzdata.persistence.hibernate.model.employee.Employee
               >...
               >...
               >...
               >	at com.lzsoft.lzdata.javaeebase.jpa.journaldev.HibernateAnnotationMain.main(HibernateAnnotationMain.java:28)
               >Exception in thread "main" org.hibernate.query.sqm.InterpretationException: Error interpreting query [from Employee]; this may indicate a semantic (user query) problem or a bug in the parser
            4. com.lzsoft.lzdata.javaeebase.jpa.journaldev.HibernateMain
               * 问题-报错，需要后续处理
               >Exception in thread "main" org.hibernate.MappingException: Unknown entity: com.lzsoft.lzdata.persistence.purebean.EmployeeBean

      + Create
         1. http://localhost:8088/lzjaxrsweb9/resources/bookstore/save
         2. http://localhost:8088/lzjaxrsweb9/resources/bookstoremy/save
      + Read
      + Update
      + Delete
         1. http://localhost:8088/lzjaxrsweb9/resources/bookstore/remove
         2. http://localhost:8088/lzjaxrsweb9/resources/bookstore/removeall
         3. http://localhost:8088/lzjaxrsweb9/resources/bookstoremy/remove
         4. http://localhost:8088/lzjaxrsweb9/resources/bookstoremy/removeall
   
   * BiDiction   OneToMany - ManyToOne
      + Create
         1. http://localhost:8088/lzjaxrsweb9/resources/bookstore/save
         2. http://localhost:8088/lzjaxrsweb9/resources/bookstoremy/save
      + Read
      + Update
      + Delete
         1. http://localhost:8088/lzjaxrsweb9/resources/bookstore/remove
         2. http://localhost:8088/lzjaxrsweb9/resources/bookstore/removeall
         3. http://localhost:8088/lzjaxrsweb9/resources/bookstoremy/remove
         4. http://localhost:8088/lzjaxrsweb9/resources/bookstoremy/removeall
   * Unidirection
      + Create
         1. http://localhost:8088/lzjaxrsweb9/resources/unidirection/bookstoremy/save - addAuthorWithBooks() 有问题？！
         2. http://localhost:8088/lzjaxrsweb9/resources/unidirection/bookstoremy/add - addNewBook()
      + Read
      + Update
      + Delete
         1. http://localhost:8088/lzjaxrsweb9/resources/unidirection/bookstoremy/removefirst
         2. http://localhost:8088/lzjaxrsweb9/resources/unidirection/bookstoremy/removelast
         3. http://localhost:8088/lzjaxrsweb9/resources/unidirection/bookstoremy/removeall
## 测试用：CRUD
   * com.lzsoft.lzdata.javaeebase.jpa.journaldev.HibernateJavaConfigMain
## Sample Data
   * [eugenp/tutorials/patterns/design-patterns-architectural/](https://github.com/eugenp/tutorials/tree/master/patterns/design-patterns-architectural)<br>
### Patterns
   * 参考
      + [DAO vs Repository Patterns](https://www.baeldung.com/java-dao-vs-repository)<br>
      + [The DAO Pattern in Java](https://www.baeldung.com/java-dao-pattern) --> [Sample Code]()<br>
      + [Service Locator Pattern and Java Implementation](https://www.baeldung.com/java-service-locator-pattern)<br>
### json
   * 优先
      + Recipes API - 设计很好，优先参考
         1. https://recipesapi.herokuapp.com/api/search
         2. https://recipesapi.herokuapp.com/api/search?q=chicken&page=3
         3. Get Recipe Details - https://recipesapi.herokuapp.com/api/get?rId=41470
   1. https://andfun-weather.udacity.com/weather
   2. https://andfun-weather.udacity.com/staticweather
   3. https://raw.githubusercontent.com/ujjwalmaity/CountriesApi/master/countriesV1.json


### xml
   1. https://quotes.rest/qod
## 安全性 -- API 认证相关
   * security to an API — HTTP Basic Auth, API Keys, and OAuth
      + 参考
         - [3 Common Methods of API Authentication Explained](https://nordicapis.com/3-common-methods-api-authentication-explained/)<br>
         - [How to Authenticate Users with API Keys](https://symfony.com/doc/4.0/security/api_key_authentication.html)<br>
         - [Upgrade your authentication method to API keys](https://sendgrid.com/docs/for-developers/sending-email/upgrade-your-authentication-method-to-api-keys/)<br>
## 部署的方法
### Wildfly Server
   * 步骤
      1. 编译

      2. 将 war文件拖到部署页面。。。


## 开发 注意事项 说明
   * 关于 字符集 CharSet 与 编码 Encoding：所采用的方式，有模块中单独说明。。。
      + JSP 页面中的设置
      + Servlet 中的设置
         - 方法
         ```java
         
            response.setCharacterEncoding("UTF-8");
            response.setHeader("Content-Type", "text/html;charset=UTF-8");
            // 用下面这一行可以代替上面两行
            // response.setContentType("text/html;charset=UTF-8");
         
         ```
      + 通过 Servlet CharacterEncodingFilter 的方法 参考下面的 Java 文件
         - com.lzsoft.lzdata.webservice.jaxrs.person.itbuzzpress.CharacterEncodingFilter
         - com.lzsoft.lzdata.webservice.jaxrs.person.itbuzzpress.ParameterHelper
         - com.lzsoft.lzdata.webservice.jaxrs.person.itbuzzpress.EncodingFilterMy
   * 关于 绝对路径 和相对路径的说明
      + JSP 页面 中 路径问题的动态处理（动态设置）
         1. 通过 ${pageContext.request.contextPath} + "Relative Path" 来设置 href tag（标签） 
            - 参考：[How to use relative paths without including the context root name?](https://stackoverflow.com/questions/4764405/how-to-use-relative-paths-without-including-the-context-root-name)<br>
         2. 在网页标签 pref中 嵌入 request.getContextPath() 函数的方法：
         ```jsp
             <a href="<%=request.getContextPath()%>/UserServlet"><%=request.getContextPath() %>/UserServlet</a>
         ```
      + Sevelet中的设置，通过：
         1. 通过 request.getContextPath()
         ```java
             // 写法可以参考上句：（用<% %>符号嵌入java语句： href="<%=request.getContextPath()%>/UserServlet" 的方法）
             html.append("<img src='" + request.getContextPath() + "/images/javaee-logo.png'><br>");
         ```
         2. 用 JSP 的 脚本 ${pageContext.request.contextPath}
         ```jsp
             response.sendRedirect("${pageContext.request.contextPath}/customer/list"); 
             也可以用下面的吗？
             response.sendRedirect(${pageContext.request.contextPath + "/customer/list");
         ```
      + Html5页面 是 静态页面，所以只能通过 . 、.. 、/ 等 路径符号来设置
         - 相关设置的方法 - 
         ```
            1. /   = Root directory<br>  - 如果加了 / 表示相对路径是 根目录 如 /images/picture.jpg 表示是根目录下的 images目录下的picture.jpg
            2. .   = This location<br> - 如何是当前目录下面的文件夹，.也可以省略，只要写文件夹名称即可 如 images/picture.jpg 表示当前目录的images目录下的picture.jpg。
            3. ..  = Up a directory<br>
            4. ./  = Current directory<br>
            5. ../ = Parent of current directory<br>
            6. ../../ = Two directories backwards<br>
         ```
## 问题 汇总
