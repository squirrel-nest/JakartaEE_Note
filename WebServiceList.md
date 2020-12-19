# Jakarta EE Project
## 说明
   * 框架搭建分为 Jakarta EE 8 和 Jakarta EE 9， 以 Jakarta EE 8 作为开发的主线, Jakarta EE 9通过拷贝 Jakarta EE 8来获得, 然后修改 javax 包名 到 jakarta, 共用的模块用 _share_ 或 _common_ 
   * 总项目文件夹：E:\JavaEEDev\JavaEELearningCode\lzdata-ee-9-gdev
   * 关于 字符集 CharSet 与 编码 Encoding：所采用的方式，有模块中单独说明。。。
   * 关于 绝对路径 和相对路径的说明
      + JSP 页面 通过 ${pageContext.request.contextPath} + "Relative Path" 来设置 href tag（标签）
      + Sevelet中的设置，通过：
         1. response.sendRedirect("${pageContext.request.contextPath}/customer/list"); 还是 
            response.sendRedirect(${pageContext.request.contextPath + "/customer/list");
      + Html5页面 是 静态页面，所以只能通过 . 、.. 、/ 等 路径符号来设置
         - 相关设置的方法
            >1. /   = Root directory<br>
            >2. .   = This location<br>
            >3. ..  = Up a directory<br>
            >4. ./  = Current directory<br>
            >5. ../ = Parent of current directory<br>
            >6. ../../ = Two directories backwards<br>

## 问题汇总
   1. 。。
### 分项目
   * lzdata-ee8-servletweb
      + 说明
         1. 模块的架构
            - 中间层Java文件放在模块 lzdata-ee8-servlet-base 中, 通过 lzdata-ee8-servlet-base 模块 调用 数据接入层模块 lzdata-ee8-jpa-model，lzdata-ee8-jpa-model 属于共用模块 其他模块 也可以 调用。。。lzdata-ee8-jpa-model模块参见 数据接入层中，Jakarta Pesistence 模块 的说明。。。
      + 例子
         - JSP 的例子 - 仅JSP页面的例子
            1. http://localhost:8089/lzservletweb8/index.jsp  --> jakartaee-9
               * 说明
                  + 例子来源：[mastertheboss - jakartaee-9](https://github.com/fmarchioni/mastertheboss.git) -- E:\JavaEESamples\JakartaEE9\mastertheboss\jakartaee\jakartaee-9
                  + 字符集编码 采用 网页级 设置
                  + 没有用 web.xml --> 如果要用可以设置web.xml <welcome-file>index.jsp</welcome-file>
            2. http://localhost:8089/jakartaee-9/helloworldnew.jsp -- 结合嵌入的 java 语言
         - JSP 与 Servlet 结合的例子，实现前后端的分离 -- 网页中不用嵌入的Java了，使得 维护方便了。。。
            1. http://localhost:8089/lzservletweb8/ 默认为 index.html   --> Source：jakartaee-9
            2. http://localhost:8089/jakartaee-9/index.html
               * 1 ~ 2 的说明
                  + 编码设置通过
                     1. Servlet 中，添加 resp.setContentType("text/html;charset=UTF-8");
                     2. 网页中设置 UTF-8 的编码
                  + 网页： index.html 、 index_org.html
                  + Servlet
                     1. org.jboss.as.quickstarts.helloworld.HelloService
                     2. org.jboss.as.quickstarts.helloworld.HelloWorldServlet
            3. http://localhost:8089/jakartaee-9/index_push.html or http://localhost:8089/jakartaee-9/ServerPush
              * 说明
                 + 编码 - 没有设置，因此是乱码：）
                 + 无法显示图片，增加：pb.path(request.getContextPath() -- 解决：pb.path(request.getContextPath() + "/images/javaee-logo.png")
                 + 网页：http://localhost:8089/jakartaee-9/index_push.html
                 + Servlet
                    1. com.lzsoft.lzdata.weblogic.servlet.ServerPush
   * REST Service (JAX-RS)
      + project module 
         - lzdata-ee8-jaxrsweb --> lzdata-ee8-jaxrs-base --> lzdata-ee8-jpa-model
            1. http://localhost:8089/lzjaxrsweb8/index.jsp - 输入对象，转换为json，并输出网页。
               - --> http://localhost:8089/lzjaxrsweb8/exampleapi/jsonb/tojson
                  * com.lzsoft.lzdata.webservice.jaxrs.person.itbuzzpress.JsonService
            2. http://localhost:8089/lzjaxrsweb8/index_todb.jsp - 输入数据存入数据库，然后从数据库中取出，用json格式展示在网页。
               - http://localhost:8089/lzjaxrsweb8/exampleapi/jsonb/dbtojson
                  * com.lzsoft.lzdata.webservice.jaxrs.person.itbuzzpress.DatabaseJsonService
            3. http://localhost:8089/lzjaxrsweb8/index_restfile_angular.jsp 上传下载文件
            4. http://localhost:8089/lzjaxrsweb8/index_restfile_purejsp.jsp
               - com.lzsoft.lzdata.webservice.jaxrs.upanddownloadfile.mastertheboss
            5. com.lzsoft.lzdata.webservice.jaxrs.book.BookResource - book crud
            6. http://localhost:8089/lzjaxrsweb8/exampleapi/hello -- {"message":"Duke says 你好，Jakarta EE 9！(Hello to Jakarta EE 9!)!"}
            7. http://localhost:8089/lzjaxrsweb8/exampleapi/greeting/美女 -- {"message":"Say Hello to 美女 at 2020-12-13T22:33:47.362864"}

## E:\JavaEEDev\JavaEELearningCode\lzdata-ee-8-jaxrs-new

   1. http://localhost:8088/lzdata-ee-8-jaxrs-gd/array
   3. http://localhost:8088/lzdata-ee-8-jaxrs-gd/generator
   4. http://localhost:8088/lzdata-ee-8-jaxrs-gd/object
   2. http://localhost:8088/lzdata-ee-8-jaxrs_gd/parser - 未取得数据，待查
   5. http://localhost:8088/lzdata-ee-8-jaxrs-gd/structure
   6.
   9. 如下
      1. http://localhost:8088/lzdata-ee-8-jaxrs--gd/quotes - 不行！ 没有设置。。。
      2. http://localhost:8088/lzdata-ee-8-jaxrs--gd/resources/quotes - 可以！
      3. http://localhost:8088/lzdata-ee-8-jaxrs--gd/api/quotes - 可以！
  10. http://localhost:8089/lzdata-ee-8-jaxrs-gd/resources/users  - Get Data from Web Api
### MySQL CRUD
   * fruits 表
      + Create
      + Read（Query) - 从 mysql 获取数据
         10. http://localhost:8088/lzdata-ee-8-jaxrs-gd/api/fruits  - How to Create and Delete?
      + Update
      + Delete
   * books
      + Create
      + Read - 从 mysql 获取数据
         11. http://localhost:8088/lzdata-ee-8-jaxrs-gd/books
         12. http://localhost:8088/lzdata-ee-8-jaxrs-gd/books/async
         13. http://localhost:8088/lzdata-ee-8-jaxrs-gd/books/3
      + Update
      + Delete
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
   * [eugenp
/
tutorials/patterns/design-patterns-architectural/](https://github.com/eugenp/tutorials/tree/master/patterns/design-patterns-architectural)<br>
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
