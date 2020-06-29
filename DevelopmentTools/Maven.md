[toc]

# 版权声明

- Maven 学习笔记来源菜鸟教程网站[^1]；
- 该笔记不以盈利为目的，仅用于个人学习、交流讨论及科学研究；
- 如有侵权，请与本人联系（hqpan@foxmail.com），经核实后即刻删除；
- 本文采用 [署名-非商业性使用-禁止演绎 4.0 国际 (CC BY-NC-ND 4.0)](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh) 协议发布；

# 1. Maven 概述

- Maven：n. [C]，专家；
  - 版本：Maven 3.0；
  - 项目管理工具；

# 2. POM

- POM：Project Object Model，项目对象模型；
  - `project`：工程根标签；
  - `modelVerion`：对于 Maven，该值必须为 4.0；
  - `groupId`：项目组标识；
  - `artifactId`：n.[C] 手工制品，项目 ID；
  - `version`：版本，E.g. X.X.X-里程碑；
    - 第 1 个 X：大版本，重大变革；
    - 第 2 个 X：小版本，修复 bug，增加功能；
    - 第 3 个 X：更新；
    - 里程碑版本：
      - SNAPSHOT：快照，开发版；
      - alpha：内部测试版；
      - beta：公开测试版；
      - Release|RC：发布版；
      - GA：正常版本；
  - `name`：可声明一个对用户更友好的项目名；
  - 注意：Maven 通过“gav”（groupId，artifactId，version）可确定任一项目的坐标；
- 目录结构：
  - `basedir`：根目录，存放`pom.xml`和所有子目录
  - `basedir/src/main/java`：项目的 Java 代码；
  - `basedir/src/main/resources`：项目的资源；
  - `basedir/src/test/java`：项目的测试类；
  - `basedir/src/test/resources`：测试使用的资源；
- Super POM：父 POM；
  - Super POM 无需显式定义，所有 POM 均继承自 Super POM；
  - Maven 使用 effective pom（Super POM 和工程自身的 POM）执行相关目标；
  - 在`pom.xml`文件所在的目录下执行`mvn help:effective-pom`，用于查看 Super POM 默认配置；

```xml
<dependencies>
    <dependency>
        <!-- 依赖的 gav -->
        
        <!-- 表示范围，仅在测试时包含该jar包 -->
        <scope>test</scope>
    </dependency>
</dependencies>
```



# 3. Maven 构建生命周期

- Maven 具有的生命周期：
  - clean：项目清理；
  - default/build：项目部署；
  - site：创建项目站点文档；

# TODO

- [ ] Schedule：
  - 总课时数：18；
  - 每天 3 课时，6 月 30 日完成；
  - 当前进度：6 课时；
- [ ] 每天整理 2 道面试题；

# References

[^1]: https://www.runoob.com/maven/maven-tutorial.html