
# 学习资料的RoadMap
## 1. [Part VIII Persistence](https://eclipse-ee4j.github.io/jakartaee-tutorial/partpersist.html) --> [Jakarta Persistence](https://projects.eclipse.org/projects/ee4j.jpa) --> [Jakarta Persistence - Specifications](https://jakarta.ee/specifications/persistence/) --> [jakarta-ee/persistence-spec](https://github.com/jakarta-ee/persistence-spec) --> [Eclipse Yasson](https://github.com/eclipse-ee4j/yasson)<br>
🢃 ⇓  🢃  ⇓  🢃  ⇓   🢃
## 2. Youtube
   * [Configure a JDBC DataSource (PostgreSQL) for Open Liberty](https://www.youtube.com/watch?v=b2rtkYKoshA&list=PLFjB4VDnlT_1UH_Ncopre4nhCRNtBxohX)  --<br>
   * []()<br>
# 源代码的流程图（顺序）- 与学习过程的 关系图（包括 参考 的 例子，时间顺序、文件位置：Project and Package）
## 2. Source Code 的 顺序 与 位置（文件位置）

   1. persistence.xml --> jakarta-ee-8-jaxrs/src/main/resources/META-INF/persistence.xml
   2. hibernate.cfg.xml --> jakarta-ee-8-jaxrs/src/main/webapp/WEB-INF/classes/hibernate.cfg.xml





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
## Persistence 与 Json
   * 参考 
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
         - [Using MySQL JSON columns to simplify your data storage: Part 1](https://www.coderdreams.com/using-mysql-json-columns-to-simplify-your-data-storage-part-1/)<br>
         
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
##
