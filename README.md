### 如何成为CentOS 6系统的的管理员

本教程旨在讲述如何入门CentOS 6系统的管理。

本教程的命令行遵循一般Linux系统的规则，**凡命令行开头为"#"的，表明此时正在使用root账户，而命令行开头为"$"的，则表明此时在使用普通用户**。

#### 1.初学者常用的两点

初学时，安全性常常不在考虑中，这点可以在后续的学习中逐渐完善。所以对于初学者，通常需要清空iptables和关闭selinux。

##### 1.1 清空iptables
```
# iptables -F
# service iptables save
```

##### 2.1 关闭selinux

在这之前需要首先学会[使用vim编辑器](https://www.vpser.net/manage/vi.html)。

编辑```/etc/selinux/config```文件，将以下行
```
SELINUX=enforcing
```
改成
```
SELINUX=disabled
```
然后执行命令：
```
# setenforce 0
```
