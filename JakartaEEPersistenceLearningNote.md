
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
