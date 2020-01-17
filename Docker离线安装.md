### Author：wrkd35																Time：2020.1.14

CSDN Address：[点击前往](https://blog.csdn.net/wrkd35/article/details/103975947)

# Docker离线安装

## 1.docker的rpm安装包下载

- 下载地址：[点击前往](https://download.docker.com/linux/centos/7/x86_64/stable/Packages/)
- 下载版本：docker-ce-17.12.0.ce-1.el7.centos.x86_64.rpm

## 2.所需依赖包下载（8 + 1）

- 其中八个依赖包下载地址：[点击前往](http://mirrors.163.com/centos/7/os/x86_64/Packages/)

- 依赖包列表：

  > 1. audit-libs-python-2.8.5-4.el7.x86_64.rpm
  > 2. checkpolicy-2.5-8.el7.x86_64.rpm
  > 3. libcgroup-0.41-21.el7.x86_64.rpm
  > 4. libseccomp-2.3.1-3.el7.x86_64.rpm
  > 5. libsemanage-2.5-14.el7.x86_64.rpm
  > 6. policycoreutils-python-2.5-33.el7.x86_64.rpm
  > 7. python-IPy-0.75-6.el7.noarch.rpm
  > 8. setools-libs-3.3.8-4.el7.x86_64.rpm

- 最后一个依赖包下载地址：[百度](www.baidu.com)

  > 9. container-selinux-2.107-3.el7.noarch.rpm

## 3.安装

- 本文测试路径：`root/docker/rpm`

- 把8个依赖上传至`root/docker`路径下

- 把docker安装包和第9个依赖上传至`root/docker/rpm`路径下

- 上传成功后docker路径下的文件结构：

- 上传成功后rpm路径下的文件结构：

- 批量安装docker路径下的依赖包：`rpm -Uvh *.rpm --nodeps --force`

- 安装 container-selinux-2.107-3.el7.noarch.rpm : 

  `rpm -Uvh container-selinux-2.107-3.el7.noarch.rpm`

- 安装docker：`rpm -Uvh docker-ce-17.12.0.ce-1.el7.centos.x86_64.rpm`

- 启动docker：`systemctl start docker`

- 查看docker版本：`docker -v`

- 安装成功

# Docker Compose离线安装

## 1.下载 **Linux** 版本的 **Docker Compose**

- 下载地址：[点击前往](https://github.com/docker/compose/releases)

- 文件名：docker-compose-Linux-x86_64


## 2.安装

- 将下载下来的“**docker-compose-Linux-x86_64**”文件上传至root目录下。

- 执行如下命令将其移动到 **/usr/local/bin**，并改名为“**docker-compose**”。

  `sudo mv docker-compose-Linux-x86_64 /usr/local/bin/docker-compose`

- 执行如下命令添加可执行权限

  `sudo chmod +x /usr/local/bin/docker-compose`

- 使用 `docker-compose -v` 命令测试是否安装成功


