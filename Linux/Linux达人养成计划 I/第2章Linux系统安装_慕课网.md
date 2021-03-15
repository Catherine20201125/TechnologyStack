# 第二章 Linux系统安装
![](..\imgs\第二章Linux系统安装.png)
## 虚拟机的安装
![](..\imgs\VMware安装.png)
- 虚拟机VMWare软件下载地址：<>
    - 收费。

### VMare主要特点
![](..\imgs\VMware主要特点.png)

- 快照功能：操作系统崩溃了，真实机器只能重新安装，虚拟机使用快照可以保存当前虚拟机的状态。如果虚拟机崩溃了，可以通过快照功能进行恢复。

### 建议的VMware配置
![](..\imgs\建议的VMware配置.png)


### VMware安装过程




虚拟机的时间不会太准确，因为实体机断电之后还有一块电池，但是虚拟机没有。



--------------------------------------------------------------------
-----------------------------------------------------------------------
---------------------------------------------------------------------------
# 补充：Docker安装Linux镜像
可以去docker hub（启动安装好的docker，右键，“docker hub”）看，很多镜像的，贼方便。
## 步骤
- 打开PowerShell
- 下载镜像命令： docker pull centos
- 查看镜像命令： docker images。找到centos对应的“ IMAGE ID ”列的值。
- 安装镜像命令： docker run -d -i -t  [IMAGE ID] /bin/bash。
- 查看进程命令：docker ps。
    - 安装完成后 执行 docker ps  查看 安装的镜像，如有 镜像的信息 即代表 安装成功。
    - 根据“ IMAGE ID ”的值，找到“CONTAINER ID”的值。
- 进入容器命令：docker attach  [CONTAINER ID]。
![](..\imgs\docker安装Linux镜像.png)
