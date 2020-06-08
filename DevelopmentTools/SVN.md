[TOC]

# 1. Overview

- SVN ：Subversion；
  - 项目仅能被本地管理；
  - C/S 模式，若无网络连接，则无法进行版本控制；



# 2. 搭建 SVN 服务器端

## 2.1 初始化文件夹

- `svnadmin create folderPath`：初始化文件夹，生成3个文件；
  - svnserve.conf：服务器整体配置文件；
  - authz：授权、认证；
  - passwd：用户名、密码；
- `svnserve -d -r folderPath`：启动 SVN 服务，不能关闭命令行窗口，否则服务终止；



## 2.2 编辑配置文件

### 2.2.1 编辑 svnserve.conf 文件

- `###`：双重注解，其中的内容为真正的注解；
- `#`：单重注解，其中的内容为可选注解；
  - 删除所有单重注解前的`#`；



### 2.2.2 编辑 passwd 文件

- 编辑 passwd 文件：设置用户信息；
  - 在文件中的`[users]`处添加一行：`username = password`；



### 2.2.3 编辑 authz 文件

- 编辑 authz 文件，设置权限；
- 在文件中的`[groups]`处添加：rw 表示读写权限；
```
[/]
username = rw
```

- 在文件中的`[/foo/bar]`处添加：rw 表示读写权限；

```
username = rw
* =
```

- 在文件中的`[repository:/baz/fuz]`处，删除`* = r`语句前的注释符；