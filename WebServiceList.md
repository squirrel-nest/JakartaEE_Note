# Jakarta EE Project
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
