
# Jakarta EE Tutorial
## 资源
   * 项目 所在 网址
   * AsciiDoc 的 参考资料
     + process-asciidoc: Converting documents --> https://docs.asciidoctor.org/maven-tools/latest/plugin/goals/process-asciidoc/
       <details>
          <summary>
            说明
          </summary>
          主要是 转换为 html 格式的文档。 -- 我们 需要转换为 PDF。
          
          Converts Asciidoc documents using AsciidoctorJ. Additionally, the goal takes care of placing additional resources (eg. images) in the output path.
       </details>
     + AsciiDoc User Guide --> [AsciiDoc User Guide](https://asciidoc-py.github.io/userguide.html)<br>
     + AsciiDoc Syntax Quick Reference. --> [AsciiDoc Syntax Quick Reference](https://docs.asciidoctor.org/asciidoc/latest/syntax-quick-reference/)<br>
     + Publish presentation-rich content from a concise and comprehensive authoring format. --><br>[Publish presentation-rich content from a concise and comprehensive authoring format.](https://asciidoc.org/#try)<br>
## PDF 格式的 生成 步骤
   1. 下载 `Jakarta EE Tutorial` `AsciiDoc` 项目
      + eclipse-ee4j/jakartaee-tutorial --> [https://github.com/eclipse-ee4j/jakartaee-tutorial](https://github.com/eclipse-ee4j/jakartaee-tutorial)<br>
      + 下载 本地 位置
        - ```shell
              cd /Users/Codes/AsciidoctorProjects
              git clone https://github.com/eclipse-ee4j/jakartaee-tutorial.git
          ```
   2. 生成 html 文档
      + ```shell
            mvn generate-resources
        ```
      + 查看生成的 文档
        >The site is generated under target/staging. Open file:///PATH_TO_PROJECT_DIR/target/staging in a browser to view the output.
   3. 生成 PDF 文档
      1. 需要下载 

