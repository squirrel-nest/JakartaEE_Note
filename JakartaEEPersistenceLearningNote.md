
# 学习资料的RoadMap
## 1. [Part VIII Persistence](https://eclipse-ee4j.github.io/jakartaee-tutorial/partpersist.html) --> [Jakarta Persistence](https://projects.eclipse.org/projects/ee4j.jpa) --> [Jakarta Persistence - Specifications](https://jakarta.ee/specifications/persistence/) --> [jakarta-ee/persistence-spec](https://github.com/jakarta-ee/persistence-spec) --> [Eclipse Yasson](https://github.com/eclipse-ee4j/yasson)<br>
🢃 ⇓  🢃  ⇓  🢃  ⇓   🢃
## 2. Youtube
      * [Configure a JDBC DataSource (PostgreSQL) for Open Liberty](https://www.youtube.com/watch?v=b2rtkYKoshA&list=PLFjB4VDnlT_1UH_Ncopre4nhCRNtBxohX)  --<br>
      * []()<br>
# 源代码的流程图（顺序）- 与学习过程的 关系图（包括 参考 的 例子，时间顺序、文件位置：Project and Package）
## 1. Source Code 的 顺序 与 位置（文件位置）
      *. persistence.xml --> jakarta-ee-8-jaxrs/src/main/resources/META-INF/persistence.xml
      *. hibernate.cfg.xml --> jakarta-ee-8-jaxrs/src/main/webapp/WEB-INF/classes/hibernate.cfg.xml
         + Example of hibernater.cfg.xml: [An example hibernate.cfg.xml for MySQL 8 and Hibernate 5](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/An-example-hibernatecfgxml-for-MySQL-8-and-Hibernate-5)<br>

## Entity-Relationship Diagram Symbols and Notation - 需要先学习
   * [Entity-Relationship Diagram Symbols and Notation](https://www.lucidchart.com/pages/ER-diagram-symbols-and-meaning)<br>
   * [Entity Relationship Diagram](https://www.smartdraw.com/entity-relationship-diagram/)<br>
      + [Build Your ERD (Database Diagram)](https://www.smartdraw.com/developers/extensions/erd.htm)<br>






# 知识点
## Persistence 相关知识点
   * Persistence.xml 位置
      + >If you package the persistent unit as a set of classes in an enterprise bean JAR file, persistence.xml should be put in the enterprise bean JAR’s META-INF directory.
        >
        >If you package the persistence unit as a set of classes in a WAR file, persistence.xml should be located in the WAR file’s WEB-INF/classes/META-INF directory.
   * Maven 与 Gradle
      + [jakarta.persistence:jakarta.persistence-api](https://search.maven.org/artifact/jakarta.persistence/jakarta.persistence-api/3.0.0-RC2/jar)<br>
      + 本地文件所在位置
         - C:\Users\w******i\.m2 - 其中 w******i 为 本地用户名 ，linux 类似。。
   * Persistence 的 Implementation - **Hibernate 与 EclipseLink**
      + Hibernate
         - **Hibernate 所有文档的索引 -- 包括quickstart、userguide 等等** [Index of /hibernate/orm/current](https://docs.jboss.org/hibernate/orm/current/)<br>
         - [Topical Guides](https://docs.jboss.org/hibernate/orm/5.3/topical/html_single/) - 这个指导包含所有的路径，优先参考<br>
         - [Hibernate ORM 5.3.16.Final User Guide](https://docs.jboss.org/hibernate/orm/current/userguide/html_single/Hibernate_User_Guide.html)<br>
         - [Hibernate Getting Started Guide](https://docs.jboss.org/hibernate/orm/current/quickstart/html_single/)<br>
         - [The Bean Validation reference implementation](http://hibernate.org/validator/)<br>
         - [Getting Started With Hibernate Annotations](https://www.codejava.net/frameworks/hibernate/getting-started-with-hibernate-annotations)<br>
         - [Chapter 21. Improving performance](https://docs.jboss.org/hibernate/core/3.6/reference/en-US/html/performance.html#performance-fetching-profiles)<br>
         - [Using latest Hibernate ORM within WildFly](https://docs.jboss.org/hibernate/orm/current/topical/html_single/wildfly/Wildfly.html)<br>
         - [Native Bootstrapping](https://docs.jboss.org/hibernate/orm/current/topical/html_single/bootstrap/NativeBootstrapping.html#_building_the_metadata)<br>
         - [Custom SessionFactory and Session Implementations Guide](https://docs.jboss.org/hibernate/orm/5.3/topical/html_single/sessionfactory/CustomSessionFactory.html)<br>
         - [Services and Registries](https://docs.jboss.org/hibernate/orm/5.3/topical/html_single/registries/ServiceRegistries.html)<br>
         - [Bytecode Enhancement](https://docs.jboss.org/hibernate/orm/5.3/topical/html_single/bytecode/BytecodeEnhancement.html)<br>
         - [JPA Static Metamodel Generator](https://docs.jboss.org/hibernate/orm/5.3/topical/html_single/metamodelgen/MetamodelGenerator.html)<br>
         - [Stored Procedures with Hibernate](https://www.baeldung.com/stored-procedures-with-hibernate-tutorial)<br>
         - [Hibernate Tutorial](https://www.javaguides.net/p/hibernate-tutorial.html) - 有空看吧<br>
         - [JSP Servlet Hibernate Web Application](https://www.javaguides.net/2019/03/jsp-servlet-hibernate-web-application.html)<br>




## Hibernate
   * 参考
      + [Hibernate Getting Started Guide](https://docs.jboss.org/hibernate/orm/6.0/quickstart/html_single/)<br>
      + [Getting started with Hibernate ORM](http://hibernate.org/orm/documentation/getting-started/)<br>
      + [Hibernate ORM 6.0.0.Alpha6 User Guide](https://docs.jboss.org/hibernate/orm/6.0/userguide/html_single/Hibernate_User_Guide.html#annotations-jpa-onetoone)<br>
      + [Hibernate Search 6.0.2.Final: Reference Documentation](https://docs.jboss.org/hibernate/search/6.0/reference/en-US/html_single/#preface)<br>
   * 关于 hibernate.cfg.xml
      + 默认文件位置应该放在 classpath（E:\JavaEEDev\JavaEELearningCode\lzdata-ee-8-jaxrs-new\src\main）目录下的 resources 目录中
      + 如果要指定目录，则设置时要指定：/resources/config/hibernate.cfg.xml，如：
      ```java
         ...
         sessionFactory = new Configuration()
                    .configure("/resources/config/hibernate.cfg.xml")
                    .addAnnotatedClass(Customer.class)
                    .buildSessionFactory();
         ...
      ```

### Hibernate 与 Jakarta 9
   * 参考
      + Hibernate ORM (5.5 开始支持 Jakarta)--> [https://hibernate.org/orm/releases/5.5/](https://hibernate.org/orm/releases/5.5/)<br>
      + Getting started with Hibernate ORM (重点要看) --> [https://hibernate.org/orm/documentation/getting-started/](https://hibernate.org/orm/documentation/getting-started/)<br>
      + Hibernate ORM 5.5.4.Final User Guide -- [Hibernate ORM 5.5.4.Final User Guide](https://docs.jboss.org/hibernate/stable/orm/userguide/html_single/Hibernate_User_Guide.html)<br>
      + Hibernate ORM 5.5.0.Final released -- 这里有使用Jakarta 9 的 **权威** 设置说明 --> [https://in.relation.to/2021/06/02/hibernate-orm-550-final-release/](https://in.relation.to/2021/06/02/hibernate-orm-550-final-release/)<br>
      + Migrating from JPA 2.x to 3.0 -- (辅助教程, 可以不看) --> [https://thorben-janssen.com/migrating-jpa-2-x-to-3-0/](https://thorben-janssen.com/migrating-jpa-2-x-to-3-0/)<br>
      + Hibernate ORM 5.5.4.Final released --> [https://in.relation.to/2021/07/19/hibernate-orm-554-release/](https://in.relation.to/2021/07/19/hibernate-orm-554-release/)<br>
### Hibernate 教程
   * [Mapping Java Entities for Persistence in Hibernate (Part 1)](https://dzone.com/articles/mapping-java-entities-for-persistence-in-hibernate)<br>
   * [Mapping Java Entities for Persistence With Hibernate (Part 2)](https://dzone.com/articles/mapping-java-entities-for-persistence-with-hiberna)<br>
   * [Mapping Java Entities for Persistence With Hibernate (Part 3)](https://dzone.com/articles/mapping-java-entities-for-persistence-with-hiberna-1)<br>
   * [Mapping Java Entities for Persistence With Hibernate (Part 4)](https://dzone.com/articles/mapping-java-entities-for-persistence-with-hiberna-2)<br>
   * 项目中Hibernate的部分参考过下面教程：[Hibernate Framework](https://github.com/RameshMF#hibernate-framework)<br>
   * [Hibernate One to Many Annotation Tutorial](https://www.baeldung.com/hibernate-one-to-many)<br>
   * [Hibernate’s Read-Only Query Hint For Faster Read Operations](https://thorben-janssen.com/read-only-query-hint/)<br>

### Persisting Maps with Hibernate
   * 参考
      + [Annotation Type OneToOne](https://jakarta.ee/specifications/platform/8/apidocs/javax/persistence/OneToOne.html)<br>
      + [Persisting Maps with Hibernate](https://www.baeldung.com/hibernate-persisting-maps)<br>
      + [Mapping LOB Data in Hibernate](https://www.baeldung.com/hibernate-lob)<br>
   * 问题处理
      + Exception handling request to /lzjaxrsweb8/exampleapi/dbmovies: org.jboss.resteasy.spi.UnhandledException: java.lang.RuntimeException: java.lang.IllegalArgumentException: org.hibernate.hql.internal.ast.QuerySyntaxException: Movie is not mapped [from Movie order by title]
      + org.hibernate.UnknownEntityTypeException: Unable to locate persister: com.lzsoft.lzdata.persistence.hibernate.model.movie.Movie
      + 以上两个问题需要修改，增加 .addAnnotatedClass(Movie.class)
      + ```java
                     sessionFactory = new Configuration()
                    .configure("hibernate.cfg.xml")
                    .addAnnotatedClass(Customer.class)
                    .addAnnotatedClass(Student.class)
                    .addAnnotatedClass(Movie.class)
                    .buildSessionFactory();
        ```

### Quarkus & Hibernate – Getting Started
   * 参考
      + Quarkus & Hibernate – Getting Started --> [https://thorben-janssen.com/quarkus-hibernate/](https://thorben-janssen.com/quarkus-hibernate/)<br>

### Data Rationship
   * [JPA and Hibernate Many To Many Relationship Mapping Example with Spring Boot and MySQL](https://hellokoding.com/jpa-many-to-many-relationship-mapping-example-with-spring-boot-maven-and-mysql/)<br>
### Hibernate - Query Language
   * [Hibernate - Query Language](https://www.tutorialspoint.com/hibernate/hibernate_query_language.htm)<br>
   * [JPA Query Parameters Usage](https://www.baeldung.com/jpa-query-parameters)<br>
   * [Hibernate Query Language Tutorial](https://www.javaguides.net/2019/10/hibernate-query-language-tutorial.html)<br>
   * [Hibernate Query Language (HQL) Example](https://www.codejava.net/frameworks/hibernate/hibernate-query-language-hql-example)<br>
   * [Best Performance Practices for Hibernate 5 and Spring Boot 2 (Part 1)](https://dzone.com/articles/50-best-performance-practices-for-hibernate-5-amp)<br>
   * [Passing query parameters through your WebClient](https://blog.knoldus.com/passing-query-parameters-through-your-webclient/)<br>

## EclipseLink
   * 参考
      + EclipseLink -- [https://www.eclipse.org/eclipselink/](https://www.eclipse.org/eclipselink/)<br>
    

## Testing JPA-based applications
   * [Chapter 18. Testing JPA-based applications](https://livebook.manning.com/book/junit-in-action-second-edition/chapter-18/)<br> 


## Persistence 与 Json
   * 参考 
      + [Persisting JSON change via AttributeConverter to database using Quarkus and Hibernate](https://stackoverflow.com/questions/59115776/persisting-json-change-via-attributeconverter-to-database-using-quarkus-and-hibe) - 用到Quarkus and Hibernate，有时间看看<br>
         - [QUARKUS - SIMPLIFIED HIBERNATE ORM WITH PANACHE](https://quarkus.io/guides/hibernate-orm-panache#transactions)<br>
      + Converter 的使用
         - [JPA Attribute Converters](https://www.baeldung.com/jpa-attribute-converters) 有空一定要试试<br>
      + [Persisting JSONObject Using JPA - JPA entity with JSONObject](https://ilhicas.com/2019/04/26/Persisting-JSONObject-Using-JPA.html) 很好的指南。。学习。。但是，Hibernate无法实现:=(<br>
         * 代码样例
            - ```java
              package com.ilhicas.converters;

              import org.json.JSONArray;
              import org.json.JSONException;

              import javax.persistence.AttributeConverter;
              import javax.persistence.Converter;

              @Converter
              public class JSONObjectConverter implements AttributeConverter<JSONObject, String> {
                  @Override
                  public String convertToDatabaseColumn(JSONObject jsonData) {
                      String json;
                      try{
                          json = jsonData.toString();
                      }
                      catch (NullPointerException ex)
                      {
                          //extend error handling here if you want
                          json = "";
                      }
                      return json;
                  }

                  @Override
                  public JSONObject convertToEntityAttribute(String jsonDataAsJson) {
                      JSONObject jsonData;
                      try {
                          jsonData = new JSONObject(jsonDataAsJson);
                      } catch (JSONException ex) {
                          //extend error handling here if you want
                          jsonData = null;
                      }
                      return jsonData;
                  }
              }
            ```
          - ```java
              @Entity
              @Data
              @Table(name = "users")
              public class User {
                  @Id
                  private Long id;

                  @NonNull
                  private String username;

                  @NonNull
                  @Column(columnDefinition = "TEXT")
                  @Convert(converter= JSONObjectConverter.class)
                  private JSONObject jsonData;
              }
           
            ```
          - ```java
              ...
              @Autowired
              private UserRepository userRepository;

              public void someMethod()
              {
                  User example = userRepository.findByUsername("ilhicas");
                  System.out.println(example.getJsonData().getString("KEY") )
                  //prints out value for key

                  JSONObject toSet = new JSONObject();
                  toSet.put("SOME_OTHER_KEY", "SOME_VALUE")
                  example.setJsonData(toSet);
                  userRepository.save(example);
                  //Saves our user uson jsonData from our JSONObject
              }
              ...
            ```
      + MySQL 的 JSON 字段 的 解决方案 （临时）
         - hibernate-types 源代码 --> [vladmihalcea/hibernate-types](https://github.com/vladmihalcea/hibernate-types/tree/master/hibernate-types-52)<br>
         - MySQL JSON字段的例子 --> [aelgali/jpa-mysql-json-sample](https://github.com/aelgali/jpa-mysql-json-sample)<br>
         - 例子 --> [mopano/hibernate-json-type](https://github.com/mopano/hibernate-json-type)<br>
         - [How to fix the Hibernate “No Dialect mapping for JDBC type” issue](https://vladmihalcea.com/hibernate-no-dialect-mapping-for-jdbc-type/)<br>
         - [How to map a String JPA property to a JSON column using Hibernate](https://vladmihalcea.com/map-string-jpa-property-json-column-hibernate/)<br>
         - [How to map JSON objects using generic Hibernate Types](https://vladmihalcea.com/how-to-map-json-objects-using-generic-hibernate-types/)<br>
         - [Hibernate PostgreSQL JSONB issue: No Dialect mapping for JDBC type: 1111](https://discourse.hibernate.org/t/hibernate-postgresql-jsonb-issue-no-dialect-mapping-for-jdbc-type-1111/1612) - 如参考上一篇，如果上一篇解决<br>
         - [How to map a JSON hierarchy with JPA and Hibernate](https://discourse.hibernate.org/t/how-to-map-a-json-hierarchy-with-jpa-and-hibernate/2380)<br>
         - [How to store schema-less EAV (Entity-Attribute-Value) data using JSON and Hibernate](https://vladmihalcea.com/how-to-store-schema-less-eav-entity-attribute-value-data-using-json-and-hibernate/)<br>
         - [How to map a map JSON column to Java Object with JPA](https://stackoverflow.com/questions/25738569/how-to-map-a-map-json-column-to-java-object-with-jpa)<br>
         - [How to map a MySQL JSON column to a Java entity property using JPA and Hibernate -](https://stackoverflow.com/questions/44308167/how-to-map-a-mysql-json-column-to-a-java-entity-property-using-jpa-and-hibernate)<br>
         - [How to use Hibernate 5.2.10 MySQL JSON support without AttributeConverter or customUserType to map to Java Entity Class?](https://stackoverflow.com/questions/44445417/how-to-use-hibernate-5-2-10-mysql-json-support-without-attributeconverter-or-cus) - 有空的话参考下面提到的例子<br>
         - [12.17.3 Functions That Search JSON Values](https://dev.mysql.com/doc/refman/8.0/en/json-search-functions.html)<br>
         
         - [How to add a data access layer to your Wicket app using Hibernate and Spring JPA with minimal code](https://www.coderdreams.com/how-to-add-a-data-access-layer-to-your-wicket-app-using-hibernate-and-spring-jpa-with-minimal-code/)<br>
            * 代码 - [RomanSery/codesnippets](https://github.com/RomanSery/codesnippets)<br>
         - [Using MySQL JSON columns to simplify your data storage: Part 1](https://www.coderdreams.com/using-mysql-json-columns-to-simplify-your-data-storage-part-1/)<br>
         - [Using MySQL JSON columns to simplify your data storage: Part 2](https://www.coderdreams.com/using-mysql-json-columns-to-simplify-your-data-storage-part-2/)<br>

## CRUD（数据库的增删改查）
   * 参考
      + [JSP Servlet Hibernate CRUD Example](https://www.javaguides.net/2019/03/jsp-servlet-hibernate-crud-example.html)<br>
         - 源代码 --> [jsp-servlet-hibernate-mysql-tutorial](https://github.com/RameshMF/jsp-servlet-hibernate-mysql-tutorial)<br>
      + [Hibernate Registration Form Example with JSP, Servlet, MySQL](https://www.javaguides.net/2019/11/hibernate-registration-form-example-with-jsp-servlet-mysql.html)<br>
      + [Login Form using JSP + Servlet + Hibernate + MySQL Example](https://www.javaguides.net/2019/11/login-form-using-jsp-servlet-hibernate-mysql-example.html)<br>
      + [MapStruct Example of Mapping JPA and Hibernate Entity to DTO](https://hellokoding.com/mapping-jpa-hibernate-entity-and-dto-with-mapstruct/)<br>
      + [Don’t expose your JPA entities in your REST API](https://thoughts-on-java.org/dont-expose-entities-in-api/)<br>
      + [Deleting Data in Spring Boot with JPA and Hibernate](https://hellokoding.com/deleting-data-with-jpa-hibernate/)<br>
      + Spring 架构
         - [Spring Boot, Spring Data JPA – Building Rest CRUD API example](https://bezkoder.com/spring-boot-jpa-crud-rest-api/)<br>
         - [Spring Data REST Example – Spring Boot RESTful API + CRUD](https://javainterviewpoint.com/spring-data-rest-example/)<br>
         - [Spring Boot JPA One To One Example with MySQL | Unidirectional & Bidirectional](https://javainterviewpoint.com/spring-boot-jpa-one-to-one-example/)<br>
         
## JakartaEE 与 NoSQL
   * 参考
      + [Eclipse Jakarta NoSQL](http://www.jnosql.org/spec/) - 开发NoSQL 数据库时要看看<br>
   * Hibernate
      + [NoSQL datastores](http://hibernate.org/ogm/)<br>
      + [Getting started with Hibernate OGM](http://hibernate.org/ogm/documentation/getting-started/)<br>
      + [Hibernate OGM - Documentation](http://hibernate.org/ogm/documentation/)<br>
      + [Run Hibernate OGM with WildFly and MongoDB as a beginner](https://discourse.hibernate.org/t/run-hibernate-ogm-with-wildfly-and-mongodb-as-a-beginner/2799)<br>
      + hibernate-ogm 源代码 - [hibernate/hibernate-ogm](https://github.com/hibernate/hibernate-ogm)<br>
      + [MySQL and MongoDB together](https://discourse.hibernate.org/t/mysql-and-mongodb-together/1846)<br>
   * Sample
      + [platformsh/java-quick-start/jakarta/tomee-mongodb](https://github.com/platformsh/java-quick-start/tree/master/jakarta/tomee-mongodb) - 待看<br>
## JakartaEE Pagination -- 关于分页的知识点 
   * NoSql
      + [Handling Pagination With JAX-RS and NoSQL in Your Jakarta EE/MicroProfile Application](https://dzone.com/articles/handling-with-pagination-with-jax-rs-in-your-jakar)<br>
      + [Improving Performance at NoSQL Query With Pagination](https://dzone.com/articles/improving-performance-at-nosql-query-with-paginati)<br>
   * Hibernate
      + [Hibernate Pagination](https://www.baeldung.com/hibernate-pagination)<br>
