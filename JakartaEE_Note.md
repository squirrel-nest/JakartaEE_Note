# ✨ Jakarta EE 的 开发
## 一些 参考 资料，临时 放这里

<details open>
    <summary>
        <i><b>✨ 参考 资料</b></i>
    </summary>
    <ul type="disc">
        <li>
            [Apache Camel REST step-by-step example](https://www.masterspringboot.com/camel/apache-camel-rest-example-for-beginners/)
        </li>
        <li>
            [Using the Gradle build system in the Eclipse IDE - Tutorial](https://www.vogella.com/tutorials/EclipseGradle/article.html#google_vignette)
        </li>
        <li>
            [Vaadin Flow Quick Start](https://vaadin.com/docs/latest/guide/quick-start)
        </li>
        <li>
            [Eclipse Jetty Programming Guide](https://eclipse.dev/jetty/documentation/jetty-12/programming-guide/index.html)
        </li>
    </ul>
</details>

----

## 开发 环境 的 搭建 

<details open>
    <summary>
        <i><b>✨ 环境 搭建</b></i>
    </summary>
    <ul type="disc">
        <li>
            <details open>
                <summary>
                    <i><b>✨ Java 环境</b></i>
                </summary>
                <ul type="disc">
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 设置</b></i>
                            </summary>
                            <a id="explanation-for-different-ver-in-diff-position"></a>
                            <ul type="disc">
                                <li>
                                    <ol type="i">
                                        <li> - </li>
                                    </ol>
                                </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                            </ul>
                        </details>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ - </b></i>
                            </summary>
                            <a id="explanation-for-different-ver-in-diff-position"></a>
                            <ul type="disc">
                                <li>
                                    <ol type="i">
                                        <li> - </li>
                                    </ol>
                                </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                            </ul>
                        </details>
                    </li>
                </ul>
            </details>
        </li>
        <li>
            <details open>
                <summary>
                    <i><b>✨ Web Server 的 安装 与 设置 </b></i>
                </summary>
                <ul type="disc">
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨  Wildfly 的 安装 与 配置</b></i>
                            </summary>
                            <ul type="disc">
                                <li>
                                    <details open>
                                        <summary>
                                            <i><b>✨ 参见： <a href="https://github.com/huarui0/WebServer_Note/blob/master/WebServer_Wildfly_Note.md">huarui0/WebServer_Note/WebServer_Wildfly_Note.md</a> </b></i>
                                        </summary>
                                        <ul type="disc">
                                            <li> 这个 版本 也是 Deprecated，待 整合：<a href="https://github.com/huarui0/WebServer_Note/blob/master/WildFly%E7%9A%84%E5%AE%89%E8%A3%85%E4%B8%8E%E9%85%8D%E7%BD%AE.md">huarui0/WebServer_Note/WildFly的安装与配置.md</a>
                                            <li>
                                                最旧的 版本：Linux（CentOS）的 <b>单服务器版</b> 安装 与 设置 参见：<a href="https://github.com/huarui0/WebServer_Note/blob/master/Wildfly/2_Note/1_1_0_Wildfly_Stantalone_Note_Centos.txt">1_1_0_Wildfly_Stantalone_Note_Centos.txt</a>
                                            </li>
                                        </ul>
                                    </details>
                                <li>
                                    <details open>
                                        <summary>
                                            <i><b>✨ 附：最旧 的 版本 所在 的 位置</b></i>
                                        </summary>
                                        <ul type="disc">
                                            <li>
                                                最旧的 版本：Linux（CentOS）的 <b>单服务器版</b> 安装 与 设置 参见：<a href="https://github.com/huarui0/WebServer_Note/blob/master/Wildfly/2_Note/1_1_0_Wildfly_Stantalone_Note_Centos.txt">1_1_0_Wildfly_Stantalone_Note_Centos.txt</a>
                                            </li>
                                            <li>
                                                最旧的 版本：Linux（CentOS）的 <b>多服务器版（Domain版）</b> 安装 与 设置 参见：<a href="https://github.com/huarui0/WebServer_Note/blob/master/Wildfly/2_Note/1_1_1_Wildfly_DomainMode_Note_Centos.txt">1_1_1_Wildfly_DomainMode_Note_Centos.txt</a>
                                            </li>
                                            <li>
                                                版本升级 的 最旧 版本 参见：<a href="https://github.com/huarui0/WebServer_Note/blob/master/Wildfly/2_Note/%E5%8D%87%E7%BA%A7_%E8%AF%B4%E6%98%8E.txt">最旧的 升级 说明 </a> 
                                            </li>
                                            <li>
                                                最旧 的 Windows 版本 的 安装 与 设置 参见：<a href="https://github.com/huarui0/WebServer_Note/blob/master/Wildfly/2_Note/1_0_0_Wildfly_Stantalone_Note_Window.txt">1_0_0_Wildfly_Stantalone_Note_Window.txt</a> 
                                            </li>
                                        </ul>
                                    </details>
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

## 项目 的 开发

----

<details open>
    <summary>
        <i><b>✨ 开发 工具</b></i>
    </summary>
    <ul type="disc">
        <li>目前 主要 用 IntelliJ IDEA CE（ 社区版 ） 进行 开发 与 辅助编译， 只要 的 编译 手段 是 用 Gradle 后端 进行 编译，这样 会 灵活 一些，容易 控制 和 进行 错误 查找。</li>
        <li>
            <details open>
                <summary>
                    <i><b>✨ IntelliJ IDEA CE（ 社区版 ）</b></i>
                </summary>
                <ul type="disc">
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 设置</b></i>
                            </summary>
                            <a id="explanation-for-different-ver-in-diff-position"></a>
                            <ul type="disc">
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                            </ul>
                        </details>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ Plugin 的 设置</b></i><br>临时
                                <a href="https://discuss.gradle.org/t/multi-module-project-how-where-to-apply-plugins/46701">Multi-Module Project: How/Where to apply plugins?</a>
                            </summary>
                            <a id="explanation-for-different-ver-in-diff-position"></a>
                            <ul type="disc">
                                <li>
                                    <ol type="i">
                                        <li> The Java Plugin </li>
                                        <li> The War Plugin </li>
                                    </ol>
                                </li>
                                <li> <a href="https://github.com/heroku/heroku-gradle-plugin">heroku/heroku-gradle-plugin</a> </li>
                                <li> <a href="https://github.com/bmuschko/gradle-tomcat-plugin">bmuschko/gradle-tomcat-plugin</a> </li>
                                <li> - </li>
                                <li> - </li>
                            </ul>
                        </details>
                    </li>
                </ul>
            </details>
        </li>
        <li>
            <details open>
                <summary>
                    <i><b>✨ Visual Studio Code</b></i>
                </summary>
                <ul type="disc">
                    <li>✨ 辅助 的 开发 工具，也 很好用</li>
                </ul>
            </details>
        </li>
    </ul>
</details>

----


<details open>
    <summary>
        <i><b>✨ 开发 框架</b></i>
    </summary>
    <ul type="disc">
        <li>
            <details open>
                <summary>
                    <i><b>✨ Native 框架 - Jakarta EE</b></i>
                </summary>
                <ul type="disc">
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 设置</b></i>
                            </summary>
                            <a id="explanation-for-different-ver-in-diff-position"></a>
                            <ul type="disc">
                                <li>
                                    <ol type="i">
                                        <li> - </li>
                                    </ol>
                                </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                            </ul>
                        </details>
                    </li>
                </ul>
            </details>
        </li>
        <li>
            <details open>
                <summary>
                    <i><b>✨ Spring</b></i>
                </summary>
                <ul type="disc">
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ Spring 框架</b></i>
                            </summary>
                            <a id="explanation-for-different-ver-in-diff-position"></a>
                            <ul type="disc">
                                <li>
                                    <ol type="i">
                                        <li> - </li>
                                    </ol>
                                </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                            </ul>
                        </details>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ Spring boot 轻量框架</b></i>
                            </summary>
                            <a id="explanation-for-different-ver-in-diff-position"></a>
                            <ul type="disc">
                                <li>
                                    <a href="https://spring.pleiades.io/spring-boot/docs/current/gradle-plugin/reference/htmlsingle/">Spring Boot Gradle プラグインリファレンスガイド</a>
                                </li>
                                </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                            </ul>
                        </details>
                    </li>
                </ul>
            </details>
        </li>
    </ul>
</details>

----

<details open>
    <summary>
        <i><b>✨ 我们 项目 的 结构 和 脉络</b></i>
    </summary>
    <ul type="disc">
        <li>
            <details open>
                <summary>
                    <i><b>✨ 概述 - 简要说明</b></i>
                </summary>
                <ul type="disc">
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 设置</b></i>
                            </summary>
                            <a id="explanation-for-different-ver-in-diff-position"></a>
                            <ul type="disc">
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                            </ul>
                        </details>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ - </b></i>
                            </summary>
                            <a id="explanation-for-different-ver-in-diff-position"></a>
                            <ul type="disc">
                                <li>
                                    <ol type="i">
                                        <li> - </li>
                                    </ol>
                                </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                                <li> - </li>
                            </ul>
                        </details>
                    </li>
                </ul>
            </details>
        </li>
    </ul>
</details>

----

<details open>
    <summary>
        <i><b>✨ 创建 项目</b></i>
    </summary>
    <ul type="disc">
        <li>
            <details open>
                <summary>
                    <i><b>✨ 创建 项目 的 步骤 </b></i>
                </summary>
                <ul type="disc">
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨  新建 项目 的 方法 </b></i>
                            </summary>
                            <a id="explanation-for-different-ver-in-diff-position"></a>
                            <ul type="disc">
                                <li>
                                    <details open>
                                        <summary>
                                            <i><b>✨ 完全 新建 一个 （空 或者 有 hello world界面）的 项目，然后 拷贝（添加）需要 的 依赖项 和 插件 的 方法</b></i>
                                        </summary>
                                        <a id="explanation-for-mysql-install-by-brew-mode" ></a>
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
                                            <i><b>✨ 手动 添加 文件 的 方法</b></i>
                                        </summary>
                                        <a id="explanation-for-mysql-install-by-brew-mode" ></a>
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
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨  拷贝 （旧）项目 模版 的 方法</b></i>
                            </summary>
                            <a id="explanation-for-different-ver-in-diff-position"></a>
                            <ul type="disc">
                                <li>
                                    <details open>
                                        <summary>
                                            <i><b>✨ 手动 添加 文件 的 方法</b></i>
                                        </summary>
                                        <ul type="disc">
                                            <li>
                                                ✨ 创建 的 项目 模版 位置：<br>
                                                &nbsp;&nbsp;/Users/Codes/JakartaEEProjects/01_LearningCode/lzdata-ee-10-gdev_template
                                            </li>
                                            <li>
                                                <details open>
                                                    <summary>
                                                        <i><b>✨ 步骤 - 2024-03-25</b></i>
                                                    </summary>
                                                    <a id="explanation-for-mysql-install-by-brew-mode" ></a>
                                                    <ol type="disc">
                                                        <li>
                                                            <details open>
                                                                <summary>
                                                                    <i><b>✨ ✨ 拷贝 文件 夹 gradle 文件夹</b></i>
                                                                </summary>
                                                                <ul type="disc">
                                                                    <li>截图 1：
                                                                        <img width="1655" alt="image" src="https://github.com/squirrel-nest/JakartaEE_Note/assets/8960325/efc0410a-d73c-40f4-a996-09f90a5a2774">
                                                                    </li>
                                                                </ul>
                                                            </details>
                                                        </li>
                                                        <li>
                                                            <details open>
                                                                <summary>
                                                                    <i><b>✨ settings.gradle.kts 文件 的 建立</b></i>
                                                                </summary>
                                                                <ul type="square">
                                                                    <li>
                                                                        <details open>
                                                                            <summary>
                                                                                <i><b>✨ dependency 和 plugin 的 管理 - 采用 version catalog 方式 管理</b></i>
                                                                            </summary>
                                                                            <ul type="square">
                                                                                <li>
                                                                                    <details open>
                                                                                        <summary>
                                                                                            <i><b>✨ toml 文件 的 添加</b></i>
                                                                                        </summary>
                                                                                        <ul type="circle">
                                                                                            <li>
                                                                                                toml 文件 的 添加 原则：<br>
                                                                                                1. 根据 dependency 和 plugin 的 类型 或 功能，进行 添加，比如：<br>
                                                                                                a. Jakarta Platform 相关 作为 一个 文件<br>
                                                                                                b. Hibernate 相关 作为 一个 文件<br>
                                                                                                c. Database 相关 作为 一个 文件<br>
                                                                                            </li>
                                                                                            <li>
                                                                                                根据 不同 类型 的 dependency 和 plugin，在 gradle 文件夹 中，添加 toml 文件。<br>
                                                                                                如：Jakarta Platform 相关 的 功能模块， 创建 名称 为 /Users/Codes/JakartaEEProjects/01_LearningCode/lzdata-ee-10-gdev_template/gradle/libs_jakarta.versions.toml 的 toml 文件，<br>
                                                                                                仅 在 这个 模块 中，添加 Jakarta 相关 的 dependency 和 plugin。
                                                                                            </li>
                                                                                            <li>
                                                                                                toml 文件： 根据 不同 类型 的 dependency 和 plugin，创建  指定 的 settings.gradle.kts 文件。<br>
                                                                                                如：Jakarta Platform 相关 的 功能模块， 创建 名称 为 /Users/Codes/JakartaEEProjects/01_LearningCode/lzdata-ee-10-gdev_template/gradle/libs_jakarta.versions.toml 的 toml 文件，仅 在 这个 模块 中，添加 Jakarta 相关 的 dependency 和 plugin 等。
                                                                                            </li>
                                                                                            <li>截图 2 - 内容：
                                                                                                <img width="1706" alt="image" src="https://github.com/squirrel-nest/JakartaEE_Note/assets/8960325/3b05c561-def4-4444-8258-17f1b15b0856">
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
                                                                                <i><b>✨ 不同 功能 模块 的 管理</b></i>
                                                                            </summary>
                                                                            <ul type="square">
                                                                                <li>
                                                                                    <details open>
                                                                                        <summary>
                                                                                            <i><b>✨ settings.gradle.kts 文件 的 建立</b></i>
                                                                                        </summary>
                                                                                        <ol type="1">
                                                                                            <li>
                                                                                                先 拷贝 最初的 settings.gradle.kts，更名为 settings_org.gradle.kts，并 更改 项目 名称 rootProject.name = "PureCompose33" 为 当前 项目 的 名称<br>
                                                                                                <img width="1290" alt="image" src="https://github.com/squirrel-nest/JakartaEE_Note/assets/8960325/e3a4595b-de0b-467a-8389-19438a56fa7f">
                                                                                            </li>
                                                                                            <li>
                                                                                                根据 不同 类型 的 功能 模块，创建 指定 的 settings.gradle.kts 文件，比如 针对 jakarta servlet 相关 的 功能 模块，可以 创建 settings_jakarta_servlet.gradle.kts，仅 在 这个 模块 中，将 相应 的 功能 模块 include 进来。
                                                                                                <br>
                                                                                            </li>
                                                                                        </ol>
                                                                                    </details>
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
                                        </ul>
                                    </details>
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


## 项目 的 调试 与 测试

----

## 项目 的 编译 与 部署

<details open>
    <summary>
        <i><b>✨ Build Tools - 编译 和 生成 工具</b></i>
    </summary>
    <ul type="disc">
        <li>
            <details open>
                <summary>
                    <i><b>✨ Build Tools - 编译 和 生成 工具</b></i>
                </summary>
                <ul type="square">
                    <li>目前 主要 用 Gradle 编译， 与 Maven 比较， 不知 哪个 更好，Gradle 直观 一些。</li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ Gradle Build Tool</b></i>
                            </summary>
                            <ul type="disc">
                                <li>✨ 笔记 参见：<a href="https://github.com/squirrel-nest/BuildTool_Note/tree/master">BuildTool_Note</a> --> <a href="https://github.com/squirrel-nest/BuildTool_Note/blob/master/Gradle_Note.md">BuildTool_Note/Gradle_Note.md</a>
                                </li>
                            </ul>
                        </details>
                    </li>
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ Maven Build Tool</b></i>
                            </summary>
                            <ul type="disc">
                                <li>
                                    ✨ 笔记 参见：<a href="https://github.com/squirrel-nest/BuildTool_Note/tree/master">BuildTool_Note</a> --> <a href="https://github.com/squirrel-nest/BuildTool_Note/blob/master/Maven_Note.md">BuildTool_Note/Maven_Note.md</a>
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
                    <i><b>✨ Deployment - 部署</b></i>
                </summary>
                <ul type="square">
                    <li>
                        <details open>
                            <summary>
                                <i><b>✨ 部署到 Wildfly</b></i>
                            </summary>
                            <ul type="disc">
                                <li>✨ 笔记 参见：<a href="https://github.com/huarui0/WebServer_Note/tree/master">WebServer_Note</a> --> <a href="">Wildfly 的 笔记 （待改）</a>
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

# Java SE LearningNote --> [JavaSELearningNote.md](https://github.com/squirrel-nest/JavaSELearningNote/blob/master/JavaSE_Note.md)<br>
# Jakarta EE 8 Reference
## 前瞻性 - 在开始Java EE 的学习旅程之前，先了解了解 前瞻性的问题，把握好学习的方向，2020.4.5 -之后这些也许又落伍了 - 理解：周虽旧邦，其命维新 的 发展规律
   * 研究项目
      + Quarkus: Supersonic Subatomic Java. -->[https://quarkus.io](https://quarkus.io)<br>
         - [QUARKUS - GUIDES](https://quarkus.io/guides/)<br>
         - 源代码： --> [quarkusio/quarkus](https://quarkus.io/guides/)<br>
   * [https://zhuanlan.zhihu.com/p/78720067](云原生时代JAVA语言的求生之路) - 参考其中的 reference<br>
   * [Java生态系统总结(QCon2019)](http://monkeybean.cn/2019/05/12/qcon2019/)<br>
   * [Kubernetes 是什么？](https://kubernetes.io/zh/docs/concepts/overview/what-is-kubernetes/)<br>
   * [EE4J Projects - Technical Direction](https://docs.google.com/document/d/12vO9Ztcxyd6oxDnKFi73p7JsYaPgifpepggFxzW_uyE/edit#)<br>
   * [GraalVM - High-performance polyglot VM: What does GraalVM do?](https://www.graalvm.org/)<br>
   * [Spring Cloud 使用 Kubernetes 作为配置中心 - 使用加密配置](https://blog.csdn.net/u013360850/article/details/100635538)<br>
## SDK Download
   * [Java™ EE 8 SDK Downloads](https://www.oracle.com/java/technologies/javaee-8-sdk-downloads.html)<br>

## Jakarta EE 9
### 0. Jakarta EE Specifications --> [Jakarta EE Specifications](https://jakarta.ee/specifications/)<br>
   * 0_1. Jakarta RESTful Web Services --> [Jakarta RESTful Web Services 3.0 (milestone)](https://jakarta.ee/specifications/restful-ws/3.0/)<br>
      + --> [Jakarta RESTful Web Services - PDF](https://jakarta.ee/specifications/restful-ws/3.0/restful-ws-spec-3.0-M1.pdf)<br> 
      + --> [Jakarta RESTful Web Services - HTML](https://jakarta.ee/specifications/restful-ws/3.0/restful-ws-spec-3.0-M1.html)<br>
### Weld Meets Jakarta EE 9
   * 参考
      + [Weld Meets Jakarta EE 9](http://weld.cdi-spec.org/news/2020/05/13/weld-jakarta-ee-9/)<br>
## Jakarta EE 8 的学习路径
### 0. Jakarta EE 8 --> [Jakarta EE 8](https://projects.eclipse.org/jakartaee/releases/8)<br>

### 0_1. Jakarta EE Tutorial Project --> [Jakarta EE Tutorial Project](https://eclipse-ee4j.github.io/jakartaee-tutorial/)<br>
### 0_2. eclipse-ee4j/jakartaee-tutorial（需要编译） --> [eclipse-ee4j/jakartaee-tutorial](https://github.com/eclipse-ee4j/jakartaee-tutorial)<br>
### 1. Jakarta EE Persistence --> [JakartaEEPersistenceLearningNote.md](https://github.com/squirrel-nest/JavaEELearningNote/blob/master/JakartaEEPersistenceLearningNote.md)
:point_down::small_red_triangle_down::arrow_down::arrow_down_small::arrow_double_down::arrow_double_down:
### 2. Jakarta EE JsonB --> [JakartaEEJsonBLearningNote.md](https://github.com/squirrel-nest/JavaEELearningNote/blob/master/JakartaEEJsonBLearningNote.md)
   * 参考
      + [Using Jakarta REST with Jakarta XML Binding[(https://eclipse-ee4j.github.io/jakartaee-tutorial/jaxrs-advanced007.html)<br>
      + [https://eclipse-ee4j.github.io/jakartaee-tutorial/cdi-adv006.html)<b>
      + [Using Interceptors in CDI Applications](https://eclipse-ee4j.github.io/jakartaee-tutorial/cdi-adv006.html)<br>
  
### 3. Jakarta EE JsonP --> []()<br>


### 4. [Jakarta EE 8 CRUD API Tutorial using Java 11](https://rieckpil.de/jakarta-ee-crud-api-tutorial/)<br>

### 5. [Handling Pagination With JAX-RS and NoSQL in Your Jakarta EE/MicroProfile Application](https://dzone.com/articles/handling-with-pagination-with-jax-rs-in-your-jakar)<br>

### 6. [JAX-RS Crud Application using Quarkus and Vue.js](http://www.mastertheboss.com/soa-cloud/quarkus/jax-rs-crud-application-using-quarkus-and-vue-js)<br>
### 7. [JAX-RS CRUD Application using Vue.js and RESTEasy](http://www.mastertheboss.com/jboss-frameworks/resteasy/jax-rs-crud-application-using-vue-js-and-resteasy)<br> - 可以参考 curl 的使用方法，了解 命令中 参数的用法。。。
   * [RESTEasy tutorial - Page 1](http://www.mastertheboss.com/jboss-frameworks/resteasy/resteasy-tutorial)<br>
   * [RESTEasy tutorial - Page 2](http://www.mastertheboss.com/jboss-frameworks/resteasy/resteasy-tutorial?showall=&start=1)<br>
### 8. [CRUD with TomEE, MicroProfile, and REST](https://www.tomitribe.com/blog/crud-with-tomee-microprofile-and-rest/)<br>


### JAX-RS


### JAX-WS
   * Interface And Class
      + Service implementation class and Service class
         - targetNamespace规则：参看：3.11. Service and Ports 
         - 没有 @ServiceName annotation - if present with a non-default value, otherwise the name of the implementation class with the "Service" suffix appended to it.
         - 7.11.1. jakarta.jws.WebService - 7.11. Annotations Defined by Jakarta XML Web Services Metadata

  * **需要看下：**WS User Guide  - WildFly Documentation
     + [WS User Guide  - WildFly Documentation](https://docs.jboss.org/author/display/WFLY/JAX-WS%20User%20Guide.html)<br>


### 9. Jakarta EE Bean
   * 参考
      + [Java Bean Validation Basics](https://www.baeldung.com/javax-validation)<br>
### 10. CHAPTER 7. JAKARTA CONTEXTS AND DEPENDENCY INJECTION
   * 参考
      + [CHAPTER 7. JAKARTA CONTEXTS AND DEPENDENCY INJECTION](https://access.redhat.com/documentation/en-us/red_hat_jboss_enterprise_application_platform/7.3/html/development_guide/contexts_and_dependency_injection)<br>
### 5. 测试相关
   * [Testing a MicroProfile or Jakarta EE application](https://openliberty.io/guides/microshed-testing.html)<br>

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
   * [From javax.* to jakarta.*: A Simple Proof of Concept](https://dzone.com/articles/from-javax-to-jakarta-a-simple-proof-of-concept)<br>
   * [从一次编译出发梳理概念: Jetty,Jersey,hk2,glassFish,Javax,Jakarta](https://cloud.tencent.com/developer/article/1702027)<br>
      + (https://www.cnblogs.com/rossiXYZ/p/13694489.html#27-glassfish)<br>
      + (https://iter01.com/530958.html)<br>
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
### Security
  * 参考
    + [Securing REST APIs with RESTEasy Filter](https://howtodoinjava.com/resteasy/resteasy-containerrequestfilter-example/)
## 包的管理
### 包的网址
   * **Maven Central Repository --> [Maven Central Repository](https://repo.maven.apache.org/) --> [Maven Central Repository: Maven2](https://repo.maven.apache.org/maven2/) - Maven Central Repository: Maven2的位置**<br>
   * Maven Central Repository 的搜索引擎 --> [The Central Repository Search Engine](https://search.maven.org/) -- 如果找到，但在IntelliJ Idea中无法用maven或gradle下载，到Maven Central Repository中没有查到，说明尚未更新到Maven Central Repository<br>
   * 次要位置 - 一般网上查的都是这个网址，但更新稍有滞后 -- [Maven Repository](https://mvnrepository.com/)<br>

   * Gradle Plugin Portal： Gradle plugins 的搜索引擎： [Search Gradle plugins - Gradle Plugin Portal](https://plugins.gradle.org/search)<br>
### 本地文件包位置
   * Gradle
      + C:\Users\userhome\\.gradle\caches\modules-2\files-2.1\
   * Maven
      + C:\Users\userhome\\.m2\repository\

## <a name="compile-command"></a>编译命令
### Gradle - 包括 Android
   * 参见: 基本命令参考 - [总结的Gradle常用编译命令](https://github.com/squirrel-nest/BuildTool_Note/blob/master/Gradle_Note.md#compile-command)<br>
### Maven
   * Build whole project with maven.
      ```shell
          mvn clean install 
          or
          mvn clean package - without clean as well
## <a name="charset-encoding"></a>字符集及编码相关
### 一般性知识
   * 参考
      + [UTF-8: The Secret of Character Encoding](http://htmlpurifier.org/docs/enduser-utf8.html)<br>
### Jakarta EE 相关部分
   * 参考
      + [Character Sets and Encodings](https://eclipse-ee4j.github.io/jakartaee-tutorial/webi18n004.html#BNAYB)<br>
      + [Character Conversions from Browser to Database](https://www.oracle.com/technical-resources/articles/javase/httpcharset.html)<br>
      + 仅参考，注意：不同的服务器有不同的设置方法 服务器级别的设置 - [How to set charset for my web application?](https://developer.jboss.org/message/804018#804018)<br>
   * 用 filter 的方法
      + [The Essentials of Filters - Example: Modifying the Request Character Encoding](https://www.oracle.com/java/technologies/filters.html)<br>
      ```java
        public void doFilter(ServletRequest request, 
        ServletResponse response, FilterChain chain) throws
        IOException, ServletException {
            String encoding = selectEncoding(request);
            if (encoding != null)
            request.setCharacterEncoding(encoding);
            chain.doFilter(request, response);
            }
            public void init(FilterConfig filterConfig) throws
            ServletException {
            this.filterConfig = filterConfig;
            this.encoding = filterConfig.getInitParameter("encoding");
            }
            protected String selectEncoding(ServletRequest request) {
            return (this.encoding);
        } 
      ```
      + [Tomcat中设置Fileter的方法 - tomcat/conf/web.xml](https://github.com/apache/tomcat/blob/master/conf/web.xml)<br>
         - Source Code
            - [tomcat/java/org/apache/catalina/filters/SetCharacterEncodingFilter.java](https://github.com/apache/tomcat/blob/master/java/org/apache/catalina/filters/SetCharacterEncodingFilter.java)<br>
            ```java
                package org.apache.catalina.filters;

                import java.io.IOException;

                import jakarta.servlet.FilterChain;
                import jakarta.servlet.ServletException;
                import jakarta.servlet.ServletRequest;
                import jakarta.servlet.ServletResponse;

                import org.apache.juli.logging.Log;
                import org.apache.juli.logging.LogFactory;

                public class SetCharacterEncodingFilter extends FilterBase {

                    // Log must be non-static as loggers are created per class-loader and this
                    // Filter may be used in multiple class loaders
                    private final Log log = LogFactory.getLog(SetCharacterEncodingFilter.class); // must not be static


                    // ----------------------------------------------------- Instance Variables

                    /**
                     * The default character encoding to set for requests that pass through
                     * this filter.
                     */
                    private String encoding = null;
                    public void setEncoding(String encoding) { this.encoding = encoding; }
                    public String getEncoding() { return encoding; }


                    /**
                     * Should a character encoding specified by the client be ignored?
                     */
                    private boolean ignore = false;
                    public void setIgnore(boolean ignore) { this.ignore = ignore; }
                    public boolean isIgnore() { return ignore; }


                    // --------------------------------------------------------- Public Methods


                    /**
                     * Select and set (if specified) the character encoding to be used to
                     * interpret request parameters for this request.
                     *
                     * @param request The servlet request we are processing
                     * @param response The servlet response we are creating
                     * @param chain The filter chain we are processing
                     *
                     * @exception IOException if an input/output error occurs
                     * @exception ServletException if a servlet error occurs
                     */
                    @Override
                    public void doFilter(ServletRequest request, ServletResponse response,
                                         FilterChain chain)
                        throws IOException, ServletException {

                        // Conditionally select and set the character encoding to be used
                        if (ignore || (request.getCharacterEncoding() == null)) {
                            String characterEncoding = selectEncoding(request);
                            if (characterEncoding != null) {
                                request.setCharacterEncoding(characterEncoding);
                            }
                        }

                        // Pass control on to the next filter
                        chain.doFilter(request, response);
                    }


                    // ------------------------------------------------------ Protected Methods

                    @Override
                    protected Log getLogger() {
                        return log;
                    }


                    /**
                     * Select an appropriate character encoding to be used, based on the
                     * characteristics of the current request and/or filter initialization
                     * parameters.  If no character encoding should be set, return
                     * <code>null</code>.
                     * <p>
                     * The default implementation unconditionally returns the value configured
                     * by the <strong>encoding</strong> initialization parameter for this
                     * filter.
                     *
                     * @param request The servlet request we are processing
                     * @return the encoding that was configured
                     */
                    protected String selectEncoding(ServletRequest request) {
                        return this.encoding;
                    }
                }
            ```
            
            
            
            
         
