# Jakarta EE Project
## 说明
   * 框架搭建分为 Jakarta EE 8 和 Jakarta EE 9， 以 Jakarta EE 8 作为开发的主线, Jakarta EE 9通过拷贝 Jakarta EE 8来获得, 然后修改 javax 包名 到 jakarta, 共用的模块用 _share_ 或 _common_ 
   * 总项目文件夹：E:\JavaEEDev\JavaEELearningCode\lzdata-ee-9-gdev
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
## 问题汇总
   1. 。。
### 分项目
   * lzdata-ee8-servletweb
      + 说明
         1. 模块的架构
            - 中间层Java文件放在模块 lzdata-ee8-servlet-base 中, 通过 lzdata-ee8-servlet-base 模块 调用 数据接入层模块 lzdata-ee8-jpa-model，lzdata-ee8-jpa-model 属于共用模块 其他模块 也可以 调用。。。lzdata-ee8-jpa-model模块参见 数据接入层中，Jakarta Pesistence 模块 的说明。。。
            - 无法使用分模块的功能，合并到 lzdata-ee8-fusionweb 模块中。。。
      + 例子
         - JSP 的例子 - 仅JSP页面的例子
            1. http://localhost:8089/lzservletweb8/index.jsp  --> jakartaee-9
               * 说明
                  + 例子来源：[mastertheboss - jakartaee-9](https://github.com/fmarchioni/mastertheboss.git) -- E:\JavaEESamples\JakartaEE9\mastertheboss\jakartaee\jakartaee-9
                  + 字符集编码 采用 网页级 设置
                  + 没有用 web.xml --> 如果要用可以设置web.xml <welcome-file>index.jsp</welcome-file>
            2. http://localhost:8089/lzservletweb8/helloworldnew.jsp -- JSP 中嵌入的 java 语言 的 实现方法
         - JSP 与 Servlet 结合的例子，实现前后端的分离 -- 网页中不用嵌入的Java了，使得 维护方便了。。。
            1. http://localhost:8089/lzservletweb8/ 默认为 index.html   --> Source：jakartaee-9
            2. http://localhost:8089/lzservletweb8/index.html
               * 1 ~ 2 的说明
                  + 编码设置通过
                     1. Servlet 中，添加 response.setContentType("text/html;charset=UTF-8");
                     2. 网页中设置 UTF-8 的编码
                  + 网页： index.html 、 index_org.html
                  + Servlet
                     1. org.jboss.as.quickstarts.helloworld.HelloService
                     2. org.jboss.as.quickstarts.helloworld.HelloWorldServlet
            3. http://localhost:8089/lzservletweb8/index_cookbook_user.jsp
               * 说明
                  + 同例子 1 类似
                  + 通过 Servlet 生成 页面，返回客服端（前端）
            4. http://localhost:8089/lzservletweb8/index_push.html or http://localhost:8089/lzservletweb8/servlets/servlet/ServerPush
               * 说明
                  + 编码 - 没有设置，因此是乱码：）
                  + 无法显示图片，增加：pb.path(request.getContextPath() -- 解决：pb.path(request.getContextPath() + "/images/javaee-logo.png") 
                  ```java
                     html.append("<img src='" + request.getContextPath() + "/images/javaee-logo.png'><br>");
                  ```
                  + 网页：http://localhost:8089/lzservletweb8/index_push.html -- 改为 index_push.jsp，解决 相对路径的问题。。。
                  + Servlet
                     1. com.lzsoft.lzdata.weblogic.servlet.ServerPush
            5. http://localhost:8089/lzservletweb8/index_cookbook_serverpush.html
               * 说明
                  + 需要了解 HTTP/2.0 ServerPush 机制。。。
                  + 可以通过 PushBuilder pb = request.newPushBuilder(); 的 Push 机制，实现将图片分片发送客户端，以提高客户端加载速度。。
            6. http://localhost:8089/lzeefusionweb8/index_cookbook_ch04_servlet.jsp --> [lzdata-ee8-fusionweb - index_cookbook_ch04_servlet.jsp](#header-index_cookbook_ch04_servlet)<br>
               * 说明
                  + 初始化 参数的方法
                  + 异步数据处理，加载页面的方法 。。。
                     - 无法使用分模块的方式。。。所以放在 ***lzeefusionweb8*** 模块中。。。
         -  JSP 结合 Servlet 和 Persistence 进行数据库的操作例子
            * MySQL 数据库的例子
               1. JSP 页面
               ```jsp
                   http://localhost:8089/lzservletweb8/customer_list.jsp
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
            1. http://localhost:8089/lzjaxrsweb8/exampleapi/hello -- {"message":"Duke says 你好，Jakarta EE 9！(Hello to Jakarta EE 9!)!"}
               * 后端实现
                  + com.lzsoft.lzdata.webservice.jaxrs.example.HelloWorldEndpoint
            2. http://localhost:8089/lzjaxrsweb8/exampleapi/greeting/美女 -- {"message":"Say Hello to 美女 at 2020-12-13T22:33:47.362864"}
               * 后端实现
                  + com.lzsoft.lzdata.webservice.jaxrs.example.GreetingResource
         - JSP 结合 JAX-RS，实现Json格式及Java对象的转换
            1. http://localhost:8089/lzjaxrsweb8/index.jsp
               * 说明
                  + tojson的部分：输入信息，转换成Java对象，然后再转换为json，并输出网页。
                     - JSP form 通过 post 将信息以参数的形式传递到 URL：/exampleapi/jsonb/tojson --> http://localhost:8089/lzjaxrsweb8/exampleapi/jsonb/tojson
                     - Service 部分 处理 Java 对象 --> com.lzsoft.lzdata.webservice.jaxrs.person.itbuzzpress.JsonService
                  + tojava部分：输入json格式的对象，如：{ "name": "韶涵", "surname": "张", "address": "台湾台北忠孝东路1号", "city": "台北" }，转换成Java对象，然后输出网页端。
         - JSP 结合 JAX-RS 和 Persistence ，实现 数据库的 CRUD
            1. http://localhost:8089/lzjaxrsweb8/index_dbcustomertojson.jsp
               * 说明
                  + 从界面输入数据，存入数据库
                  + 从数据库中取出，用json格式展示在网页。
                     - http://localhost:8089/lzjaxrsweb8/exampleapi/dbjsonb/dbcustomertojson
                  + JAX-RS 数据处理部分：lzdata-ee8-jaxrs-base -->  com.lzsoft.lzdata.webservice.jaxrs.person.itbuzzpress.DbCustomerJsonService
            2. http://localhost:8089/lzjaxrsweb8/index_dbstudenttojson.jsp
               * 说明
                  + 从界面输入数据，存入数据库
                  + 从数据库中取出，用json格式展示在网页。
                     - http://localhost:8089/lzjaxrsweb8/exampleapi/dbjsonb/dbstudenttojson
                  + JAX-RS 数据处理部分：lzdata-ee8-jaxrs-base -->  com.lzsoft.lzdata.webservice.jaxrs.person.itbuzzpress.DbStudentJsonService

            3. http://localhost:8089/lzeefusionweb8/index.html - origin<br>
               http://localhost:8089/lzeefusionweb8/index_fruits.html - Path 的 设置方法，未实现
              
               * 说明
                  + 参考：[]()<br>
                  + html 界面 -- 脚本：angular js --没有实现，angular js 对 path 的 动态path不知如何实现 待了解
                     - http://localhost:8089/lzeefusionweb8/index_fruits.html
                     - http://localhost:8089/lzeefusionweb8/index.html - origin
                  + io.openliberty.example.FruitResource
                  + CRUD部分
                     - Create
                     + Read - 从 mysql 获取数据
                        1. http://localhost:8089/lzeefusionweb8/api/fruits
                        2. http://localhost:8089/lzeefusionweb8/api/fruits/3
                     + Update
                     + Delete

            4. com.lzsoft.lzdata.webservice.jaxrs.book.BookResource - book crud and async
               * 说明
                  + 参考：[JAX-RS - Getting Started with MicroProfile](https://www.youtube.com/watch?v=-TmKXm0k7UI&feature=youtu.be)<br>
                  + JSP 界面
                     - 无
                  + CRUD部分
                     - Create
                     + Read（Query) - 从 mysql 获取数据
                        1. http://localhost:8089/lzjaxrsweb8/exampleapi/books
                        2. http://localhost:8089/lzjaxrsweb8/exampleapi/books/async - 异步方式，Jax-rs中，将pesistence与resource分模块放就无法实现。。。报错。是否是变量声明的范围问题 public。。。，应该是 服务器端 本身的问题 -- 待查 - 参见 [lzeefusionweb8 - books/async](#header-books_async)<br>
                        ```
                            RESTEASY003320: Failed processing arguments of public void
                            com.lzsoft.lzdata.webservice.jaxrs.book.BookResource.getBooksAsync(jakarta.ws.rs.container.AsyncResponse)
                        ```
                        3. http://localhost:8089/lzjaxrsweb8/exampleapi/books/6
                     + Update
                     + Delete
                  + 可以将 @PostConstruct 的 init 部分改成 从 数据库中 获取数据


         - JAX-RS，实现 引用 网络上 Json Api 的数据的方法
            * 说明
            * 例子
               1. http://localhost:8089/lzjaxrsweb8/exampleapi/quotes - ApplicationPath需要设置。。。否则，不行。
                  + 说明
                     - com.lzsoft.lzdata.webservice.jaxrs.quote.de.rieckpil.blog.QuoteResource
                     - com.lzsoft.lzdata.webservice.jaxrs.quote.de.rieckpil.blog.UserAgentClientFilter
                     - com.lzsoft.lzdata.webservice.jaxrs.quote.de.rieckpil.blog.ClientLoggingResponseFilter
                     
              10. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/users  - Get Data from Web Api

         - JSP 结合 JAX-RS，实现 文件的 上传 与 下载
            * JSP 页面
               1. http://localhost:8089/lzjaxrsweb8/index_restfile_angular.jsp 上传下载文件
               2. http://localhost:8089/lzjaxrsweb8/index_restfile_purejsp.jsp
                  - com.lzsoft.lzdata.webservice.jaxrs.upanddownloadfile.mastertheboss
            * JAX-RS 后端实现
               + com.lzsoft.lzdata.webservice.jaxrs.upanddownloadfile.mastertheboss
   * lzdata-ee8-fusionweb
      + Servlet 和 JSP 结合 实现前后端分离，以及异步数据处理的方式
         - <a id="header-index_cookbook_ch04_servlet"></a> http://localhost:8089/lzeefusionweb8/index_cookbook_ch04_servlet.jsp
      
      
      + JAX-RS
         - <a id="header-books_async"></a> http://localhost:8089/lzjaxrsweb8/exampleapi/books/async
            * 说明
               + com.lzsoft.lzdata.webservice.jaxrs.blog.BookResource
               + Book model 还是 放在 lzdata-ee8-jpa-model 模块中
      
      + 
## E:\JavaEEDev\JavaEELearningCode\lzdata-ee-8-jaxrs-new

   1. http://localhost:8088/lzdata-ee-8-jaxrs-gd/array
   3. http://localhost:8088/lzdata-ee-8-jaxrs-gd/generator
   4. http://localhost:8088/lzdata-ee-8-jaxrs-gd/object
   2. http://localhost:8088/lzdata-ee-8-jaxrs_gd/parser - 未取得数据，待查
   5. http://localhost:8088/lzdata-ee-8-jaxrs-gd/structure
   6.

### MySQL CRUD

   * Person 表
      + Create
      + Read
         1. http://localhost:8088/lzdata-ee-8-jaxrs-gd/persons
         2. http://localhost:8088/lzdata-ee-8-jaxrs-gd/resources/persons - 在 de.rieckpil.blog.JAXRSConfiguration 中设置。
         3. http://localhost:8088/lzdata-ee-8-jaxrs-gd/api/persons
         4. http://localhost:8088/lzdata-ee-8-jaxrs-gd/persons/1
         5. http://localhost:8088/lzdata-ee-8-jaxrs-gd/resources/persons/1
         6. http://localhost:8088/lzdata-ee-8-jaxrs-gd/api/persons/1
      + Update
      + Delete
   * Cusotomer
      + Read - 从 mysql 获取数据
         1. http://localhost:8088/lzdata-ee-8-jaxrs-gd/myarray - mysql data
         2. http://localhost:8088/lzdata-ee-8-jaxrs-gd/resources/myarray - 在 de.rieckpil.blog.JAXRSConfiguration 中设置@ApplicationPath("resources") 路径， 为何也可以，研究！
         3. http://localhost:8088/lzdata-ee-8-jaxrs-gd/api/myarray 在 de.rieckpil.blog.JAXRSConfiguration 中设置了 /api 路径

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
         1. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstore/save
         2. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstoremy/save
      + Read
      + Update
      + Delete
         1. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstore/remove
         2. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstore/removeall
         3. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstoremy/remove
         4. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstoremy/removeall
   
   * BiDiction   OneToMany - ManyToOne
      + Create
         1. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstore/save
         2. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstoremy/save
      + Read
      + Update
      + Delete
         1. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstore/remove
         2. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstore/removeall
         3. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstoremy/remove
         4. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/bookstoremy/removeall
   * Unidirection
      + Create
         1. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/unidirection/bookstoremy/save - addAuthorWithBooks() 有问题？！
         2. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/unidirection/bookstoremy/add - addNewBook()
      + Read
      + Update
      + Delete
         1. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/unidirection/bookstoremy/removefirst
         2. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/unidirection/bookstoremy/removelast
         3. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/unidirection/bookstoremy/removeall
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
