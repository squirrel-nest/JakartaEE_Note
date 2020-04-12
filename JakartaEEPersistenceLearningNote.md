
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
   * Hibernate
      + [Topical Guides](https://docs.jboss.org/hibernate/orm/5.3/topical/html_single/) - 这个指导包含所有的路径，优先参考<br>
      + [Hibernate ORM 5.3.16.Final User Guide](https://docs.jboss.org/hibernate/orm/current/userguide/html_single/Hibernate_User_Guide.html)<br>
      + [Hibernate Getting Started Guide](https://docs.jboss.org/hibernate/orm/current/quickstart/html_single/)<br>
## Persistence 与 Json
   * 参考 
      + [Persisting JSONObject Using JPA - JPA entity with JSONObject](https://ilhicas.com/2019/04/26/Persisting-JSONObject-Using-JPA.html) 非常好的指南。。学习<br>
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
## Hibernate 与 E。。
### Hibernate
   * 参考
      + [Chapter 21. Improving performance](https://docs.jboss.org/hibernate/core/3.6/reference/en-US/html/performance.html#performance-fetching-profiles)<br>

## JakartaEE 与 NoSQL
   * 参考
      + [Eclipse Jakarta NoSQL](http://www.jnosql.org/spec/) - 开发NoSQL 数据库时要看看<br>

##
