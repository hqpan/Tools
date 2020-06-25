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
  - `modelVerion`：4.0；
  - `groupId`：工程组标识；
  - `artificialId`：工程的标识；
  - `version`：工程版本号；
- Super POM：父 POM；
  - Super POM 无需显式定义，所有 POM 均继承自 Super POM；
  - Maven 使用 effective pom（Super POM 和工程自身的 POM）执行相关目标；
  - 在`pom.xml`文件所在的目录下执行`mvn help:effective-pom`，用于查看 Super POM 默认配置；

# TODO

- [ ] Schedule：
  - 总课时数：18；
  - 每天 3 课时，6 月 30 日完成；
  - 当前进度：3 课时；
- [ ] 每天整理 2 道面试题；

# References

[^1]: https://www.runoob.com/maven/maven-tutorial.html